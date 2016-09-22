---
layout: author
aname: svetashov
permalink: /svetashov/
stat: Основатель сайта MemesHub, величайший мемолог и критик мемесов
vk: artyomsvetashov
---
<div class="posts">
{% for post in site.posts %}
{% if post.author == page.aname %}
<article class="post">
<div class="author-line">
    <a href="/{{ post.author }}">
        <img src="/images/author-{{ post.author }}.png" class="author-img"> 
        <div class="author-name">
            <h1>{{ post.author }}</h1>
        </div>
    </a>
    <div class="datetime">
        <p>{% include short_date.html date=post.date %}</p>
    </div>
</div>
{% if post.comment %}
<div class="author-comment">
    {{ post.comment }}
</div>
{% endif %}
<div class="mem">
    <a rel="simplebox" href="{{ post.url }}">
    <img src="{{ post.image }}"></a>
</div>
<div class="tags">
    {% for tag in post.categories %}
    <a href="/{{ tag }}">#{{ tag }}</a>
    {% endfor %}
    {% endif %}
    {% endfor %}
</div>