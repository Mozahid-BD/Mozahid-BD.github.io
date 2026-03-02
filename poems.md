---
layout: single
title: "Poetry"
permalink: /poems/
---

{% assign poems = site.poems | default: empty %}

{% if poems == empty %}
No poems published yet.
{% else %}
{% assign poems_sorted = poems | sort: "date" | reverse %}
<ul class="poem-list">
{% for p in poems_sorted %}
  <li>
    <a href="{{ p.url }}">{{ p.title }}</a>
  </li>
{% endfor %}
</ul>
{% endif %}
