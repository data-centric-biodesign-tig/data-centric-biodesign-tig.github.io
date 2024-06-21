---
layout: page
title: Talks
permalink: /talks/
description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [present, future, past]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category }}</h2>
    </a>
    {% assign categorized_projects = site.projects | where: "category", category %}
    {% assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    {% if category == 'present' %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-1">
          {% for project in sorted_projects %}
            {% include projects_horizontal.liquid category=category %}
          {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for project in sorted_projects %}
            {% include projects_horizontal.liquid category=category %}
          {% endfor %}
        </div>
      </div>
    {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->
{% assign sorted_projects = site.projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  <div class="container">
    <div class="row row-cols-1 row-cols-md-1">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>

{% endif %}
</div>
