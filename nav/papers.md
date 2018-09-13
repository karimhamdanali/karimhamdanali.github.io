---
layout: default
title: Papers
permalink: /papers/
weight: 3
group: pubs
---

{% assign papers_by_year = site.data.papers | group_by_exp:"paper", "paper.year | plus: 0" %}
{% for year in papers_by_year %}
  <h3>{{ year.name }}</h3>
  {% for paper in year.items %}
  <div class="publication" id="{{ paper.id }}">
    {% if paper.award %}
    <span class="icon">
      <svg><use xlink:href="#icon-award"/></svg>
      <b>{{ paper.award }}</b>
    </span> <br/>
    {% endif %}
    <div class="publication-title">
      {{ paper.authors }}. {{ paper.title }}. {{ paper.venue }}{% if paper.pages %}, {{ paper.pages }}{% endif %}.
    </div>
    <div class="right">
      <a href="{{ "/resources/papers/" | append: paper.id | append: ".pdf" | prepend: site.baseurl }}" target="_blank">
        <span class="icon"><svg><use xlink:href="#icon-pdf"/></svg></span>
      </a>
      {% if paper.code %}
      <a href="{{ paper.code }}" target="_blank">
        <span class="icon"><svg><use xlink:href="#icon-github"/></svg></span>
      </a>
      {% endif %}
      {% if paper.video %}
      <a href="{{ paper.video }}" target="_blank">
        <span class="icon"><svg><use xlink:href="#icon-youtube"/></svg></span>
      </a>
      {% endif %}
    </div>
  </div>
  {% endfor %}
{% endfor %}
