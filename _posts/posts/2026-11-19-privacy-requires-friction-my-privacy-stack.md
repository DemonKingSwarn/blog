---
layout: post
title: Privacy Requires Friction
updated: 2026-11-19
excerpt: "In this blog, I talked about what my privacy stack is and a lot more."
keywords: [proton, helium browser, tuta, aegis, kagi, searxng, grapheneos, linux]
category: posts
---

Hey everyone,

Today I am just gonna talk about why having a private alternative to most of the **Big Tech** stuff is important. In the long run, it will save you a lot of frustrations and sudden losing access to your important stuffs. 

## Email

Everyone these days just defaults to GMail for their email, or SSO. But you know, using this provider for a SSO is not a good thing, for example, recently a manga artist’s GMail was suspended and it lead to every work he had on his Google Drive get lost forever. 

I started having separate emails for separate stuff, and in Proton Mail instead of GMail. 

I used to use plus (+) addressing before this, it was good but now i just use a throwaway email which i wont even open while signing up to some random service which needs email and doesn’t work with temp mail. 

Here are my picks:

1. ProtonMail
2. Tuta
3. Self hosted email (only if you want to dive deeper into the privacy rabbit hole)

## Security

Never use Google or Apple’s password manager / 2FA to keep your passwords. 

The above-mentioned consequence applies here too.

**Password Managers**

Use a good third-party password manager. I personally use Proton Pass. 

Password Managers do make your life a lot easier. 

I am currently looking to self-host my Password Manager, for which I will go with KeePassXC. 

Password Managers are way more secure than you, the average Joe. Unlike you, who might use DOB, or their pet’s name for the password, they use randomised ones. Don’t sleep on them because they are inconvenient. 

**2FA**

Don’t use Google Authenticator, app is good but if you lose your Google account, then you lose every login.

The platforms which ask you to use Google Authenticator will also work with the alternatives. 

I have used these ones personally:

1. Proton Authenticator - I currently use this, I switched to it because currently I can’t find a good auth tool for iPhone. 
2. Aegis - A great offline 2FA app, only works for Android. So I had to switch from it when I got an iPhone. 

You can use any one you want, they are really easily switchable. 

## Browsers

Most people either use Chrome or Brave, but think about it, that’s probably where your life lives most of the time when you are on your computer. 

Contrary to popular belief, Brave isn’t as private as they sell it. And it also comes with a ton of crap, and even worse performance than Chrome. 

Here are my top picks for browsers:

1. Helium - It has the best ad blocker, and anti-tracking features. Also has a lot of QoL features and a good UI. A great Chrome replacement too. 
2. Firefox for personal use and also DRM content. 

For phone:

On Android I would recommend removing Chrome (using ADB) with Firefox. It supports extensions on mobile too. 

On iPhone, Orion browser by Kagi is really great and it also supports both Chrome and Firefox extensions. 

Safari is also a decent private browser for iPhone, only if you use private relay. 

Also note, Helium is working on the Android and iOS support and it may be available soon for mobile. 

## Notes

Believe it or not, a lot of note-taking apps do tend to use your data for learning about you. 

I recommend these ones:

1. Obsidian is really great, it is proprietary but it is fully offline and has a lot of cool features for note writing. Ever since I started using it, I have been getting a lot more urge to write stories, notes, or even blogs like this one. It is also available on mobile. 
2. Logseq, the FOSS replacement for Obsidian. Everything which is true for Obsidian is true for this too. 
3. Joplin is also a great alternative, and it’s also open-source.

All the above-mentioned note-taking apps use markdown for note-taking. 

## Search Engine

This by far is the most data-harvesting platform, don’t use Google blindly just because it’s the default search engine on most browsers. 

Here are my picks:

1. SearXNG, it is selfhostable which I used to use before moving to another search engine. You can also use one of its public instances. Honestly, it is only private if multiple people use your SearXNG instance, if only you use it then it is pretty easy to still profile you. 
2. Ecosia is private and also a non-profit organisation which plants a tree for every time you use it to searching something. I currently use it.
3. Kagi is a really good private search engine. It has both paid and free tiers. The free tier offers 100 searches per day which might be enough for you, but you can always get the paid tier, which will also support the devs. 

## DNS and VPN

For DNS, I would recommend you to use Cloudflare’s 1.1.1.1. Most of the world runs on Cloudflare anyway, and it will also make you access the web much faster with being private. 

ProtonVPN is a really good VPN service, for both paid and free VPNs. 

Other than that, you can also host pihole, either on a raspberry pi or use a docker/podman container to block ads network wide. 


## Messaging

This is one of the most crucial parts of our every day lives, and most of us use one provided by big tech. 

In India specifically, everyone uses WhatsApp, or Telegram for messaging. And most of the times it is private, but recently they have started targeting you with their specific ads and also added a premium plan for everyone. And they will also sell your data to either government or any highest bidder in a nutshell, either it’s your number, your profile picture, or how long you spend on their apps. 

Here are my recommendations to get back your conversations from them:

1. Signal is by far the best private messaging service out there. Has every feature you want from WhatsApp but better. 
2. BitChat, it is a decentralised communication platform. It uses Bluetooth to communicate, but can also use the internet for people farther away from you. 
3. Matrix, another great encrypted messaging service, which is a lot like Discord but you can also self host it if you don’t want to use their instance. It is also federated so any instance can talk to anyone.

I currently use Signal and my own selfhosted instance of Matrix. And it is by far the great experience these days. 

I know it’s not easy moving away from the messaging apps, but I have started setting up bridges for the messaging apps where I wasn’t able to convince others to message me there. 
I mostly did this with my family, that I would only reply in Signal so message me there. 

## Operating Systems

Computers play a large role in our lives these days, and some of the operating systems are responsible for spying on us. So replacing them is a lot more sensible approach. 

For desktops, here are my picks in the most private to least private order. 

1. Linux, any Linux-based operating system is good to go for privacy and also security. 
2. MacOS, it is honestly a great private and secure choice. But it’s mostly linked with MacBooks. 

For mobile, here are my picks in the most secure to least secure order. 

1. GrapheneOS, it is by far the most secure mobile operating system. It is also compatible with Android, so any app which works on Android works here. Though it is mostly available for Pixels and Motorola devices. 
2. iOS, it is also one of the most private mobile operating systems right now, but is only available for iPhones. 

## Photo Backup

Just like you all, I used to use Google Photos. But I switched away from it 5 years ago.
Storing all your photos and videos in their services means you can lose access to them if you lose the email, like I mentioned how that manga artist lost everything. And these days Google has started training Gemini on the stuffs you upload to Google Photos and Drive. 

On Android, I removed the Google Photos app and replaced it with Fossify Gallery, so it doesn’t auto sync my photos and videos to Google Photos, plus Fossify Gallery is offline first. 

But then I started self-hosting Nextcloud, and moved to using Nextcloud Photos. 

And now I use my selfhosted Immich, which is a lot more like Google/Apple Photos. 

But you can also use Ente Photos, it is amazing and also has the facial recognition feature which works locally on your device. 

## Conclusion

Your privacy is in your hand, if you ignore it for the sake of convenience then you are giving access to whoever wants to control your personal life. 

All of this softwares is culminated from my personal experience, and were not made in a single day. It took a lot of days to fully make everything way more private than it used to be back then. 

Anyway, that’s all for today’s blog. I hope you all enjoyed reading it, and I will see you guys in the next one. 
