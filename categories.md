---
layout: default
title: Категории
permalink: /categories/
---

{% for category in site.tags %}
<p>#{{ category.tag }}</p>
{% endfor %}