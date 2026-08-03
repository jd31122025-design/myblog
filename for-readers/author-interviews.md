---
layout: page
title: Author Interviews
---
<div class="posts">
  {% for post in site.categories.author-interviews %}
  <article class="post">
      <h1 class="post-title">
        <a href="{{ post.url | relative_url }}">
          {{ post.title }}
        </a>
      </h1>
      {{ post.content | markdownify | strip_html | truncatewords: 30 }}
    </article>
  {% endfor %}
</div>
