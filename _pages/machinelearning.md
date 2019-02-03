---
layout: arquive
permalink: /machine-learning/
title: "Manipulação de Dados"
author_profile: true
header:
  image: "/images/city-863692_1920.png"
---

# Projetos de Machine learning

Projetos mais relevantes:

1. Bikeshare



{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
