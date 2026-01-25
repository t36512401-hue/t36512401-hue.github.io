---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<div style="margin-top:2rem;"> <!-- noticeable space below the title -->

<ul style="list-style:none; padding-left:0;">
{% for post in site.publications reversed %}
  <li style="margin-bottom:1.2rem;">
    <!-- Paper title -->
    <strong>
      <a href="{{ post.url | relative_url }}" style="text-decoration:none; color:inherit;">
        {{ post.title }}
      </a>
    </strong>
    
    <!-- Journal / venue -->
    {% if post.venue or post.date %}
    <div style="font-size:0.9rem; color:var(--color-fg-muted); margin-top:0.2rem;">
      {% if post.venue %}{{ post.venue }}{% endif %}
      {% if post.date %} ({{ post.date | date: "%Y" }}){% endif %}
    </div>
    {% endif %}

    <!-- PDF / paper link -->
    {% if post.paperurl %}
    <div style="font-size:0.9rem; margin-top:0.1rem;">
      <a href="{{ post.paperurl }}" target="_blank" style="color:var(--color-accent); text-decoration:underline;">
        PDF / Link
      </a>
    </div>
    {% endif %}
  </li>
{% endfor %}
</ul>
