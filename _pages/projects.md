---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 2
display_categories: [Funding, Projects]
horizontal: false
---

**Interests.** My research focuses broadly on leveraging emergent technologies to engineer software systems designed to measure and improve network service performance. Recently, I have given particular attention to the development of methods that bridge state-of-the-art concepts in network systems and measurement together with data science and machine learning applied to network inference.

**Goals and Approach.** My research exploits computing resources available in the network infrastructure to develop network management tools that can profoundly impact how networks operate. A key aspect to my work is a practical approach to advanced research informed by extensive experience converting academic research projects into functional solutions. Throughout my career, I have striven to build software that 1) validates the proposed system designs via real-world rigorous evaluation, 2) that can be verified, reused, and extended by the research community, and 3) that can achieve important broader implications for both ISPs and consumers at large.

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
