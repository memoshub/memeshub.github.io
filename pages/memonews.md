---
layout: default
permalink: /memonews/
---
<p style="text-align: center; font-size: 2em; margin-bottom: 30px;">Самые горячие МемоНовости</p>
<div class="posts">
{% for post in site.posts %}
{% if post.news %}
    {% include post.html %}
{% endif %}
{% endfor %}
    <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>
</div>