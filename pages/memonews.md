---
layout: default
permalink: /memonews/
---
<p style="text-align: center; font-size: 2em; margin-bottom: 30px;">Самые горячие МемоНовости</p>
<div class="posts">
{% for post in site.posts %}
{% if post.news %}
    <article class="post">
        <div class="author-line">
            <a href="/{{ post.author }}">
                <img src="/images/author-{{ post.author }}.png" class="author-img"> <img src="/images/news-logo.png">
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
            <p>{{ post.comment }}</p>
            <p class="istochnik">Источник: <a href="{{post.news}}" target="_blank">{{post.news}}</a></p>
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
        </div>
        <div class="vk-share-button"><a href='http://vk.com/share.php?url=https://memoshub.github.io{{ post.url | uri: absolute }}&image={{post.image}}' target='_blank' onclick="window.open('http://vk.com/share.php?url=https://memoshub.github.io{{ post.url | uri: absolute }}&image={{post.image}}', this.title, 'toolbar=0, status=0, width=548, height=325'); return false"><img src="/images/vk1.png"><span>Поделиться</span></a></div>
        <a href="http://twitter.com/share?text=&url=https://memoshub.github.io{{post.url}}" title="Поделиться ссылкой в Твиттере" onclick="window.open(this.href, this.title, 'toolbar=0, status=0, width=548, height=325'); return false" target="_parent" class="twitter-share-button" data-size="large">Твитнуть</a>
    </article>
{% endif %}
{% endfor %}
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>
</div>