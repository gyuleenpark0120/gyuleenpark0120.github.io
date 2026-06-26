---
layout: page
title: projects
permalink: /projects/
description: Research and engineering projects spanning AI systems for scientific discovery and experimental materials science.
nav: true
nav_order: 2
---

<div class="proj-filter-bar">
  <button class="proj-filter-btn active" data-filter="all">All</button>
  <button class="proj-filter-btn" data-filter="AI for Scientific Discovery">
    <i class="fa-solid fa-brain"></i>&nbsp; AI for Scientific Discovery
  </button>
  <button class="proj-filter-btn" data-filter="Experimental Materials Science">
    <i class="fa-solid fa-flask-vial"></i>&nbsp; Experimental Materials Science
  </button>
</div>

<div class="proj-cards-grid">
{% assign all_projects = site.projects | sort: "importance" %}
{% for project in all_projects %}
<a href="{{ project.url | relative_url }}" class="proj-card-link" data-category="{{ project.category }}" data-tags="{{ project.tags | join: ',' }}">
  <div class="proj-card {% if project.category == 'AI for Scientific Discovery' %}proj-card-ai{% else %}proj-card-exp{% endif %}">
    <div class="proj-cat-pill {% if project.category == 'AI for Scientific Discovery' %}pill-ai{% else %}pill-exp{% endif %}">
      {% if project.category == "AI for Scientific Discovery" %}
        <i class="fa-solid fa-brain"></i> AI for Scientific Discovery
      {% else %}
        <i class="fa-solid fa-flask-vial"></i> Experimental Materials Science
      {% endif %}
    </div>
    <h3 class="proj-card-title">{{ project.title }}</h3>
    {% if project.institution %}<div class="proj-institution"><i class="fa-solid fa-building"></i> {{ project.institution }}</div>{% endif %}
    <p class="proj-card-desc">{{ project.description }}</p>
    {% if project.tags %}
    <div class="proj-tags-row">
      {% for tag in project.tags limit: 4 %}
        <span class="proj-tag">{{ tag }}</span>
      {% endfor %}
    </div>
    {% endif %}
    <div class="proj-card-arrow"><i class="fa-solid fa-arrow-right"></i></div>
  </div>
</a>
{% endfor %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  var btns = document.querySelectorAll('.proj-filter-btn');
  var cards = document.querySelectorAll('.proj-card-link');

  function filterCards(category, skill) {
    cards.forEach(function (card) {
      var catMatch = !category || category === 'all' || card.dataset.category === category;
      var tagMatch = !skill || (card.dataset.tags || '').toLowerCase().includes(skill.toLowerCase());
      card.style.display = (catMatch && tagMatch) ? '' : 'none';
    });
  }

  // Handle URL ?skill= param on load
  var params = new URLSearchParams(window.location.search);
  var skillParam = params.get('skill');
  if (skillParam) {
    filterCards('all', skillParam);
    var label = document.createElement('div');
    label.className = 'proj-skill-filter-label';
    label.innerHTML = 'Filtered by skill: <strong>' + skillParam + '</strong> <button onclick="window.location.href=window.location.pathname" class="proj-clear-btn">✕ clear</button>';
    document.querySelector('.proj-filter-bar').after(label);
  }

  btns.forEach(function (btn) {
    btn.addEventListener('click', function () {
      btns.forEach(function (b) { b.classList.remove('active'); });
      this.classList.add('active');
      filterCards(this.dataset.filter, null);
    });
  });
});
</script>
