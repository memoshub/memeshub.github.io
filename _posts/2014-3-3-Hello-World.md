---
layout: post
title: Mem
date: 2016-09-20 14:43:36 +0300
author: svetashov
image: 2016-09-20-16-40.jpg
comment: ору с таких мемесов
categories: кек лол религия ору
---

{{ page.comment }}

![memes]({{ site.baseurl }}/memes/{{ page.image }})

{% for tag in page.categories %}
    		<a href="/tag.md/?tag={{ tag }}">#{{ tag }}</a>
{% endfor %}

