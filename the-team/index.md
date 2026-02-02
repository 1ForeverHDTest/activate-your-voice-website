---
title: The Team
layout: page
---

We’re a friendly, experienced team focused on empowering voices.

<div class="team-grid">
  {% for member in site.team %}
    <a class="team-card" href="{{ member.url | relative_url }}">
      {% if member.photo %}
        <img src="{{ member.photo | relative_url }}" alt="{{ member.name }}" />
      {% endif %}
      <h3>{{ member.name }}</h3>
      <p>{{ member.role }}</p>
    </a>
  {% endfor %}
</div>
