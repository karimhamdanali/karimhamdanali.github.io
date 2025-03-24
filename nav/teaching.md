---
layout: default
title: Teaching
permalink: /teaching/
weight: 4
group: teaching
---
### Current Courses
{% assign current = site.data.courses | where:"status","current" %}
{% include courses.html data=current %}

### Previous Courses
{% assign former = site.data.courses | where:"status","former" %}
{% include courses.html data=former %}
