---
layout: page
title: Projects
permalink: /project/
description: A growing collection of cool projects.
nav: true
nav_order: 3
display_categories: [research, exhibition]
horizontal: false
---

<div class="container">
  {% if site.enable_project_categories and page.display_categories %}

    {% for category in page.display_categories %}
      <a id="{{ category }}"></a>
      <h2 class="category">{{ category }}</h2>

      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}

      <div class="row g-4">
        {% for project in sorted_projects %}
          <div class="col-md-4">
            {% include projects.liquid %}
          </div>
        {% endfor %}
      </div>
    {% endfor %}

  {% else %}

    {% assign sorted_projects = site.projects | sort: "importance" %}

    <div class="row g-4">
      {% for project in sorted_projects %}
        <div class="col-md-4">
          {% include projects.liquid %}
        </div>
      {% endfor %}
    </div>

  {% endif %}
</div>
