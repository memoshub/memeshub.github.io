---
layout: default
name: svetashov
permalink: /svetashov/
---


<div class="posts">
{% for post in site.posts %}
{% if post.author == "svetashov" %}
 <article class="post">



    <div class="author-line">
    	<a href="/{{ post.author }}.md">
    	<img src="/images/author-{{ post.author }}.png" class="author-img"> 
    		<div class="author-name">
    				<h1>{{ post.author }}</h1>
    		</div>
    		</a>
    		<div class="datetime">
    			<p>{{ post.date | date: "%d %b %H:%M" }}</p>
    		</div>
    </div>
    {% if post.comment %}
    <div class="author-comment">
    	{{ post.comment }}
    </div> 
    {% endif %}
    
    <div class="mem">
    	<a rel="simplebox" href="/memes/{{ post.image }}">
		<img src="/memes/{{ post.image }}"></a>

    </div>
    
    <div class="tags">
    	{% for tag in post.categories %}
    		<a href="/tags/{{ tag }}.md">#{{ tag }}</a>
    	{% endfor %}
    </div>
{% endif %}
{% endfor %}
</div>