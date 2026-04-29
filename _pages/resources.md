---
layout: page
permalink: /resources/
title: resources
nav: true
nav_order: 2
---

<style>
.resources-intro {
  background: linear-gradient(135deg, rgba(52, 152, 219, 0.1) 0%, rgba(46, 204, 113, 0.1) 100%);
  border-left: 5px solid var(--global-theme-color);
  border-radius: 8px;
  padding: 2rem;
  margin-bottom: 3rem;
  font-size: 1.1rem;
  line-height: 1.7;
}

.resources-intro h2 {
  margin-top: 0;
  color: var(--global-theme-color);
  font-size: 1.6rem;
}

.section-header {
  color: var(--global-theme-color);
  font-size: 1.8rem;
  margin: 2rem 0 1.5rem 0;
  border-bottom: 3px solid var(--global-theme-color);
  padding-bottom: 0.5rem;
}

.datasets-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0 3rem 0;
}

.dataset-card {
  background: var(--global-card-bg-color);
  border: 2px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
}

.dataset-card:hover {
  border-color: var(--global-theme-color);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  transform: translateY(-4px);
}

.dataset-card img {
  max-height: 150px;
  object-fit: contain;
  margin-bottom: 1rem;
  border-radius: 8px;
}

.dataset-card h3 {
  color: var(--global-theme-color);
  margin: 0 0 0.5rem 0;
  font-size: 1.4rem;
}

.dataset-card p {
  flex-grow: 1;
  margin-bottom: 1rem;
  line-height: 1.6;
}

.dataset-card .badge {
  display: inline-block;
  background: var(--global-theme-color);
  color: white;
  padding: 0.4rem 0.8rem;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.dataset-links {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.dataset-links a {
  display: inline-block;
  padding: 0.6rem 1rem;
  background: var(--global-theme-color);
  color: white;
  text-decoration: none;
  border-radius: 6px;
  font-size: 0.9rem;
  font-weight: bold;
  transition: all 0.3s ease;
}

.dataset-links a:hover {
  opacity: 0.9;
  transform: scale(1.05);
  text-decoration: none;
}

.bibliography-section {
  background: var(--global-card-bg-color);
  border: 2px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 2rem;
  margin: 2rem 0;
}

.bibliography-section .publications {
  margin: 0;
}

.bib-note {
  background: rgba(52, 152, 219, 0.1);
  border-left: 4px solid var(--global-theme-color);
  padding: 1rem;
  border-radius: 6px;
  font-style: italic;
  color: var(--global-text-color);
  margin-bottom: 1.5rem;
}

.resource-item {
  background: rgba(0, 0, 0, 0.02);
  padding: 1.5rem;
  border-radius: 8px;
  border-left: 4px solid var(--global-theme-color);
  margin-bottom: 1rem;
}

.resource-item h4 {
  color: var(--global-theme-color);
  margin: 0 0 0.5rem 0;
}

.resource-item p {
  margin: 0;
  font-size: 0.95rem;
}

/* Bibliography category tags */
.publications {
  position: relative;
}

.publications li {
  padding-left: 1rem;
  list-style-position: inside;
}

.publications li::before {
  content: "";
  display: block;
  height: 100%;
  width: 0;
  position: absolute;
  left: 0;
  top: 0;
}

.pub-category {
  display: inline-block;
  padding: 0.3rem 0.8rem;
  border-radius: 12px;
  font-size: 0.75rem;
  font-weight: bold;
  color: white;
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
}

.pub-machine-learning {
  background: #3498db; /* Blue */
}

.pub-transport {
  background: #e74c3c; /* Red */
}

.pub-inversion {
  background: #9b59b6; /* Purple */
}

.pub-ecosystem {
  background: #27ae60; /* Green */
}

.pub-monitoring {
  background: #f39c12; /* Orange */
}

.pub-benchmark {
  background: #1abc9c; /* Turquoise */
}

.pub-methods {
  background: #34495e; /* Dark gray */
}

.pub-review {
  background: #16a085; /* Dark turquoise */
}
</style>

<div class="resources-intro">
<h2>🔬 Resources & Tools</h2>
<p>A curated collection of datasets, benchmarks, and publications from the AI4Carbon Initiative and the broader research community working on machine learning for carbon cycle science.</p>
</div>

---

<h2 class="section-header">📊 Datasets & Benchmarks</h2>

<p>Explore our collection of open-source datasets and benchmarks designed to accelerate machine learning research in atmospheric transport and carbon cycle modeling.</p>

<div class="datasets-grid">
  {% if site.datasets %}
    {% assign sorted_datasets = site.datasets | sort: "importance" %}
    {% for dataset in sorted_datasets %}
    <div class="dataset-card">
      {% if dataset.img %}
        <img src="/{{ dataset.img }}" alt="{{ dataset.title }}">
      {% endif %}
      <h3>{{ dataset.title }}</h3>
      <p><strong>{{ dataset.description }}</strong></p>
      <div class="badge">{{ dataset.category | default: "Dataset" }}</div>
      <div class="dataset-links">
        <a href="{{ dataset.url | default: '#' }}">Learn More</a>
      </div>
    </div>
    {% endfor %}
  {% endif %}
</div>

---

<h2 class="section-header">📚 Publications</h2>

<p>Recent and seminal publications on machine learning for carbon cycle science, atmospheric transport modeling, and inverse modeling techniques. Publications are tagged by topic:</p>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 0.5rem; margin-bottom: 2rem;">
  <div><span class="pub-category pub-machine-learning">Machine Learning</span></div>
  <div><span class="pub-category pub-transport">Atmospheric Transport</span></div>
  <div><span class="pub-category pub-inversion">Inversion</span></div>
  <div><span class="pub-category pub-ecosystem">Ecosystem</span></div>
  <div><span class="pub-category pub-monitoring">Monitoring</span></div>
  <div><span class="pub-category pub-benchmark">Benchmark</span></div>
  <div><span class="pub-category pub-methods">Methods</span></div>
  <div><span class="pub-category pub-review">Review</span></div>
</div>

<div class="bibliography-section">
<div class="bib-note">
<strong>*</strong> indicates joint first authorship
</div>
<div class="publications">
{% bibliography %}
</div>
</div>

---

<h2 class="section-header">🔗 Related Resources</h2>

<div class="resource-item">
<h4>📖 Global Greenhouse Gas Watch (G3W)</h4>
<p>WMO initiative to establish a comprehensive, integrated and user-focused global system for monitoring greenhouse gases and supporting climate action. <a href="https://public.wmo.int/en/our-mandate/climate/global-greenhouse-gas-watch" target="_blank">Learn more →</a></p>
</div>

<div class="resource-item">
<h4>💻 Join the Community</h4>
<p>Subscribe to our <a href="https://mail.bgc-jena.mpg.de/mailman/listinfo/ai4carbon">mailing list</a> to stay updated on new datasets, publications, and community initiatives.</p>
</div>