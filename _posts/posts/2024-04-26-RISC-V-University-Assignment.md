---
layout: post
title: Building my own RISC-V CPU
updated: 2024-04-26
category: posts
---

Hey everyone,

just wanted to share a quick update on my RISC-V CPU project for uni. It's been a wide ride so far, but things are actually coming together much smoother than I anticipated.

For those who aren't familiar, RISC-V is a super cool open-source instruction set architecture (ISA) that's gaining a lot of traction. I'm basically building a "tiny little" processor (you will see how tiny it is xD) that can understand and execute RISC-V instructions.

The big news is that I've already gotten a bunch of the core functionality working! This includes things like:

- **Non-shifted ALU instructions**: Add, subtract, all that good stuff. No fancy bit-shifting yet, but baby steps!
- **Store instructions**: Saving data to memory like a champ.
- **Jumps and branches**: The CPU can now jump around in its program based on certain conditions.

And the most amazing part? These parts are all reasonably stable! I've been running the CPU simulator for like, minutes at a time at 10khz (which is way faster than I thought possible at this stage), and haven't seen any weird compute errors.

Don't get me wrong, there's still a ton to do. I need to tackle shifted instructions, handle loads from memory, implement control flow stuff like loops, and probably a bunch of other things I haven't even thought of yet. But hey, at least I'm not starting from scratch anymore!

I'll definitely keep you guys posted on my progress. Hopefully next time I write, I'll have some even more exciting things to share. In the meantime, feel free to leave any comments or questions below!

**P.S.** If you're interested in learning more about RISC-V, there are some great resources out there. I'll try to compile a list and share it in the next post!
