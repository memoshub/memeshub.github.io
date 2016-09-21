---
layout: default
title: Категории
permalink: /categories/
list: инвалиды смерть
---

{% for post in site.posts %}
{% for category in post.categories %}
{% for i in page.list %}
 {% assign founded = 0 %}
	{% if category == i%}
	{% assign founded = 1 %}
	{% endif %}
	{% if founded != 1 %}
	{% assign page.list = page.list | append: category %}
	{% assign page.list = page.list | append: " " %}
	{% endif %}

{% endfor %}
{% endfor %}
{% endfor %}
{{ page.list }}
hh