---
layout: page
title: Author Interviews
---
<div id="archives">
  {% for category in site.categories %}
    <div class="archive-group">
      {% capture category_name %}{{ category | first }}{% endcapture %}
      <h3 class="category-head">{{ Author Interviews }}</h3>
      {% for post in site.categories[Author Interviews] %}
        <article class="archive-item">
          <h4><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h4>
        </article>
      {% endfor %}
    </div>
  {% endfor %}
</div>
