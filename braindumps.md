---
layout: default
title: Braindumps
---

## Braindumps

<input type="text" id="braindump-search" class="search-input" placeholder="Search braindumps...">

<ul class="braindumps">
  {% for braindump in site.categories.braindumps %}
    <li class="braindump" data-title="{{ braindump.title | downcase }}" data-content="{{ braindump.content | strip_html | downcase }}">
      <a href="/blog{{ braindump.url }}">{{ braindump.title }}</a>
      <time class="publish-date" datetime="{{ braindump.date | date: '%F' }}">
        {{ braindump.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
