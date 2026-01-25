---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<ul style="list-style:none; padding-left:0;">
{% for post in site.publications reversed %}
  {% if post.permalink != "/publications/" %}
  <li style="margin-bottom:1rem;">
    <!-- Title -->
    <strong><a href="{{ post.url | relative_url }}" style="text-decoration:none; color:inherit;">{{ post.title }}</a></strong>
    
    <!-- Venue / Year -->
    <div style="font-size:0.9rem; color:inherit; margin-top:0.2rem;">
      {% if post.venue %}{{ post.venue }}{% endif %}
      {% if post.date %} ({{ post.date | date: "%Y" }}){% endif %}
    </div>

    <!-- PDF / Link -->
    {% if post.paperurl %}
    <div style="font-size:0.9rem; margin-top:0.1rem;">
      <a href="{{ post.paperurl }}" target="_blank" style="color:inherit;">[PDF / link]</a>
    </div>
    {% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>
