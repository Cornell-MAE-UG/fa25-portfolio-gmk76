---
layout: default
title: Projects
permalink: /projects/
---

# HW5

{% assign hw5 = site.projects | where: "title", "HW5" | first %}
{% if hw5 %}
  <h2><a href="{{ hw5.url }}">{{ hw5.title }}</a></h2>
  {% if hw5.description %}
    <p>{{ hw5.description }}</p>
  {% endif %}
  <!-- You can add more fields as needed, e.g., date, tags, etc. -->
{% else %}
  <p>Project HW5 not found.</p>
{% endif %}
