---
layout: author
aname: svetashov
permalink: /svetashov/
stat: Основатель сайта MemesHub, величайший мемолог и критик мемесов
vk: artyomsvetashov
---
{% assign my_array = "" %}
{% for post in site.posts %}
{% if post.author == page.aname %}
{% assign my_array = my_array | append: ", " %}
{% assign my_array = my_array | append: post %}
{% endif %}
{% endfor %}
{% assign my_array = my_array | split: ", " %}
{{ my_array }}