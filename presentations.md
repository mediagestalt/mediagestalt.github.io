---
layout: page
title: Presentations
---
<ul>
  {% for post in site.categories.presentations %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
