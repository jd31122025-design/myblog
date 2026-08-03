---
layout: page
title: Book Reviews
---
 
{% for post in site.categories.book-reviews %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
