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

{% assign date_format = site.date_format | default: "%-d %B %Y" %}

{%- capture site_tags -%}
    {%- for tag in site.tags -%}
        {{- tag | first -}}{%- unless forloop.last -%},{%- endunless -%}
    {%- endfor -%}
{%- endcapture -%}
{%- assign tags_list = site_tags | split:',' | sort -%}

{%- for tag in tags_list -%}
    <a href="#{{- tag -}}" class="btn btn-primary tag-btn"><i class="fas fa-tag" aria-hidden="true"></i>&nbsp;{{- tag -}}&nbsp;({{site.tags[tag].size}})</a>
{%- endfor -%}

## Search by Post:

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>