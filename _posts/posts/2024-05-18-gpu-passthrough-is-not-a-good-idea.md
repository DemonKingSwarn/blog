---
layout: post
title: GPU Passthrough is not a Good Idea for Gamers on Linux
updated: 2024-05-18
category: posts
---

Hey everyone,

Gaming on Linux in the year 2024 is just incredible. Valve's compatibility layer Proton but also advancements to the tools running beneath the Proton have really changed the game. Gaming on Linux have become just click and play most games but what about those wont work? Well the most games which don't work are the ones which has kernel level anti-cheats. Many in the online community has setup a virtual machine (VM) passing their GPU through to it and let me just say that this isn't a good idea.

While GPU passthrough is a cool concept that allows you to run a VM and assign resources to it from the underlying host, it's not ideal for gaming, especially if you are trying to bypass anti-cheat limitations.

Here are the reasons why it is not a good idea:

- **Terms of Service Violation:** Using VMs to play games often violates the terms of services of the game or the anti-cheat itself.

- **Risk of Getting Banned:** Even if you manage to bypass detection and avoid getting banned initially, the game developers can change their policy at any time, resulting in a permanent ban.

- **Hardware Requirements:** To effictively use GPU passthrough, you will ideally need a dual GPU setup, an enterprise grade GPU which are not meant for gaming or an integrate GPU if your CPU even supports it. On a single GPU system, using passthrough would render your Linux unusable because it would take away the graphics output.

There are ways to work around some of these limitations but it's not worth a risk especially for serious gamers who value their accounts.

I recommend against using GPU passthrough for gaming on Linux but hey if you decide to try it then you should be cautious and aware of the risks involved.
