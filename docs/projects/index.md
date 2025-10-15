---
title: "Projects"
layout: archive
permalink: /projects/
---

{% assign projects = site.projects | sort: "date" | reverse %}
{% for p in projects %}
  {% include archive-single.html type="grid" %}
{% endfor %}
