---
layout: post
title: The Controversy of Telemetry in Open Source Software
updated: 2023-07-24
category: posts
---

With the recent talks of Fedora proposing Telemetry for Workstation 40, I find myself genuinely surprised by how split the discussion is. Maybe it was just my corner of Linux, but I distinctly recall a few years back, the general consensus was that Telemetry equaled bad. It didn't matter if it was anonymized data or if the system was completely open. Especially if it was opt-out or on by default, Telemetry was seen as a negative aspect. However, it seems that things might be slowly starting to change. In this blog post, I want to explore some different perspectives on the topic and share my thoughts.

## The Case for Opt-In Telemetry

Some argue that if you're going to have Telemetry, it should be on by default. Opt-in Telemetry, where users must actively choose to enable it, may not work in practice. It can lead to inaccurate and biased data, often skewed towards more enthusiastic users. For instance, if you have an optional package like Genome Info Collect, only those who specifically install it will be part of the Telemetry data. This can lead to skewed results, as the data will primarily represent the more involved and enthusiast users, not the typical user.

Additionally, opt-in Telemetry might go unnoticed by most users, as it is often obscured in settings or hidden in the background. This can result in a lack of participation from less technical users and not truly represent the entire user base.

## The Case for Opt-Out Telemetry

On the other hand, advocates of opt-out Telemetry argue that it addresses some of the issues associated with opt-in approaches. By including everyone by default, including less technical users, the data can provide a more representative picture of the entire user base. This is crucial for open-source projects aiming to design software for a wide range of users, including those who might not be tech-savvy.

However, a potential drawback of opt-out Telemetry is that users who dislike data collection might feel uncomfortable with their data being collected without express permission. While they can choose to opt-out, some may still feel uneasy about it.

## The Importance of Feedback

Regardless of the approach chosen, it's crucial for open-source projects to actively seek feedback from users. Pop-ups, banners, or other prompts can be effective ways to ask for feedback and engage users. However, it's essential to strike a balance, as overly intrusive or forced prompts might lead to skewed or unhelpful data.

## Conclusion

In the end, Telemetry in open-source software is a topic of ongoing debate. While some developers see it as valuable data to improve their software, others might be concerned about privacy and user consent. Ultimately, it's crucial for projects to find a balance that respects users' choices while still collecting valuable data for improvement.
