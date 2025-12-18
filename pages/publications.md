---
layout: default
title: Publications
---

# Publications

{% for year_data in site.data.publications %}
  {% assign year = year_data[0] %}
  {% assign publications = year_data[1] %}
  
  {% unless year == 'book_chapters' %}
## {{ year }}

{% for pub in publications %}
<div class="publication">
  <div class="publication-title">{{ pub.title }}</div>
  <div class="publication-authors">{{ pub.authors | join: ', ' }}</div>
  <div class="publication-journal">
    <em>{{ pub.journal }}</em>{% if pub.volume %}, {{ pub.volume }}{% endif %}{% if pub.pages %}: {{ pub.pages }}{% endif %} ({{ pub.year }})
    {% if pub.doi %}
      | <a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>
    {% endif %}
  </div>
</div>
{% endfor %}
  {% endunless %}
{% endfor %}

## Book Chapters

{% for pub in site.data.publications.book_chapters %}
<div class="publication">
  <div class="publication-title">{{ pub.title }}</div>
  <div class="publication-authors">{{ pub.authors | join: ', ' }}</div>
  <div class="publication-journal">
    In: <em>{{ pub.book }}</em>{% if pub.editors %} (Eds: {{ pub.editors | join: ', ' }}){% endif %}. {{ pub.publisher }} ({{ pub.year }})
    {% if pub.doi %}
      | <a href="https://doi.org/{{ pub.doi }}" target="_blank">DOI</a>
    {% endif %}
  </div>
</div>
{% endfor %}