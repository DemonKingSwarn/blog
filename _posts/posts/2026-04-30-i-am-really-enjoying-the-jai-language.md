---
layout: post
title: i am really enjoying the jai language
updated: 2026-04-30
excerpt: "in this post i discuss about how i am enjoying programming in the jai language which is being developed by jonathan blow."
keywords: [jai language, jonathan blow, experience in jai]
category: posts
---

hey guys,

so a month back on March of 2026, i got into the jai closed beta. to those who dont know, i will try my best to explain what jai is:

its a new systems programming language made by Jonathan Blow, known for The Witness and Braid. he originally created this language as he was frustrated with c++ and felt none of the other languages were addressing what they needed or dont understand their own programs. so he started working on jai.

jai is what c++ should have been, it brings back the joy of programming with some of the really cool features which are microprogramming, compile time execution, etc.

---

so with all that, lets begin with a "Hello, World!" in jai.

so i am using linux, so for me the compiler is

> `jai-linux`: the main jai compiler
> `lld-linux`: the linker

in jai, the "Hello, World!" is "Hello, Sailor!" as Jonathan Blow says it. so we are gonna use that terminology here as well.

```jai
#import "Basic";

main :: () {
    print("Hello, Sailor!\n");
}
```

another thing about jai, which makes it different from c++ is that you dont need to have the import, or "include" statement right at the top. you can have it at the bottom itself.

```jai
main :: () {
    print("Hello, Sailor!\n");
}

#import "Basic";
```

the jai compiler is smart enough to understand where you defined it.

to compile our program, you basically do this:

```sh
jai-linux main.jai
```

it will create a binary called `main`, also you can "autorun" the binary right after it compiled.

```sh
jai-linux main.jai +Autorun
```

this will compile and then execute the binary

output:
```sh
Hello, Sailor!
```

also you can make the compiler "quiet" by adding the following flags while compiling

```sh
jai-linux main.jai -quiet +Autorun
```

---

in jai, essentially your build script is written in the language itself, for example, this is how a first.jai would essentially look. in jai the build script is called `first.jai`.

```jai
#import "Basic";
#import "Compiler";

#run build();

build :: () {
    w := compiler_create_workspace("First Jai Program");

    options := get_build_options(w);

    options.output_executable_name = "our_first_program_in_jai";

    set_build_options(options, w);

    compiler_begin_intercept(w);
    add_build_file("main.jai", w);

    compiler_end_intercept(w);

    set_build_options_dc(.{ do_output = false });
}

```

the `#run` tells the compiler that this needs compile-time execution. and then you can just do:

```sh
jai-linux first.jai
```

---

so i have been enjoying jai so much, that i started working on my second steam release using this language itself. i am really having ufn programming in this language, i will be sharing the development and progress over my [twitter](https://x.com/demonkingswarn) and [bluesky](https://bsky.app/profile/demonkingswarn.live), so make sure to follow me there.

and this is all for today's blog, i will see you guys in the next one. till then, take care and good bye.
