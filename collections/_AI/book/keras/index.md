---
title: "케라스 창시자에게 배우는 딥러닝"
layout : category
sidebar:
        nav: "keras"
---
![](/assets/img/20190228/keras.png){: .align-center style="max-width:300px"}

케라스 창시자에게 배우는 딥러닝을 공부의 목적으로 요약 정리하여 보관하고자 한다.

순차적으로 정리하여 포스팅하도록 하겠다.

소스코드 같은 것은 역자의 [github](https://github.com/rickiepark/deep-learning-with-python-notebooks){:target='_blank'}에 잘 요약정리 되어 있기 참고하기 바란다.


<!-- {% assign categories_max = 0 %}
{% for category in site.categories %}
  {% if category[1].size > categories_max %}
    {% assign categories_max = category[1].size %}
  {% endif %}
{% endfor %}

{% for i in (1..categories_max) reversed %}
  {% for category in site.categories %}
    {% if category[1].size == i %}
        {% for post in category.last %}
            {% if category[0] == 'keras-book' %}
                {% include archive-title.html type=page.entries_layout %}
            {% endif %}
        {% endfor %}
    {% endif %}
  {% endfor %}
{% endfor %} -->