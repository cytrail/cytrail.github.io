---
title: "Research"
layout: page
permalink: /research/
---

# Research

<p class="page-intro">Four connected themes that follow the Lab's pipeline from vulnerability to threat, evidence, and defense.</p>

<!-- Themes are listed in _data/themes.yml, projects in _data/projects.yml -->
{% for theme in site.data.themes %}
{% assign theme_projects = site.data.projects | where: "theme", theme.id %}
<section class="research-theme" id="{{ theme.id }}" markdown="0">
<h2>{{ theme.title }}</h2>
<p class="theme-intro">{{ theme.summary }}</p>
<div class="research-grid">
{% for project in theme_projects %}{% unless project.hidden %}
<div class="research-card">
<div class="research-body">
<span class="chip{% if project.muted %} chip-muted{% endif %}">{{ project.status }}</span>
<h3 class="research-title">{{ project.title }}</h3>
{% for paragraph in project.description %}<p class="research-desc">{{ paragraph }}</p>
{% endfor %}{% if project.links %}<div class="research-links">{% for link in project.links %}<a class="chip" href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }} &nearr;</a>{% endfor %}</div>
{% endif %}{% if project.meta %}<p class="research-meta">{{ project.meta }}</p>{% endif %}
</div>
</div>
{% endunless %}{% endfor %}
</div>
</section>
{% endfor %}
