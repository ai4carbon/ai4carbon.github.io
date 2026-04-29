---
layout: home
title: home
permalink: /
page_title: "AI4Carbon: Machine Learning for Carbon Cycle Science"
page_subtitle: >
  A community effort
news: true # includes a list of news items
---

<style>
.home-intro {
  background: linear-gradient(135deg, rgba(52, 152, 219, 0.15) 0%, rgba(46, 204, 113, 0.15) 100%);
  border-radius: 12px;
  padding: 3rem;
  margin-bottom: 3rem;
  text-align: center;
}

.home-intro h2 {
  color: var(--global-theme-color);
  font-size: 2rem;
  margin-bottom: 1rem;
}

.home-intro p {
  font-size: 1.2rem;
  line-height: 1.7;
  color: var(--global-text-color);
}

.challenge-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 3rem 0;
}

.challenge-card {
  background: var(--global-card-bg-color);
  border: 2px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 2rem;
  transition: all 0.3s ease;
}

.challenge-card:hover {
  border-color: var(--global-theme-color);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  transform: translateY(-4px);
}

.challenge-card h3 {
  color: var(--global-theme-color);
  margin-top: 0;
  font-size: 1.4rem;
}

.challenge-card p {
  line-height: 1.6;
  margin-bottom: 0;
}

.highlight-box {
  background: rgba(52, 152, 219, 0.1);
  border-left: 5px solid var(--global-theme-color);
  padding: 1.5rem;
  border-radius: 8px;
  margin: 2rem 0;
  font-size: 1.1rem;
  line-height: 1.7;
}

.highlight-box strong {
  color: var(--global-theme-color);
}

.initiative-header {
  display: flex;
  align-items: center;
  gap: 2rem;
  margin: 2rem 0;
}

.initiative-header h2 {
  color: var(--global-theme-color);
  font-size: 2rem;
  margin: 0;
}

.cta-button {
  display: inline-block;
  background: var(--global-theme-color);
  color: white;
  padding: 1rem 2rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  margin: 1rem 1rem 0 0;
}

.cta-button:hover {
  opacity: 0.9;
  transform: scale(1.05);
  text-decoration: none;
}

.cta-secondary {
  background: transparent;
  border: 2px solid var(--global-theme-color);
  color: var(--global-theme-color);
}

.cta-secondary:hover {
  background: var(--global-theme-color);
  color: white;
}

.mailing-list-form {
  background: var(--global-card-bg-color);
  border: 2px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 2rem;
  max-width: 500px;
  margin: 2rem 0;
}

.mailing-list-form h3 {
  color: var(--global-theme-color);
  margin-top: 0;
}

