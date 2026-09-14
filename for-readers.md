---
permalink: /for-readers
layout: page
title: For Readers
subtitle: Book Reviews and Author Interviews
---

The headings on this page include:
* TOC
{:toc}

## Author Interviews

<ul>
  {% assign posts = site.categories.author-interview %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>({{ post.date | date: "%Y-%m-%d" }})</span>
    </li>
  {% endfor %}
</ul>

## Book Reviews

<ul>
  {% assign posts = site.categories.book-review %}
  {% for post in posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span>({{ post.date | date: "%Y-%m-%d" }})</span>
    </li>
  {% endfor %}
</ul>

## My Book Review Policy


