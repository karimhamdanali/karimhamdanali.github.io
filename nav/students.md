---
layout: default
title: SANADers
permalink: /sanaders/
weight: 2
group: students
---

<figure>
	<img style="display=inline-block" width="15%" src="{{ "/resources/images/sanad.png" |  prepend: site.baseurl }}" alt="The SANAD Lab" />
</figure>

SANADers are members of my research lab (SANAD), including postdoctoral researchers, master's and doctoral students, as well as undergrad research assistants. If you are interested in joining SANAD, please read [this information page](/apply) before contacting me.

Below is a list of current and alumni members.

### Current Members
{% assign current = site.data.maplers | where:"status","current" %}
{% include maplers.html data=current %}

### Alumni
{% assign former = site.data.maplers | where:"status","former" %}
{% include maplers.html data=former %}
