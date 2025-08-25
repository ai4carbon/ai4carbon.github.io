---
layout: page
permalink: /resources/
title: resources
---

# Datasets
<div class="datasets">
  {% assign sorted_datasets = site.datasets | sort: "importance" %}
  {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
        {% for dataset in sorted_datasets %}
          {% include projects_horizontal.liquid project=dataset %}
        {% endfor %}
      </div>
    </div>
  {% else %}
    <div class="row row-cols-1 row-cols-md-3">
      {% for dataset in sorted_datasets %}
        {% include projects.liquid project=dataset %}
      {% endfor %}
    </div>
  {% endif %}
</div>

# Bibliography

<!-- _pages/publications.md -->
<div class="publications">
<p>*indicates joint first authorship</p>
{% bibliography %}

</div>