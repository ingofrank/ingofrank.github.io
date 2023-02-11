---
layout: page
title: Glossary
permalink: /glossary/
---

# Glossary

<ul>
{% for p in site.pages %}
   {% if p.categories contains 'Glossary' %}
      <li><a href="{{ p.url }}">{{ p.title }}</a></li>
   {% endif %}
{% endfor %}
</ul>


<ul>
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
</ul>