.mailing-list-form form {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.mailing-list-form input[type="email"] {
  flex: 1;
  min-width: 200px;
  padding: 0.75rem;
  border: 1px solid var(--global-divider-color);
  border-radius: 6px;
  font-size: 1rem;
}

.mailing-list-form input[type="submit"] {
  padding: 0.75rem 1.5rem;
  background: var(--global-theme-color);
  color: white;
  border: none;
  border-radius: 6px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
}

.mailing-list-form input[type="submit"]:hover {
  opacity: 0.9;
  transform: scale(1.02);
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
  text-align: center;
}

.stat-item {
  padding: 1.5rem;
  background: rgba(0, 0, 0, 0.02);
  border-radius: 8px;
}

.stat-number {
  font-size: 2rem;
  font-weight: bold;
  color: var(--global-theme-color);
}

.stat-label {
  font-size: 0.9rem;
  color: var(--global-text-color);
  margin-top: 0.5rem;
}

.objectives-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.objective-item {
  padding: 1.5rem;
  background: rgba(0, 0, 0, 0.02);
  border-left: 4px solid var(--global-theme-color);
  border-radius: 8px;
}

.objective-item h4 {
  color: var(--global-theme-color);
  margin: 0 0 0.5rem 0;
}

.objective-item p {
  margin: 0;
  font-size: 0.95rem;
}
</style>

<div class="home-intro">
<h2>🌍 Advancing AI for Carbon Cycle Science</h2>
<p>The AI4Carbon Initiative is a community-driven effort to leverage cutting-edge machine learning for carbon cycle research, atmospheric transport modeling, and climate monitoring.</p>
</div>

---

## The Challenge

<p>Recent breakthroughs in artificial intelligence have transformed numerical weather prediction, with deep learning models like GraphCast and PanguWeather now outperforming operational forecasting systems. However, the carbon cycle—critical for understanding climate and supporting climate policy—remains largely untouched by these AI advances.</p>

<div class="challenge-section">
  <div class="challenge-card">
    <h3>🔬 The Transport Problem</h3>
    <p>Inverse modeling of the carbon cycle relies on atmospheric transport models operating at coarse resolutions, leading to systematic errors in retrieving surface carbon fluxes. Higher resolution models existing in research are computationally prohibitive for operational inverse modeling.</p>
  </div>

  <div class="challenge-card">
    <h3>📊 The Data Gap</h3>
    <p>Unlike weather prediction, there is no consensus benchmark dataset for training machine learning models on atmospheric CO₂ transport. This lack of standardization hinders progress and collaboration across the research community.</p>
  </div>

  <div class="challenge-card">
    <h3>🤝 The Opportunity</h3>
    <p>Machine learning can bridge the gap: trained on high-resolution model outputs, neural networks could learn to correct transport errors and accelerate inversions—supporting the WMO Global Greenhouse Gas Watch (G3W).</p>
  </div>
</div>

<div class="highlight-box">
💡 <strong>Our Vision:</strong> By bringing together the atmospheric transport modeling, inverse modeling, and machine learning communities, we can build AI-based CO₂ transport models that are operational, accurate, and trustworthy.
</div>

---

## Our Mission

<div class="objectives-list">
  <div class="objective-item">
    <h4>📈 Build Consensus</h4>
    <p>Establish benchmark datasets and evaluation frameworks for AI in carbon cycle research.</p>
  </div>

  <div class="objective-item">
    <h4>🔗 Foster Community</h4>
    <p>Connect researchers in atmospheric transport, inverse modeling, and machine learning through workshops and collaborative projects.</p>
  </div>

  <div class="objective-item">
    <h4>🎯 Drive Impact</h4>
    <p>Develop and validate AI methods that improve carbon flux estimates and support climate monitoring.</p>
  </div>

  <div class="objective-item">
    <h4>🌐 Enable Action</h4>
    <p>Provide tools and techniques that support policy-relevant carbon accounting and the Global Greenhouse Gas Watch.</p>
  </div>
</div>

---

## Stay Connected

<div class="mailing-list-form">
<h3>📧 Join Our Mailing List</h3>
<form action="https://mail.bgc-jena.mpg.de/mailman/subscribe/ai4carbon" method="POST">
  <input type="email" name="email" placeholder="your@email.com" required>
  <input type="submit" value="Subscribe">
</form>
<p style="font-size: 0.9rem; margin-top: 1rem;"><a href="https://mail.bgc-jena.mpg.de/mailman/listinfo/ai4carbon">View list details →</a></p>
</div>

---

## Upcoming Events

<p>Join us at upcoming workshops and conferences to learn more about AI for carbon cycle science:</p>

<a href="/workshops/" class="cta-button">📅 View All Workshops</a>
<a href="/resources/" class="cta-button cta-secondary">📚 Explore Resources</a>

<!-- ## Call for Interest -->

<!-- <style>  -->
<!-- .responsive-wrap iframe{ max-width: 100%;}  -->
<!-- </style> -->
<!-- <div class="responsive-wrap"> -->
<!-- this is the embed code provided by Google -->
<!-- <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScKQbUhrKQLhcrZGWb_mi350rhTWzjOpMYXgnjaTKrrigQqwQ/viewform?embedded=true" width="640" height="1032" frameborder="0" marginheight="0" marginwidth="0">Loading Google Form…</iframe> -->
<!-- Google embed ends -->
<!-- </div> -->

<!-- ## Schedule

- 14:00 - 9:15 / **Welcome and opening remarks** :raised_hands:

- 14:15 - 14:45 / <strong>Invited Talk</strong> <b><i>AI for Science</i></b>, TBA
- 14:45 - 15:15 / <strong>Invited Talk</strong> <b><i>Atmospheric Transport</i></b>, TBA
- 15:15 - 15:35 / <strong>Lightning Talk</strong> <b><i>AI for Carbon</i></b>, TBA
- 15:35 - 15:55 / <strong>Lightning Talk</strong> <b><i>AI for Carbon</i></b>, TBA

- 15:55 - 16:15 / **Coffee break** :coffee:

- 16:15 - 17:45 / <strong><u>Breakout Groups:</u> Towards a Community Effort on AI for Atmospheric Transport</strong> :mega:

  - Datasets
  - Evaluation
  - Methods

- 17:45 - 19:00 / **Closing Plenary Session** :wave:

- 19:00 / **Social Dinner** :spaghetti: -->

## Organizing Committee

<div class="row row-cols-2 projects pt-3 pb-3">
  {% include people_horizontal.liquid name="Vitus Benson" affiliation="Max Planck Institute for Biogeochemistry" url="https://vitusbenson.github.io/" img="assets/img/organizers/vitus_benson.png" %}
  {% include people_horizontal.liquid name="Nikhil Dadheech" affiliation="University of Washington" url="https://nd349.github.io/" img="assets/img/organizers/nikhil_dadheech.png" %}
  {% include people_horizontal.liquid name="Elena Fillola" affiliation="University of Bristol" url="https://research-information.bris.ac.uk/en/persons/elena-fillola-mayoral" img="assets/img/organizers/elena_fillola.png" %}
  {% include people_horizontal.liquid name="Tai-Long He" affiliation="University of Washington" url="https://tailonghe.github.io/" img="assets/img/organizers/tailong_he.png" %}
  {% include people_horizontal.liquid name="Yuming Jin" affiliation="NCAR" url="https://www.linkedin.com/in/yuming-jin-306a7b126" img="assets/img/organizers/yuming_jin.png" %}
  {% include people_horizontal.liquid name="Sam Upton" affiliation="Max Planck Institute for Biogeochemistry" url="https://www.bgc-jena.mpg.de/person/supton/4955530" img="assets/img/organizers/sam_upton.png" %}
</div>

## Advisory Board

<div class="row row-cols-2 projects pt-3 pb-3">
  {% include people_horizontal.liquid name="Anna Agusti-Panareda" affiliation="ECMWF & CAMS" url="https://www.ecmwf.int/en/about/who-we-are/staff-profiles/anna-agusti-panareda" img="assets/img/organizers/anna_agustipanareda.png" %}
  {% include people_horizontal.liquid name="Gianpaolo Balsamo" affiliation="Global Greenhouse Gas Watch (G3W) & WMO" url="https://wmo.int/profile/gianpaolo-balsamo" img="assets/img/organizers/gianpaolo_balsamo.png" %}
  {% include people_horizontal.liquid name="Ana Bastos" affiliation="Leipzig University" url="https://www.bgc-jena.mpg.de/person/abastos/4680491" img="assets/img/organizers/ana_bastos.png" %}
  {% include people_horizontal.liquid name="Frédéric Chevallier" affiliation="LSCE & CAMS" url="https://www.lsce.ipsl.fr/Phocea/Pisp/index.php?nom=frederic.chevallier" img="assets/img/organizers/frederic_chevallier.png" %}
  {% include people_horizontal.liquid name="Anna Michalak" affiliation="Carnegie" url="https://bse.carnegiescience.edu/dr-anna-michalak-0" img="assets/img/organizers/anna_michalak.png" %}
  {% include people_horizontal.liquid name="Wouter Peters" affiliation="Wageningen University" url="https://www.wur.nl/en/persons/wouter-peters.htm" img="assets/img/organizers/wouter_peters.png" %}
  {% include people_horizontal.liquid name="Markus Reichstein" affiliation="Max Planck Institute for Biogeochemistry" url="https://www.bgc-jena.mpg.de/en/reichstein.html" img="assets/img/organizers/markus_reichstein.png" %}
  {% include people_horizontal.liquid name="Britt Stephens" affiliation="NCAR" url="https://staff.ucar.edu/users/stephens" img="assets/img/organizers/britt_stephens.png" %}
  {% include people_horizontal.liquid name="Alex Turner" affiliation="University of Washington" url="https://alexjturner.github.io/index.html" img="assets/img/organizers/alex_turner.png" %}
</div>

## Contact

If you are interested in joining the collaborative effort, please reach out to vbenson (at) bgc-jena (dot) mpg (dot) de!
