---
layout: default
title: Projects
permalink: /projects/
---

# HW5

{% assign hw5 = site.projects | where: "title", "hw5" | first %}
{% if hw5 %}
  <h2><a href="{{ hw5.url }}">{{ hw5.title }}</a></h2>
  {% if hw5.description %}
    <p>{{ hw5.description }}</p>
  {% endif %}
  {% if hw5.technologies %}
    <p><strong>Technologies:</strong> {{ hw5.technologies | join: ", " }}</p>
  {% endif %}
  {% if hw5.images %}
    <div>
      {% for img in hw5.images %}
        <img src="{{ img | relative_url }}" alt="{{ hw5.title }} image" style="max-width:300px;">
      {% endfor %}
    </div>
  {% endif %}
  <div>
    {{ hw5.content }}
  </div>
{% else %}
  <p>Project not found.</p>
{% endif %}
