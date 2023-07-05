---
layout: post
title: YouTube's New Policy- AdBlocker Users Blocked Out, a Simple Solution Emerges
updated: 2023-07-05
category: posts
---

YouTube, the world's largest video-sharing platform, recently implemented a controversial policy that restricts users from accessing its content after watching only three videos if they have an adblocker enabled. This decision has sparked a heated debate among users who rely on adblockers to enhance their online browsing experience. However, a solution has emerged to counter YouTube's adblocker blocker, providing a workaround for users who prefer an ad-free viewing experience.

YouTube's new policy has left many adblocker users frustrated and inconvenienced. For years, adblockers have offered a way to avoid intrusive and irrelevant advertisements, enabling a smoother and more enjoyable browsing experience. However, the platform's recent implementation aims to counter these adblockers, effectively blocking users from accessing content after a mere three videos.

Fortunately, an ingenious solution has emerged for users seeking to circumvent YouTube's adblocker blocker. By adding a few lines of code to the popular adblocking extension, uBlock Origin, users can regain control over their ad experience on YouTube.

```js
youtube.com##+js(set, yt.config_.openPopupConfig.supportedPopups.adBlockMessageViewModel, false)
youtube.com##+js(set, Object.prototype.adBlocksFound, 0)
youtube.com##+js(set, ytplayer.config.args.raw_player_response.adPlacements, [])
youtube.com##+js(set, Object.prototype.hasAllowedInstreamAd, true)
```

The provided lines of code, when added to uBlock Origin's "My Filters" section, effectively disable YouTube's adblocker detection. These lines ensure that the platform's adBlockMessageViewModel, adBlocksFound counter, adPlacements, and hasAllowedInstreamAd settings are all modified, allowing users to watch videos uninterrupted by intrusive advertisements.

This simple solution empowers users to enjoy an ad-free experience while continuing to access the vast array of content available on YouTube. It presents a way to strike a balance between the platform's monetization needs and users' desire for a less cluttered viewing experience.

YouTube's new policy targeting users with adblockers has triggered a wave of frustration and discontent. However, the emergence of a simple solution offers a glimmer of hope for those seeking an ad-free viewing experience. By adding a few lines of code to uBlock Origin, users can bypass YouTube's adblocker blocker and regain control over their browsing experience. As the debate between content creators and adblocker users continues, this solution serves as a reminder of the evolving nature of the internet and the ongoing struggle for a harmonious balance between user preferences and platform monetization.
