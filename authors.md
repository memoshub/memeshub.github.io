---
layout: default
title: Авторы
permalink: /authors/
---

{% assign my_array = "svetashov" %}
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


{% for author in my_array %}
<a href="/{{ author }}.md">
<div class="author">
	<div class="author-photo"><img src="/images/author-{{ author }}.png"></div> 
</div>
</a>
{% endfor %}