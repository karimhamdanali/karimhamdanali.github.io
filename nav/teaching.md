---
layout: default
title: Teaching
permalink: /teaching/
weight: 4
group: teaching
---
These are the courses that I regularly teach.
{% for course in site.data.courses %}
<div class="row" name="{{ course.id }}">
	<div class="row-pic">
		{% include /functions/getcoursepic.html course=course %}
	</div>
	<div class="row-info">
		<a href="{{ course.website | default: "#" }}" target="_blank">{{ course.code }} &ndash; {{ course.name }}</a>
		<p>{{ course.description }}</p>
	</div>
</div>
{% endfor %}
