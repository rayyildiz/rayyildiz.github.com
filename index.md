---
layout: page
title: rayyildiz.com
tagline: Bilgi Paylaşıldıkça Güzelleşir
---
{% include JB/setup %}

<p>
{% for post in site.posts limit:7 %}
	<h3><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h3>
	{{ post.date | date_to_string }} Yazan {{ site.author.name }} 
	<p>
	{{post.content}}
	</p>
	<hr />
	<br /><br />
{% endfor %}
</p>


<h2>Diğer Yazılar</h2>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

