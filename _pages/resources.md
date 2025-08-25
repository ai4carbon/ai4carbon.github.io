---
layout: page
permalink: /resources/
title: resources
nav: true
nav_order: 2
---

# Datasets
<div class="datasets">
  {% if site.datasets %}
    {% assign sorted_datasets = site.datasets | sort: "importance" %}
  {% else %}
    {% assign sorted_datasets = "" %}
  {% endif %}
  {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
        {% if sorted_datasets %}
          {% for dataset in sorted_datasets %}
            {% include projects.liquid project=dataset %}
          {% endfor %}
        {% endif %}
      </div>
    </div>
  {% else %}
    <div class="row row-cols-1 row-cols-md-3">
      {% if sorted_datasets %}
        {% for dataset in sorted_datasets %}
          {% include projects.liquid project=dataset %}
        {% endfor %}
      {% endif %}
    </div>
  {% endif %}
</div>

# Bibliography

<!-- _pages/publications.md -->
<div class="publications">
<p>*indicates joint first authorship</p>
{% bibliography %}

</div>