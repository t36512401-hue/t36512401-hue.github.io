---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<div style="display:flex; flex-direction:column; gap:1rem;">
{% for post in site.publications reversed %}
  {% if post.permalink != "/publications/" %}
  <div style="border-bottom:1px solid #ddd; padding-bottom:0.5rem;">
    <!-- Title as link -->
    <a href="{{ post.url | relative_url }}" style="font-weight:600; font-size:1.1rem; text-decoration:none; color:#1a0dab;">
      {{ post.title }}
    </a>
    
    <!-- Venue / Year -->
    <div style="font-size:0.9rem; color:#555; margin-top:0.2rem;">
      {% if post.venue %}{{ post.venue }}{% endif %}
      {% if post.date %} ({{ post.date | date: "%Y" }}){% endif %}
    </div>

    <!-- PDF link -->
    {% if post.paperurl %}
    <div style="font-size:0.9rem; margin-top:0.1rem;">
      <a href="{{ post.paperurl }}" target="_blank" style="color:#007acc;">[PDF / link]</a>
    </div>
    {% endif %}
  </div>
  {% endif %}
{% endfor %}
</div>
