---
layout: single
title: "Poetry"
permalink: /poems/
---

{% assign poems = site.poems | sort: "date" | reverse %}

<ul class="poem-list">
{% for p in poems %}
  <li>
    <a href="{{ p.url }}">{{ p.title }}</a>
    {% if p.poem_meta %}<span class="muted"> — {{ p.poem_meta }}</span>{% endif %}
  </li>
{% endfor %}
</ul>
