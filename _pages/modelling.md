---
layout: archive
permalink: /modelling/
title: "Machine learning posts by tags"
author_profile: true
header:
 image: "/images/header_2.jpg"
---




{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}