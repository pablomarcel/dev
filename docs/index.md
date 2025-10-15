---
title: ""
layout: single
classes: "wide page--home"
excerpt: "Python • Control Systems • Robotics • Web"
---

<!-- Left TOC Rail -->
<nav class="left-rail" aria-label="Sections">
  <h4>Sections</h4>
  <ul>
    <li><a href="#featured">Featured Projects</a></li>
    <li><a href="#latest">Latest Projects</a></li>
  </ul>
</nav>

## Featured Projects {: #featured }

<div class="stack">
{% assign featured = site.projects | where_exp: "p", "p.featured == true" | sort: "date" | reverse %}
{% for p in featured limit: 6 %}
  <div class="project-card">
    <div class="card-media">
      {% if p.thumb %}<img src="{{ p.thumb | relative_url }}" alt="{{ p.title }} thumbnail">{% endif %}
    </div>
    <div class="card-body">
      <h3>{{ p.title }}</h3>
      <p>{{ p.stack }}</p>
    </div>
    <div class="card-buttons">
      <a class="btn-pill" href="{{ p.url | relative_url }}">More</a>
      {% if p.hyperlink %}<a class="btn-pill" href="{{ p.hyperlink }}" target="_blank" rel="noopener">Link</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

## Latest Projects {: #latest }

<div class="stack">
{% assign latest = site.projects | sort: "date" | reverse %}
{% for p in latest limit: 12 %}
  <div class="project-card">
    <div class="card-media">
      {% if p.thumb %}<img src="{{ p.thumb | relative_url }}" alt="{{ p.title }} thumbnail">{% endif %}
    </div>
    <div class="card-body">
      <h3>{{ p.title }}</h3>
      <p>{{ p.stack }}</p>
    </div>
    <div class="card-buttons">
      <a class="btn-pill" href="{{ p.url | relative_url }}">More</a>
      {% if p.hyperlink %}<a class="btn-pill" href="{{ p.hyperlink }}" target="_blank" rel="noopener">Link</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
