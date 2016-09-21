---
layout: default
title: Категории
permalink: /categories/
list: инвалиды смерть kek lol
---
{% assign my_array = "инвалиды, смерть, kek, lol" %}
{% for post in site.posts %}
{% for category in post.categories %}
{% assign my_array = my_array | append: ", " %}
{% assign my_array = my_array | append: category %}
{% endfor %}
{% endfor %}
{{ my_array }} 

