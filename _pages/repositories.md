---
layout: page
permalink: /software/
title: Software
description: 
nav: true
nav_order: 3
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_software = site.softwares | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_software -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_software -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>
