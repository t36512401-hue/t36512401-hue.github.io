---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<ul style="list-style:none; padding-left:0;">
{% for post in site.publications reversed %}
  {% if post.permalink != "/publications/" %}
  <li style="margin-bottom:1rem; border-bottom:1px solid #ddd; padding-bottom:0.5rem;">
    <strong><a href="{{ post.url | relative_url }}" style="text-decoration:none; color:#0366d6;">{{ post.title }}</a></strong>
    <div style="font-size:0.9rem; color:#555; margin-top:0.2rem;">
      {% if post.venue %}{{ post.venue }}{% endif %}
      {% if post.date %} ({{ post.date | date: "%Y" }}){% endif %}
    </div>
    {% if post.paperurl %}
    <div style="font-size:0.9rem; margin-top:0.1rem;">
      <a href="{{ post.paperurl }}" target="_blank" style="color:#0366d6;">[PDF / link]</a>
    </div>
    {% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>
