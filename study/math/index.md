---
layout: single
title: "Math"
permalink: /study/math/
sidebar:
  nav: main
---

## Math Notes

<ul>
  {% assign math_pages = site.pages 
        | where_exp:"p", "p.url contains '/study/math/'" 
        | sort: "url" %}
  {% for p in math_pages %}
    {% if p.url != page.url %}
      <li><a href="{{ p.url | relative_url }}">{{ p.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

