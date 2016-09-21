---
layout: default
title: Категории
permalink: /categories/
---
{% assign my_array = "инвалиды, смерть, kek, lol" %}
{% for post in site.posts %}
{% for category in post.categories %}
{% assign my_array = my_array | append: ", " %}
{% assign my_array = my_array | append: category %}
{% endfor %}
{% endfor %}
{% assign my_array = my_array | split: ", " %}
{% assign my_array = my_array | uniq %} 
{% assign my_array = my_array | sort %}
{{ my_array | join: ", " }}
<div class="tags-list">
{% for tag in my_array %}
<a href="/{{ tag }}">
<p>#{{ tag }}</p>
</a>
{% endfor %}
</div>