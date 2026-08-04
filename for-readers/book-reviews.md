---
title: Book Reviews
---
{% for book_reviews in site.book_reviews %}
  <h2>
    <a href="{{ book_reviews.url }}">
      {{ book_reviews.title }}
    </a>
  </h2>
  <h4>{{ sbook_reviews.rating }}</h4>
  <p>{{ book_reviews.content | markdownify }}</p>
{% endfor %}
