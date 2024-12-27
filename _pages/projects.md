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

**Interests.** My research broadly centers on leveraging emergent technologies
to engineer software systems designed to measure and improve network service
performance. My work particularly focuses on the development of methods that
integrate state-of-the-art concepts in network systems and measurement with data
science and machine learning techniques.

**Goals and Approach.** I aim to utilize the increasing availability of computing resources within network infrastructure to create impactful network management tools that transform how networks operate. A cornerstone of my research is a practical approach to advanced challenges that emphasizes three key objectives:

1.	Validation: Designing systems rigorously evaluated in real-world environments.
2.	Reusability: Ensuring that tools and solutions are verifiable, reusable, and extensible by the research community.
3.	Impact: Creating broader benefits for both ISPs and end-users.

**Code and Datasets.** I strongly believe that building systems is one of the most effective ways to to validate research hypotheses. To this end, my work strives to design and open source tools and collect unique datasets tailored to network management and measurement tasks. 

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
