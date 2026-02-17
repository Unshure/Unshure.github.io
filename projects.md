---
layout: page
title: Projects
permalink: /projects/
---

A selection of projects I've built or contributed to.

<div class="project-grid">
{% assign sorted_projects = site.projects | sort: "position" %}
{% for project in sorted_projects %}
  <a href="{{ project.url | relative_url }}" class="project-card">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </a>
{% endfor %}
</div>

---

See more on my [GitHub profile](https://github.com/Unshure).
