---
permalink: /blog
layout: page
title: Blog
subtitle: This is where I tell my friends way too much about myself
---

Here you can find all my blog posts, sorted by date. You will find a list of tags below.

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


## Tags  
Here are the topics I frequently write about:

<ul>
  {% for tag in site.tags %}
    <li><strong>{{ tag[0] }}</strong> ({{ tag[1] | size }} posts)</li>
  {% endfor %}
</ul>
