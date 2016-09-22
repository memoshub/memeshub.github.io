---
layout: post
title: Mem
date: 2016-09-20 14:43:36 +0300
author: svetashov
image: 2016-09-20-16-40.jpg
comment: ору с таких мемесов
categories: kek lol
---

{{ page.comment }}

![memes]({{ site.baseurl }}/memes/{{ page.image }})

{% for tag in page.categories %}
<a href="https://memeshub.github.io/{{ tag }}">
	#{{ tag }}
</a>
{% endfor %}
 <a href='http://vkontakte.ru/share.php?url=https://memeshub.github.io{{ page.url | uri: absolute }}' target='_blank'><img src='/images/vk.png' border='0' width='120' height='30' alt='' title='Поделиться ВКонтакте'></a>
