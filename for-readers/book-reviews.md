---
title: Book Reviews
---
{% for book_reviews in site.book_reviews %}
  <h2>{{ book_reviews.title }}</h2>
  <h4>{{ book_reviews.rating }}</h4>
  <p>{{ book_reviews.content | markdownify }}</p>
{% endfor %}
