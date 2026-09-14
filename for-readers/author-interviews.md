---
title: Author Interviews
---
<ul>
  {% assign posts = site.categories.author-interview %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>({{ post.date | date: "%Y-%m-%d" }})</span>
    </li>
  {% endfor %}
</ul>
