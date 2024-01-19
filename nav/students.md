---
layout: default
title: Students
permalink: /maplers/
weight: 2
group: students
---

<figure>
	<img style="display=inline-block" width="15%" src="{{ "/resources/images/maple.png" |  prepend: site.baseurl }}" alt="The Maple Lab" />
</figure>

Maplers are members of my research lab (Maple), including postdoctoral researchers, master's and doctoral students, as well as undergrad research assistants. If you are interested in joining Maple, please read [this information page](/apply) before contacting me.

Below is a list of current and alumni Maplers.

### Current Maplers
{% assign current = site.data.maplers | where:"status","current" %}
{% include maplers.html data=current %}

### Alumni Maplers
{% assign former = site.data.maplers | where:"status","former" %}
{% include maplers.html data=former %}
