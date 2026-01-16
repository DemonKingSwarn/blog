---
layout: default
title: Braindumps
---

## Braindumps

<ul class="braindumps">
  {% for braindump in site.categories.braindumps %}
    <li class="braindump">
      <a href="/blog{{ braindump.url }}">{{ braindump.title }}</a>
      <time class="publish-date" datetime="{{ braindump.date | date: '%F' }}">
        {{ braindump.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>
