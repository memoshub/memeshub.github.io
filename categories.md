---
layout: default
title: Категории
permalink: /categories/
list: инвалиды смерть
---
{% assign my_array = "инвалиды, смерть" %}
{% for post in site.posts %}
{% for category in post.categories %}
{% for i in my_array %}
 {% assign founded = 0 %}
	{% if category == i%}
	{% assign founded = 1 %}
	{% endif %}
	{% if founded != 1 %}
	{% assign my_array = my_array | append: ", " %}
	{% assign my_array = my_array | append: category %}
	{% endif %}

{% endfor %}
{% endfor %}
{% endfor %}
{{ my_array }}
hh