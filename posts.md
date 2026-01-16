---
layout: default
title: Posts
---

## Posts

<input type="text" id="post-search" class="search-input" placeholder="Search posts...">

<ul class="posts">
  {% for post in site.categories.posts %}
    <li class="post" data-title="{{ post.title | downcase }}" data-content="{{ post.content | strip_html | downcase }}">
      <a href="/blog{{ post.url }}">{{ post.title }}</a>
      <time class="publish-date" datetime="{{ post.date | date: '%F' }}">
        {{ post.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
