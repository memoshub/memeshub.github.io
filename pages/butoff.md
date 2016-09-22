---
layout: author
aname: butoff
permalink: /butoff/
stat: Я могу назвать себя мемологом, потому что&#058 <br> Я шарю в мемасах<br> Ору над ними<br> И потому что ты петух
vk: id166666047
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
    <img src="/memes/{{ post.image }}"></a>
</div>
<div class="tags">
    {% for tag in post.categories %}
    <a href="/{{ tag }}">#{{ tag }}</a>
    {% endfor %}
    {% endif %}
    {% endfor %}
</div>