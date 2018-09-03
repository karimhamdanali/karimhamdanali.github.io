---
layout: default
title: Research
weight: 1
group: research
---

Few static analyses make their way to the real-world due to the unrealistic assumptions that they make. I am interested in developing and evaluating various program analysis techniques that can be used in practice by exploring three aspects: scalability, precision, and usability. My interests span programming languages, software systems, and software engineering.

Below is a list of my current and inactive projects.

### Current Projects
{% assign current = site.data.projects | where_exp: "project", "project.end == nil" %}
{% include projects.html data=current %}

### Inactive Projects
{% assign inactive = site.data.projects | where_exp: "project", "project.end != nil" %}
{% include projects.html data=inactive %}
