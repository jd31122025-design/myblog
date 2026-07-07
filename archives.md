---
layout: page
title: 'Archives'
subtitle: A list of all posts and tags used on this site.
---
The headings on this page include:
* TOC
{:toc}

Sometimes it is fun to go back and read old posts. If you enjoy doing that, then this page is for you. 
It lists all the tags used on this site, and under each tag, it lists all the posts that have that tag. 
You can click on any post title to read that post.

## Search by Tag:

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
      <a href=".{{ ./blog/post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>