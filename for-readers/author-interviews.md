---
title: Author Interviews
---
{% for author_interviews in site.author_interviews %}
  <h2>{{ author_interviews.name }}</h2>
  <p>{{ author_interviews.content | markdownify }}</p>
{% endfor %}
