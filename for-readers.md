---
permalink: /for-readers
layout: page
title: For Readers
subtitle: Book Reviews and Author Interviews
---

* [Author Interviews](./for-readers/author-interviews.md)
* [Book Reviews](./for-readers/book-reviews.md)
* Book Review Policy

<h1>Author Interviews</h1>

<ul>
  {% assign posts = site.categories.author-interviews %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>({{ post.date | date: "%Y-%m-%d" }})</span>
    </li>
  {% endfor %}
</ul>

