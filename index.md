---
layout: default
title: Home
---

Swarn's personal blog, featuring a grab bag of stories, computers, photos, mind, and all the other thoughts that won't let me go.

A weblog means a personal blog rather than a corporate one. It's a retro word for a retro person.

[rss](/blog/feed.xml)

## Recent posts

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

[See all posts](/blog/posts)
