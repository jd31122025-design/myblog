{% raw %}
---
layout: page
title: "Post Archive by Tag"
permalink: /tags/
---
<h1>All Tags</h1>

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  {% assign tag_name = tag | first %}
  <h2 id="{{ tag_name | slugify }}">{{ tag_name }}</h2>
  <ul class="post-list">
    {% for post in site.tags[tag_name] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
{% endraw %}