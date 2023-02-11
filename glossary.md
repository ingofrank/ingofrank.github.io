---
layout: page
title: Glossary
permalink: /glossary/
---

# Glossary

<ul>
{% for p in site.pages %}
   {% if p.category contains 'Glossary' %}
      <li><a href="{{ p.url }}">{{ p.title }}</a></li>
   {% endif %}
{% endfor %}
</ul>
