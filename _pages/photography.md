---
layout: page
title: photography
permalink: /photography/
description: A collection of some photography I have done.
nav: true
nav_order: 3
display_categories: [landscapes, travel, portraits] # the photo album themes, in display order
horizontal: false
---

<!-- pages/photography.md -->
<!--
  This page automatically builds itself from the album files in the _photography/ folder.
  Each album shows up here as a clickable card, grouped under its theme (category).
  To add a new album: create a new file in _photography/ with a `category:` that
  matches one of the themes in `display_categories` above (or add a new theme there).
-->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized albums -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_albums = site.photography | where: "category", category %}
  {% assign sorted_albums = categorized_albums | sort: "importance" %}
  <!-- Generate cards for each album -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_albums %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_albums %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display albums without categories -->

{% assign sorted_albums = site.photography | sort: "importance" %}

  <!-- Generate cards for each album -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_albums %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_albums %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
