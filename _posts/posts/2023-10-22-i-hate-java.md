---
layout: post
title: I Hate JAVA
updated: 2023-10-22
category: posts
---

I hate Java. And in this post, I'll talk about why I hate its type system. Maybe in the future I'll write about why I hate its other stuff.

Types in Java are all very well and good and neat until you want to do ANYTHING with generics. Generics in Java are busted.

If you're familiar with types and generics already, skip down to the orange text that says "skipped to here", but my mother reads this blog, so I'll write a pretty explanation :)

For the unfamiliar, a type in programming is the, well, type of thing you're storing in a variable. For example, if I'm storing an integer in a variable, then the variable's type is integer.

In Java, once the type of a variable is set, it can't be changed. This means that if I declare `Integer faces = 6`, I can't then do `faces = "hello"`, because "hello" is a string, and strings can't be put in integers, because they aren't the same. This is pretty cool because it means you can do faces / 2 and you know that it will work, because faces must be a number rather than something else. For example, it wouldn't make sense to divide a string. This way, you know for sure that you're dividing something that you can divide.

Java also has inheritance. This means that custom types that you create can be compatible with each other in a tree-like manner. For example, in a video game, there might be an Actor type which represents any in-world object, and then more specific versions of an Actor which are said to extend from that Actor. For example, the Player is a version of an Actor. A Box is a version of an Actor. Both Player and Box extend Actor.

In Java, everything, including numbers, strings, and custom types, extends from the base class called Object. This means that you can store anything in an Object. It just won't be very useful because now that it's treated as an Object, you can't access any of the more specific properties that it had before. If I store an Actor as an Object, I can't `.move` it because it looks like an Object now. Remember this, you'll need it later. **Everything in Java extends from Object**.

The useful thing here is that if the variable's type is labelled as Actor, then anything that extends Actor can actually be put into that variable! This means that you can store any kind of Actor, which is extremely useful in a game context: if you want to move the Actor within the world, you can call `actor.move()` without needing to care about what kind of Actor it is, only that it is an Actor and that it supports being moved, because both Players and Boxes are Actors and they support being moved as a result.

Sometimes, types don't extend from each other, but you will want to be able to operate on any type because what you're doing doesn't depend on the interface of the type. For example, if I want to put something into a list, the list doesn't need to care about what type of thing goes into it, since the list can store anything. All that matters is that the thing is stored.

One way of accomplishing this would be to make the list store a list of Objects, because anything can go into an Object.

Unfortunately, this isn't very useful when I want to get stuff out of the list, because it'll just look like an Object. What we really want is a list that treats things like Objects when it stores them, but when things are put into and taken out of the list they look like whatever type I want, like an Integer, or a String, or an Actor, or anything. This is accomplished through generics.

If I write `List<Integer>` then I have created a List that can store Integers. When I try to run code like `list.add(2)` the computer will check that the thing I'm trying to add is actually an Integer, and it'll produce an error when compiling if I try to add anything else, like a String, with `list.add("hello")`, because String isn't an Integer and it doesn't extend Integer. However, once the list takes over control of code execution, it secretly treats the thing I'm adding as an Object, because the list doesn't need to know what I'm storing.

When coding a definition using generics, they're represented as `<T>`, where T stands for any type. For example, `List<T>`. When using generics, you just write `<Integer>` with whatever type you actually want to use. For example, `List<Integer>`.

Executed well, this can be a good system.

Java does not execute it well.


<font color="orange">If you already know how types work, you should have skipped to here as directed above.</font>


I have three main gripes with generics so far, and it seems that every time I try to do anything interesting in Java I discover a brand new gripe and eventually just give up because I cannot do the thing that I want to do.

## Primitive generics

Java actually has two kinds of integer: an `int` and an `Integer`. The first one is called a primitive type and the second one is called a reference type. Remember how I said everything extends from Object? Not really. Primitive types don't. This means that you can't use the primitive type `int` in a list. Even though a sensible person might think that `List` should work, it doesn't, because Java secretly requires generics to extend Object. This freaking sucks.

Fortunately, this one has a relatively simple solution, which involves just using the other kind of integer. So I can store numbers in a list, thank god.

## Generic arrays

Java also have multiple kinds of lists. One of these is called List. It lets you add things to the end, to the start, between other things, and then remove things from any position. It's pretty useful for those reasons.

The other kind of list is called an array, and it's a special snowflake. It's not represented as a type, it's represented as "array of (thing)". It doesn't go into generics. Once created, it has a fixed size. You can't use the metaphor of inserting or removing elements, you can only overwrite an element at a specific slot, because all the slots are placeholders that are created ahead of time. You cannot add or remove slots once it's created. This array can hold primitive types, and reference types, but you can't create an array of generic: `new T[]` does not compile. Java says that "generic array creation is forbidden" which is some top tier crap if you ask me.

You can work around this by doing the second worst hack in the world: Create an array of object, then cast it to an array of generic type. You also have to suppress unchecked type warnings. `T[] someArray = (T[]) new Object[]`

This is horrible and I have no idea why Java won't let me just make a generic array because it seems like a thing that I should definitely be able to do. I hate this.

## Generic extends

Remember how I said it was really cool that you can put a Box into an Actor and then pretend that it's an Actor? How it was really useful and stuff? Yeah, you can't do that with generics.

List<Box> boxList = new List<Box>();
List<Actor> actorList = boxList;

This doesn't compile because you can't put `List<Box>` into `List<Actor>`, which is just really dumb. You should really be able to do this. It's compatible.

This brings me to the world's worst workaround, which I just discovered today while needing to do this. You have to create this method:

@SuppressWarnings("unchecked")
private static <T extends Actor> List<Actor> convertToActor(List<Box> boxList) {
   return (List<Actor>) boxList;
}

This is horrible. This is the worst thing. I hate Java for making me do this.

In my opinion, because this is a personal blog on which I can write opinions, these are decisions that make Java a bad programming language.

Stay tuned for tomorrow when I might write about what I actually needed this monstrous code for. I'll tell you that it has something to do with writing tests in Java.

A highlight from today's music bracket: [Prappe - ウタヲキカセテ 【夢リミックス】](https://epicord.bandcamp.com/track/--6)

I do not know what this means, but it's very pretty, especially the last 26 seconds.

-- Swarn
