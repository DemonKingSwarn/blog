---
layout: post
title: My Blogging System
updated: 2024-04-19
category: posts
---

*A tour of what makes my blog totally awesome*

I've been actively blogging for almost a year now, releasing over 18 posts in the process. Along the way I optimised a bunch of parts of my publishing process and website.

## Hosting

Site hosting is done via github pages. That way I don't have to administrate linux servers in my free time as well. Also no expiring certificates like on every old blog I see nowadays.

I got my domain from [is-a.dev](https://is-a.dev) which is a really cool subdomain. It doesn't really matter what domain you use or from where you get it from.

## Post Categories

I sort my posts by categories. Tags dont really make sense until you reach triple digits of posts. On my landing page you can filter through those categories with those convenient buttons at the top.

## Asset Management

I tend to convert any image I use in posts to webp.
You can do this via imagemagick on most linux systems: `convert <input> asset.webp`

## Quality Assurance

To combat bit rot of my posts, I use a [dead link checker](https://github.com/hahwul/deadfinder) via github actions. It's pretty slow.

## Misc

I disallow the GPTBot in my [robots.txt](https://github.com/DemonKingSwarn/blog/blob/master/robots.txt), and recommend you do the same.

This website doesn't have an about page, which is fine since I don't currently syndicate my posts on hacker news, lobste.rs or, god forbid, reddit. I might add one in the future, or I might not.

I hopt this post is helpful to some of you.
Being an internet [landlord](https://www.youtube.com/watch?v=SynQFoNMcQU) is fun, you should try it!
