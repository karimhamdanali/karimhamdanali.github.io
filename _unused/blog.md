---
layout: default
title: Blog
permalink: /blog/
weight: 7
group: blog
---
<ul class="post-list">
{% for post in site.posts %}
<li>
	<h2>
		<a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
	</h2>
	{% if post.content contains site.excerpt_separator %}
	{{ post.content | split:site.excerpt_separator | first }}
		<a href="{{ post.url | prepend: site.baseurl }}">Read more...</a>
	{% else %}
		{{ post.content }}
	{% endif %}
</li>
{% endfor %}
</ul>
