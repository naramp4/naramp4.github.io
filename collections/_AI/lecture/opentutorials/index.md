---
title: "머신러닝 야학"
layout : category
sidebar:
        nav: "opentutorials"
---
![](/assets/img/20200822/machinelearning.png){: .align-center}

google과 생활코딩이 함께 하는 머신러닝야학을 참여하면서 강의내용을 요약 정리하고자 한다.

머신러닝 야학은 작심 5일로 짧은 시간에 핵심적인 내용 전달을 해주고 있으며, 머신러닝 및 코딩을 전혀 모르는 분들부터 코딩은 어느정도 알지만 텐서플로우를 경험해보고 싶은 분들까지 여러 층을 대상으로 강의를 무료로 제공을 해주고 있다.

해당 블로그에서는 텐서플로우를 통해 머신러닝을 경험해 보는 과정을 5일동안 정리해보고자 한다.



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
            {% if category[0] == 'opentutorials' %}
                {% include archive-title.html type=page.entries_layout %}
            {% endif %}
        {% endfor %}
    {% endif %}
  {% endfor %}
{% endfor %}