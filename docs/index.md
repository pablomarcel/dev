---
title: ""
layout: single
classes: "wide page--home"
excerpt: "Python • Control Systems • Robotics • Web"
---

## Featured Projects

{% assign featured = site.projects | where_exp: "p", "p.featured == true" | sort: "date" | reverse %}
{% if featured.size > 0 %}
<div class="grid">
{% for p in featured limit: 6 %}
  <div class="project-card">
    <div class="card-media">
      {% if p.thumb %}<img src="{{ p.thumb | relative_url }}" alt="{{ p.title }} thumbnail">{% endif %}
    </div>
    <div class="card-body">
      <h3 style="margin-top:.6rem;">{{ p.title }}</h3>
      <p>{{ p.stack }}</p>
    </div>
    <div class="card-buttons">
      <a class="btn-pill" href="{{ p.url | relative_url }}">More</a>
      {% if p.hyperlink %}<a class="btn-pill" href="{{ p.hyperlink }}" target="_blank" rel="noopener">Link</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
{% endif %}

## Latest Projects

<div class="grid">
{% assign latest = site.projects | sort: "date" | reverse %}
{% for p in latest limit: 12 %}
  <div class="project-card">
    <div class="card-media">
      {% if p.thumb %}<img src="{{ p.thumb | relative_url }}" alt="{{ p.title }} thumbnail">{% endif %}
    </div>
    <div class="card-body">
      <h3 style="margin-top:.6rem;">{{ p.title }}</h3>
      <p>{{ p.stack }}</p>
    </div>
    <div class="card-buttons">
      <a class="btn-pill" href="{{ p.url | relative_url }}">More</a>
      {% if p.hyperlink %}<a class="btn-pill" href="{{ p.hyperlink }}" target="_blank" rel="noopener">Link</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
