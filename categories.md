---
layout: default
title: Категории
permalink: /categories/
---
{% assign list_categories = инвалиды %}
{% for post in site.posts %}
{% for category in post.categories %}
{% for i in list_categories %}
 {% assign founded = 0 %}
	{% if category == i%}
	{% assign founded = 1 %}
	{% endif %}
	{% if founded != 1 %}
	{% assign list_categories = list_categories | append: category %}
	{% assign list_categories = list_categories | append: " " %}
	{% endif %}

{% endfor %}
{% endfor %}
{% endfor %}
{{list_categories}}