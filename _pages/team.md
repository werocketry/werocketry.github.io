---
layout: single
title: Team
permalink: /team/
author_profile: false
---

Meet the faces behind WE Rocketry!

{% for year in site.data.teams %}

## {{ year[0] }} Team

<div class="team-grid">
  {% for member in year[1] %}
    <div class="team-member">
      <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
      <p class="name"><strong>{{ member.name }}</strong></p>
      <p class="position">{{ member.position }}</p>
      <p class="program">{{ member.program }}</p>
    </div>
  {% endfor %}
</div>
{% endfor %}
