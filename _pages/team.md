---
title: "People"
layout: page
permalink: /team/
---

# People

<p class="page-intro">CyTRAIL Lab researchers at the University of New Haven.</p>

{% assign pi = site.data.pi[0] %}
## Faculty

<div class="section-card" markdown="0">
<div class="pi-card">
{% if pi.photo %}<img src="{{ pi.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ pi.name }}" width="160" height="160">{% else %}<div class="pi-photo initials-avatar" aria-hidden="true">{{ pi.initials }}</div>{% endif %}
<div>
<h3 class="pi-name">{{ pi.name }}</h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ pi.role }}</p>
<div class="chip-container">
{% for area in pi.areas %}<span class="chip chip-muted">{{ area }}</span>
{% endfor %}
</div>
</div>
</div>
{% if pi.bio %}<div class="pi-bio">
{% for paragraph in pi.bio %}<p>{{ paragraph }}</p>
{% endfor %}</div>{% endif %}
</div>

{% if site.data.team_members.size > 0 %}
## Current Researchers

<div class="team-grid" markdown="0">
{% for member in site.data.team_members %}
{% include person-card.html member=member %}
{% endfor %}
</div>
{% endif %}

{% if site.data.alumni.size > 0 %}
## Former Researchers &amp; Alumni

<div class="team-grid" markdown="0">
{% for member in site.data.alumni %}
{% include person-card.html member=member alumni=true %}
{% endfor %}
</div>
{% endif %}
