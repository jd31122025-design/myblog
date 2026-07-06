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

<!-- sort posts by tags -->
{% for item in page.tags %}
    <h2>{{ item }}</h2><a name="{{ item | slugify }}"></a>
    <ul style="list-style-type: none">
    {% for post in site.tags[item] %}
        <li>
        <h3>
            <a href="{{ post.url | relative_url }}">
                {{ post.title | escape }}
            </a>
        </h3>
        <span>{{ post.date | date_to_long_string }}</span>
        {{ post.excerpt }}
        {% if post.content contains site.excerpt_separator %}
            <a href="{{ site.baseurl }}{{ post.url }}">Read more</a>
        {% endif %}
        </li>
    {% endfor %}
    </ul>
{% endfor %}


## Search by Post:

<ul>
  {% for post in site.posts %}
    <li>
      <a href=".{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>