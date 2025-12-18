---
layout: default
title: News
---

# News

<div class="news-list">
{% for item in site.data.news %}
<a href="{{ item.link }}" target="_blank" class="news-item">
  <div class="news-item-date">{{ item.date | date: "%b %d, %Y" }}</div>
  <div class="news-item-content">
    <h3>{{ item.title }}</h3>
    <p>{{ item.description }}</p>
  </div>
  <div class="news-item-arrow">→</div>
</a>
{% endfor %}
</div>