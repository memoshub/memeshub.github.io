---
layout: default
title: Категории
permalink: /categories/
list: инвалиды смерть
---
{% assign my_array = "инвалиды, смерть" %}
{% for post in site.posts %}
{% for category in post.categories %}
{% assign my_array = my_array | append: ", " %}
{% assign my_array = my_array | append: category %}
{% endfor %}
{% endfor %}
{% assign my_array = my_array | split ", " %}
{{ my_array | uniq | join: ", " }}
