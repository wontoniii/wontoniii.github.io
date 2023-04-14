---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<h2> Conferences, Journals, and Workshops </h2>
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f journal -f conf -f workshop -q @*[year={{y}}]* %}
{% endfor %}
</div>

<!-- <h2> Demos, Posters, and Tutorials </h2> -->
<!-- <div class="publications"> -->

<!-- {sss% bibliography -f dpt %sss}  -->
<!-- </div>  -->
