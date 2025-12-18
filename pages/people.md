---
layout: default
title: People
---

# Meet the team!

<div class="people-grid">
{% for person in site.data.people.principal_investigator %}
<div class="person-card" onclick="openModal('modal-pi-{{ forloop.index }}')">
  <div class="person-card-header">
    {% if person.image %}
      <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-photo-card">
    {% endif %}
    <div class="person-card-overlay">
      <h3>{{ person.name }}</h3>
      <p class="person-role">{{ person.role }}</p>
    </div>
  </div>
</div>

<div id="modal-pi-{{ forloop.index }}" class="modal">
  <div class="modal-content">
    <span class="modal-close" onclick="closeModal('modal-pi-{{ forloop.index }}')">&times;</span>
    <div class="modal-body">
      {% if person.image %}
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="modal-photo">
      {% endif %}
      <div class="modal-info">
        <h2>{{ person.name }}</h2>
        <p class="modal-role">{{ person.role }}</p>
        {% if person.bio %}
          <p>{{ person.bio }}</p>
        {% endif %}
        <div class="modal-links">
          {% if person.email %}
            <p><strong>Email:</strong> <a href="mailto:{{ person.email }}">{{ person.email }}</a></p>
          {% endif %}
          {% if person.website %}
            <p><strong>Website:</strong> <a href="{{ person.website }}" target="_blank">{{ person.website }}</a></p>
          {% endif %}
          {% if person.orcid %}
            <p><strong>ORCID:</strong> <a href="https://orcid.org/{{ person.orcid }}" target="_blank">{{ person.orcid }}</a></p>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
</div>
{% endfor %}
{% for person in site.data.people.current_members %}
<div class="person-card" onclick="openModal('modal-{{ forloop.index }}')">
  <div class="person-card-header">
    {% if person.image %}
      <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-photo-card">
    {% endif %}
    <div class="person-card-overlay">
      <h3>{{ person.name }}</h3>
      <p class="person-role">{{ person.role }}</p>
    </div>
  </div>
</div>

<div id="modal-{{ forloop.index }}" class="modal">
  <div class="modal-content">
    <span class="modal-close" onclick="closeModal('modal-{{ forloop.index }}')">&times;</span>
    <div class="modal-body">
      {% if person.image %}
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="modal-photo">
      {% endif %}
      <div class="modal-info">
        <h2>{{ person.name }}</h2>
        <p class="modal-role">{{ person.role }}</p>
        {% if person.bio %}
          <p>{{ person.bio }}</p>
        {% endif %}
        <div class="modal-links">
          {% if person.email %}
            <p><strong>Email:</strong> <a href="mailto:{{ person.email }}">{{ person.email }}</a></p>
          {% endif %}
          {% if person.website %}
            <p><strong>Website:</strong> <a href="{{ person.website }}" target="_blank">{{ person.website }}</a></p>
          {% endif %}
          {% if person.orcid %}
            <p><strong>ORCID:</strong> <a href="https://orcid.org/{{ person.orcid }}" target="_blank">{{ person.orcid }}</a></p>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
</div>
{% endfor %}

{% for person in site.data.people.undergraduates %}
<div class="person-card" onclick="openModal('modal-undergrad-{{ forloop.index }}')">
  <div class="person-card-header">
    {% if person.image %}
      <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="person-photo-card">
    {% endif %}
    <div class="person-card-overlay">
      <h3>{{ person.name }}</h3>
      <p class="person-role">{{ person.role }}</p>
    </div>
  </div>
</div>

<div id="modal-undergrad-{{ forloop.index }}" class="modal">
  <div class="modal-content">
    <span class="modal-close" onclick="closeModal('modal-undergrad-{{ forloop.index }}')">&times;</span>
    <div class="modal-body">
      {% if person.image %}
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}" class="modal-photo">
      {% endif %}
      <div class="modal-info">
        <h2>{{ person.name }}</h2>
        <p class="modal-role">{{ person.role }}</p>
        {% if person.bio %}
          <p>{{ person.bio }}</p>
        {% endif %}
        <div class="modal-links">
          {% if person.email %}
            <p><strong>Email:</strong> <a href="mailto:{{ person.email }}">{{ person.email }}</a></p>
          {% endif %}
          {% if person.website %}
            <p><strong>Website:</strong> <a href="{{ person.website }}" target="_blank">{{ person.website }}</a></p>
          {% endif %}
        </div>
      </div>
    </div>
  </div>
</div>
{% endfor %}
</div>

{% if site.data.people.alumni and site.data.people.alumni.size > 0 %}
## Alumni

<div class="alumni-list">
{% for person in site.data.people.alumni %}
  <div class="alumni-item">
    <strong>{{ person.name }}</strong> - {{ person.role }}
  </div>
{% endfor %}
</div>
{% endif %}

<script>
function openModal(modalId) {
  document.getElementById(modalId).style.display = 'block';
  document.body.style.overflow = 'hidden';
}

function closeModal(modalId) {
  document.getElementById(modalId).style.display = 'none';
  document.body.style.overflow = 'auto';
}

// Close modal when clicking outside
window.onclick = function(event) {
  if (event.target.classList.contains('modal')) {
    event.target.style.display = 'none';
    document.body.style.overflow = 'auto';
  }
}
</script>
