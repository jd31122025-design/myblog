---
layout: page
title: Book Reviews
---
<div class="posts">
  {% for post in site.categories.book-reviews %}
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
