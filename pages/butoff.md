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
    <img src="{{ post.image }}"></a>
</div>
<div class="tags">
    {% for tag in post.categories %}
    <a href="/{{ tag }}">#{{ tag }}</a>
    {% endfor %}
</div>
<a href='http://vkontakte.ru/share.php?url=https://memeshub.github.io{{ post.url | uri: absolute }}' target='_blank'><img src='/images/vk.png' border='0' width='76' height='28' alt='' title='Поделиться ВКонтакте'></a>
    <a href="https://twitter.com/share" class="twitter-share-button" data-size="large" data-hashtags="memesHub">Tweet</a> <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>
</article>
{% endif %}
{% endfor %}