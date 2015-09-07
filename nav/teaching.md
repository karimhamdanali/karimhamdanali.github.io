---
layout: page
title: Teaching
navtitle: Teaching
permalink: /teaching/
weight: 3
group: teaching
---

## Winter Semester 2015/16 ##

<ul class="post-list">
{% assign posts = site.posts | where: 'group','teaching' | sort:'weight', 'last' %}
{% for post in posts %}
<li>
	<!-- <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span> -->
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