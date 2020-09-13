---
title: "web"
layout : category
---

## node.js

{% assign categories_max = 0 %}
{% for category in site.categories %}
  {% if category[1].size > categories_max %}
    {% assign categories_max = category[1].size %}
  {% endif %}
{% endfor %}

{% for i in (1..categories_max) reversed %}
  {% for category in site.categories %}
    {% if category[1].size == i %}
        {% for post in category.last %}
            {% if category[0] == 'node.js' %}
                {% include archive-title.html type=page.entries_layout %}
            {% endif %}
        {% endfor %}
    {% endif %}
  {% endfor %}
{% endfor %}
