---
layout: page
title: For Writers
---

## Writing, Editing & Publishing

<ul>
{% assign posts = site.categories.writing %}
{% for post in posts %}
  <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
