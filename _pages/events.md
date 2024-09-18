---
layout: page
title: Events
permalink: /events/
description: Events organized by the interest group.
nav: true
nav_order: 3
display_categories: [next, upcoming, past]  # Changed 'future' to 'upcoming'
horizontal: false
---


<style>
  .category {
    color: #000; /* Set text color to black for high contrast */
    font-weight: bold; /* Make the text bold */
    font-size: 2em; /* Increase the font size */
    opacity: 1; /* Ensure full opacity */
    margin-top: 1.5em; /* Add space above the heading */
  }
</style>

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category | capitalize }}</h2>  <!-- Capitalize category names -->
    </a>
    {% assign categorized_projects = site.projects | where: "category", category %}
    {% assign sorted_projects = categorized_projects | sort: "importance" %}
    
    <!-- Generate cards for each project -->
    {% if category == 'next' %}
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
