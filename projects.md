---
layout: page
title: Projects
permalink: /projects/
---

A selection of projects I've built or contributed to.

<div class="project-grid">
{% for project in site.projects %}
  <a href="{{ project.url | relative_url }}" class="project-card">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    {% for tag in project.tags %}
      <span class="tag">{{ tag }}</span>
    {% endfor %}
  </a>
{% endfor %}
</div>

---

See more on my [GitHub profile](https://github.com/Unshure).
