---
layout: page
title: 'Archives'
subtitle: A list of all posts and tags used on this site.
---

Sometimes it is fun to go back and read old posts. If you enjoy doing that, then this page is for you. 
It lists all the tags used on this site, and under each tag, it lists all the posts that have that tag. 
You can click on any post title to read that post.

The headings on this page include:
* TOC
{:toc}

## Search by Tags:

<h1>Tags</h1>
<ul>
  {% assign tags_list = site.tags | sort %}
  {% for tag in tags_list %}
    <li>
      <a href="/tag/{{ tag[0] | slugify }}/">
        {{ tag[0] }} ({{ tag[1].size }})
      </a>
    </li>
  {% endfor %}
</ul>

## Search by Post:

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>