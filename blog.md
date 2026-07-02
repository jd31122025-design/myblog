---
permalink: /blog
layout: page
title: Blog
subtitle: My thoughts, ramblings, experiment findings and more.
---

Here you can find all my blog posts, sorted by date with the newest at the top. You will find a list of tags at the bottom of the page if you're interested.

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
