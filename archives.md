---
layout: page
title: Archives
---

<h1>Categories</h1>
<ul>
  {% for category in site.categories %}
    <li>
      <h2>{{ category[0] }}</h2>
      <ul>
        {% for post in category[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span>({{ post.date | date: "%Y-%m-%d" }})</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>

<hr>

<h1>Tags</h1>
<ul>
  {% for tag in site.tags %}
    <li>
      <h2>{{ tag[0] }}</h2>
      <ul>
        {% for post in tag[1] %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span>({{ post.date | date: "%Y-%m-%d" }})</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
