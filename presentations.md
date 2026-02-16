---
layout: page
title: Presentations
permalink: /presentations/
---

Talks and presentations I've given at conferences and events.

<div class="presentation-list">
{% assign sorted = site.presentations | sort: "date" | reverse %}
{% for pres in sorted %}
  <a href="{{ pres.url | relative_url }}" class="presentation-card">
    <div class="presentation-date">{{ pres.date | date: "%B %Y" }}</div>
    <h3>{{ pres.title }}</h3>
    <p>{{ pres.description }}</p>
  </a>
{% endfor %}
</div>
