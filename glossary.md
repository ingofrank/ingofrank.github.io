---
layout: page
title: Glossary
permalink: /glossary/
categories: [Glossary]
---

# Glossary

- [Entry 1](/glossary/entry1/)
- [Entry 2](/glossary/entry2/)

<ul>
{% for cat in site.category-list %}
    <li>
    {{ cat }}
        <ul>
    {% for order in (1..10) %}
    {% for page in site.pages %}
     {% if page.order == order %}   
        {% if page.resource == true %}
            {% for pc in page.categories %}
                {% if pc == cat %}
                <li><a href="{{ page.url }}">{{ page.title }}</a></li>
                {% endif %}
            {% endfor %}
        {% endif %}
      {% endif %}
    {% endfor %} <!-- page -->

  {% endfor %}
    </ul>
    </li>
{% endfor %}  <!-- cat -->
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

{% for p in site.pages %}
   {% if p.categories contains 'Glossary' %}
      <li><a href="{{ p.url }}">{{ p.title }}</a></li>
   {% endif %}
{% endfor %}
</ul>
  
