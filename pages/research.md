---
layout: default
title: Research
---

# Research

We remotely sense biodiversity and ecosystem function across spatial, temporal and ecological scales.

Limiting the negative consequences of the global biodiversity and climate crises requires the protection, restoration, and better management of our ecosystems. But we cannot keep up with today's challenges using field research alone; changes are happening too fast and they are too wide ranging. We need remote sensing to monitor and assess ecosystems and their biodiversity frequently and continuously across large areas. We develop the theory and methods to investigate biodiversity and ecosystem function, and assess the impact of protection, restoration, and management programs by connecting remote sensing and ecology.

## Current Projects

<div class="research-grid">
{% for project in site.research %}
<a href="{{ project.url | relative_url }}" class="research-card">
  <div class="research-card-image">
    {% if project.image %}
      <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
    {% else %}
      <div class="research-placeholder"></div>
    {% endif %}
    <div class="research-card-overlay">
      <span class="research-status {{ project.status }}">{{ project.status | capitalize }}</span>
    </div>
  </div>
  <div class="research-card-content">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </div>
</a>
{% endfor %}
</div>


