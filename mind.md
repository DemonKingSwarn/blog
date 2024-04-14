---
layout: default
title: Braindumps
---

## Braindumps

<ul class="mind">
  {% for mind in site.categories.braindumps %}
    <li class="mind">
      <a href="/blog{{ mind.url }}">{{ mind.title }}</a>
      <time class="publish-date" datetime="{{ mind.date | date: '%F' }}">
        {{ mind.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
