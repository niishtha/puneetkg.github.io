---
layout: archive
permalink: /learning/
title: "machine Learning posts for learning"
author_profile: true
header:
 image: "/images/header_4.jpg"
---


{% include group-by-array collection=site.learningposts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>

  {% for post in learningposts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
