---
layout: default
title: Papers
permalink: /papers/
weight: 3
group: pubs
---

{% assign papers_by_year = site.data.papers | group_by_exp:"paper", "paper.year | plus: 0" %}
{% for year in papers_by_year %}
  <h2>{{ year.name }}</h2>
  {% for paper in year.items %}
  <div class="publication">
    <div class="publication-title">
      {{ paper.authors }}. <b>{{ paper.title }}</b>. {{ paper.venue }}{% if paper.pages %}, {{ paper.pages }}{% endif %}.
    </div>
    <div class="publication-links">
      <a class="pub-link" href="{{ "/resources/papers/" | append: paper.id | append: ".pdf" | prepend: site.baseurl }}" target="_blank">
        <img src="{{ "/resources/icons/pdf.png" | prepend: site.baseurl }}" title="PDF" alt="PDF" />
      </a>
      {% if paper.code %}
      <a class="pub-link" href="{{ paper.code }}" target="_blank">
        <img src="{{ "/resources/icons/uw.png" | prepend: site.baseurl }}" title="GitHub" alt="GitHub" />
      </a>
      {% endif %}
      {% if paper.video %}
      <a class="pub-link" href="{{ paper.video }}" target="_blank">
        <img src="{{ "/resources/icons/dl.png" | prepend: site.baseurl }}" title="YouTube" alt="YouTube" />
      </a>
      {% endif %}
    </div>
  </div>
  {% endfor %}
{% endfor %}
