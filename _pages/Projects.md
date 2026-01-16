---
layout: page
permalink: /projects/
title: Projects
subtitle: Documentation of the works.
description: >
  Kindly hit me up through [email](mailto:fatimahasyapk2015@gmail.com) and let's see what we can do together! 
nav: true
nav_order: 2
horizontal: false
---

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}

  {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
      </div>
    </div>
  {% else %}
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  {% endif %}
</div>
