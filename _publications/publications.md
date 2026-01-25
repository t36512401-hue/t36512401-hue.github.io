---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<br><br>

<ul>
{% for post in site.publications reversed %}
  {% if post.permalink != "/publications/" %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    {% if post.venue %} — <em>{{ post.venue }}</em>{% endif %}
    {% if post.date %} ({{ post.date | date: "%Y" }}){% endif %}
    {% if post.paperurl %} — <a href="{{ post.paperurl }}" target="_blank">[PDF/link]</a>{% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>
