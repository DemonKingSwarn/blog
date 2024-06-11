---
layout: default
title: Home
---

Swarn's personal blog, featuring a grab bag of stories, computers, photos, mind, and all the other thoughts that won't let me go.

A weblog means a personal blog rather than a corporate one. It's a retro word for a retro person.

[![EMAIL](https://port19.xyz/buttons/email.gif)](mailto:swarnaditya.isometric@gmail.com)  [![RSS](https://github.com/DemonKingSwarn/blog/raw/master/assets/static/rss.gif)](/blog/feed.xml)

## Recent blogs

<ul class="posts">
  {% for post in site.categories.posts limit:6 %}
    <li class="post">
      <a href="/blog{{ post.url }}">{{ post.title }}</a>
      <time class="publish-date" datetime="{{ post.date | date: '%F' }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>

[See all blogs](/blog/posts)

## Recent braindumps

<ul class="braindumps">
  {% for braindump in site.categories.braindumps limit:6 %}
    <li class="braindump">
      <a href="/blog{{ braindump.url }}">{{ braindump.title }}</a>
      <time class="publish-date" datetime="{{ braindump.date | date: '%F' }}">
        {{ braindump.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>

[See all braindumps](/blog/braindumps)

## linkback?

I think your site is cool - do you think my site is cool too?

of course you do! feel free to use this button to link back to my website.

<img src="https://demonkingswarn.live/assets/media/buttons/web-button.svg" height="31px" width="88px"> <i>swarn now!</i>

```html
<a href="https://demonkingswarn.is-a.dev/blog"><img src="https://demonkingswarn.live/assets/media/buttons/web-button.svg" height="31px" width="88px" alt="swarn now!"></a>
```
