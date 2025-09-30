---
layout: page
title: Research Projects
permalink: /projects/
# description: A growing collection of your cool projects.
nav: true
nav_order: 1
display_categories: [current, past]
horizontal: false
---

<p style=margin-bottom: 16px;">&nbsp;</p>

Understanding human language plays a pivotal role in creating intelligent systems. With that in view, Banerjee's research spans multiple areas that bring together machine learning (ML) and natural language processing (NLP): biomedical knowledge discovery for better healthcare, misinformation analysis, and linguistics for security and privacy.

Language use varies a lot depending on the what (content), why (intent), who (speaker/writer and audience), and how (style). Natural language understanding can be improved based on these insights, and intelligent systems built using a deeper understanding of human language can be employed for immense social good. The language used in medical research, for instance, is highly specialized as it is meant for technical comprehension by other researchers in that field; but a system capable of understanding it, and extracting useful information from it, can help healthcare practitioners and patients. Quotidian language use, on the other hand, is dictated by various aspects of individual and collective human behavior. An intelligent system can be refined to provide better help to individuals and/or social groups by interpretation of (and inference from) language.

<p style=margin-bottom: 16px;">&nbsp;</p>

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
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
