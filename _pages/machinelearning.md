---
layout: single
permalink: /Projetos/
title: "Projetos de Aprendizado de Máquina"
author_profile: true
header:
  image: "/images/city-863692_1920.jpg"
  caption: "Photo by Foundry Co in Pixabay"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
