---
layout: single
title: "মৃত্যু গহ্বরে তাং ঈ — Chapters"
permalink: /read/usm-book-1/
---

{% assign chapters = site.chapters | where: "book_id", "usm-book-1" | sort: "chapter_no" %}

{% if chapters == empty %}
No chapters published yet.
{% else %}
<ol>
{% for ch in chapters %}
  <li><a href="{{ ch.url }}">{{ ch.chapter_no }}. {{ ch.chapter_title }}</a></li>
{% endfor %}
</ol>
{% endif %}
