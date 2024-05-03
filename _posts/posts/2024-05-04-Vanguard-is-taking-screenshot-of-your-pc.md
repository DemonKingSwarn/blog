---
layout: post
title: Vanguard Is Taking Screenshot of Your PC!
updated: 2024-05-04
category: posts
---

Hey everyone,

There's been some buzz lately about Vanguard, the anti-cheat software for Valorant (and soon to be for League of Legends aswell), and its alleged screenshot taking capabilities. Today, we're diving deep into this topic to understand what's happening and what it means for you.

**The Short Story:**

- Vanguard can capture screenshots of your entire PC screen, including overlays like Discord chats.

- These screenshots may be uploaded to their servers, potentially ending up in locations outside your region (e.g. EU data on US servers).

**The Technical Breakdown (for the curious):**

A Researcher (**@0xCODEBABE**) discovered a module within Vanguard that takes screenshots based on instructions from their servers. Here's the gist:

- If Vanguard finds nothing suspicious (no "window_title = VALORANT" parameter), it captures your entire screen.

- Otherwise, it focuses on the game window itself.

- The captured image format (JPG, quality), and capture area (window or full screen) are all determined by Vanguard's servers.

**Important Points:**

- This screenshotting happens per game session.

- While some games take screenshots, they're usually engine-related and can't capture overlayes.

- The researcher offers to collaborate on video proof of this module's existence.

**Addressing Concerns:**

- Yes, Vanguard's full-screen screenshotting is intrusive.

- The researcher was screenshotted even with an unranked, low-level account.

**Transparency and Privacy:**

This discovery raises questions about transparency and user privacy. While anti-cheat measures are crucial for fair gameplay, the extent of data collection needs to be clear and user-consented.

**What's Next?**

I'll be keeping an eye on developments and share any official responses from Vanguard or Riot Games.

**Stay Informed!**

This is a complex issue, and discussions are ongoing. I encourage you to do your own research and stay informed.

**Credits:**

A huge thank you to @0xCODEBABE for their initial discovery!

**Screenshots From the Code of the Revelation Post:**

![](https://i.imgur.com/u13lcWQ.png)

![](https://i.imgur.com/JWy6nHo.png)

![](https://i.imgur.com/9CujErO.png)
