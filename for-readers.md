---
permalink: /for-readers
layout: page
title: For Readers
subtitle: Book Reviews and Author Interviews
---

* TOC
{:toc}

## Author Interviews

<ul>
  {% assign posts = site.categories.author-interview %}
  {% if posts %}
    {% for post in posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span>({{ post.date | date: "%Y-%m-%d" }})</span>
      </li>
    {% endfor %}
  {% else %}
    <li>No author interviews have been posted yet.</li>
  {% endif %}
</ul>

## Book Reviews

<ul>
  {% assign posts = site.categories.book-review %}
  {% if posts %}
    {% for post in posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span>({{ post.date | date: "%Y-%m-%d" }})</span>
      </li>
    {% endfor %}
  {% else %}
    <li>No book reviews have been posted yet.</li>
  {% endif %}
</ul>

## Book Review Policy

<p>
  The Book Review Policy page is coming soon.  
  When ready, it will appear here:
  <a href="/book-review-policy">Book Review Policy</a>
</p>
