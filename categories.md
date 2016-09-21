---
layout: default
title: Категории
permalink: /categories/
list: инвалиды смерть
---
{% assign my_array = "инвалиды, смерть" %}
{% for post in site.posts %}
{% for category in post.categories %}
{% assign founded = 0 %}
{% for i in my_array %}
	{% if category == i %}
		{% assign founded = 1 %}
		{{ founded }}
	{% endif %}
{% endfor %}
{% if founded == 0 %}
	{% assign my_array = my_array | append: ", " %}
	{% assign my_array = my_array | append: category %}
{% endif %}
{% endfor %}
{% endfor %}
{{ my_array }}
