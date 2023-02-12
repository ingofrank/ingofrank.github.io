---
layout: page
title: Ontologie-Entwurfsmuster
permalink: /odp/
---

## Ontologie-Entwurfsmuster

<ul>
{% for p in site.pages %}
   {% if p.categories contains 'ODP' %}
      <li><a href="{{ p.url }}">{{ p.title }}</a></li>
   {% endif %}
{% endfor %}
</ul>
