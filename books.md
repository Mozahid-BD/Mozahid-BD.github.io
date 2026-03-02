---
layout: single
title: "Books & Series"
permalink: /books/
---

{% assign series_list = site.data.books.series %}
{% assign books_list = site.data.books.books %}

{% for s in series_list %}
## {{ s.title_bn }} {% if s.title_en %}({{ s.title_en }}){% endif %}

{{ s.description }}

{% assign sbooks = books_list | where: "series_id", s.id %}
<ul>
{% for b in sbooks %}
  <li>
    <a href="/books/{{ b.slug }}/">
      {{ b.book_title_bn | default: b.book_title_en }}
    </a>
  </li>
{% endfor %}
</ul>

{% endfor %}
