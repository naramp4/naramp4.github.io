---
title: "programming"
layout : category
sidebar:
        nav: "programming"
---


{% assign categories_max = 0 %}
{% for category in site.categories %}
  {% if category[1].size > categories_max %}
    {% assign categories_max = category[1].size %}
  {% endif %}
{% endfor %}

## python

{% for i in (1..categories_max) reversed %}
  {% for category in site.categories %}
    {% if category[1].size == i %}
        {% for post in category.last %}
            {% if category[0] == 'python' %}
                {% include archive-title.html type=page.entries_layout %}
            {% endif %}
        {% endfor %}
    {% endif %}
  {% endfor %}
{% endfor %}
