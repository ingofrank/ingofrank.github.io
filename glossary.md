---
layout: page
title: Glossary
permalink: /glossary/
---

# Glossary

<ul>
{% for p in site.pages %}
   {% if p.categories contains 'Glossary' %}
      <li><a href="{{ p.url }}">{{ p.title }}</a> (
        {% for tag in p.tags %}
          {{ tag }} 
        {% endfor %}
      )</li>
   {% endif %}
{% endfor %}
</ul>
