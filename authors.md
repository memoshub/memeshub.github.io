---
layout: default
title: Авторы
permalink: /authors/
---

{% assign my_array = "" %}
{% for post in site.posts %}
{% for a in post.author %}
{% assign my_array = my_array | append: ", " %}
{% assign my_array = my_array | append: a %}
{% endfor %}
{% endfor %}
{% assign my_array = my_array | split: ", " %}
{% assign my_array = my_array | uniq %} 
{% assign my_array = my_array | sort %}
{{ my_array | join: ", " }}