---
title: ""
layout: single
classes: "page--home"
description: "Python • Control Systems • Web"
---

## Featured Projects {: #featured-projects }

<div class="stack">
{% assign featured = site.projects | where_exp: "p", "p.featured == true" | sort: "date" | reverse %}
{% for p in featured %}
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

## Latest Projects {: #latest-projects }

<div class="stack">
{% assign latest = site.projects | sort: "date" | reverse %}
{% for p in latest %}
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
