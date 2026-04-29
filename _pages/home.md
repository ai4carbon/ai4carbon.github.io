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

.person-card {
  background: var(--global-card-bg-color);
  border: 2px solid var(--global-divider-color);
  border-radius: 12px;
  padding: 1.5rem;
  transition: all 0.3s ease;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.person-card:hover {
  border-color: var(--global-theme-color);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.12);
  transform: translateY(-4px);
}

.person-card img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid var(--global-theme-color);
  margin-bottom: 1rem;
}

.person-card h4 {
  color: var(--global-theme-color);
  margin: 0.5rem 0;
  font-size: 1.1rem;
}

.person-card p {
  margin: 0.25rem 0;
  font-size: 0.9rem;
  color: var(--global-text-color);
}

.person-card a {
  margin-top: 0.75rem;
  display: inline-block;
  color: var(--global-theme-color);
  font-size: 0.85rem;
  font-weight: bold;
}

.people-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  margin: 1.5rem 0;
}
</style>

<div class="home-intro">
<h2>🌍 Advancing AI for Carbon Cycle Science</h2>
<p>The AI4Carbon Initiative is a community-driven effort to leverage cutting-edge machine learning for understanding and monitoring carbon cycles. We bridge top-down atmospheric inversion approaches with bottom-up ecosystem modeling through AI, advancing both atmospheric transport science and carbon accounting.</p>
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

## The Challenge

<p>Artificial intelligence has revolutionized weather prediction and other scientific domains. Yet the carbon cycle—critical for understanding climate and supporting climate policy—remains largely untouched by these AI advances. AI4Carbon works to close this gap by leveraging machine learning across both atmospheric-based (top-down) and ecosystem-based (bottom-up) approaches to carbon science.</p>

<div class="challenge-section">
  <div class="challenge-card">
    <h3>🔬 The Top-Down Challenge</h3>
    <p>Atmospheric inverse modeling relies on coarse-resolution transport models, leading to systematic errors in retrieving surface carbon fluxes. Higher-resolution models exist in research but are computationally prohibitive for operational use.</p>
  </div>

  <div class="challenge-card">
    <h3>📊 The Data Gap</h3>
    <p>Unlike weather prediction, there is no consensus benchmark dataset for training machine learning models on atmospheric CO₂ transport. This lack of standardization hinders progress and collaboration across the research community.</p>
  </div>

  <div class="challenge-card">
    <h3>🤝 The Bottom-Up Complement</h3>
    <p>Ecosystem models and direct measurements provide valuable constraints, but integrating them with atmospheric observations remains challenging. AI can help unify these perspectives by learning patterns across scales and bridging gaps between different data sources.</p>
  </div>
</div>

<div class="highlight-box">
💡 <strong>Our Vision:</strong> By bringing together atmospheric scientists, ecosystem modelers, machine learning researchers, and policy makers, we can develop AI methods that unify top-down and bottom-up carbon cycle understanding—creating a new era of AI-assisted carbon science.
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
    <p>Connect researchers across top-down atmospheric science, bottom-up ecosystem modeling, and machine learning through workshops and collaborative projects.</p>
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

## Upcoming Events

<p>Join us at upcoming workshops and conferences to learn more about AI for carbon cycle science:</p>

<a href="/workshops/" class="cta-button">📅 View All Workshops</a>
<a href="/resources/" class="cta-button cta-secondary">📚 Explore Resources</a>

---

## Organizing Committee

<div class="people-grid">
  <div class="person-card">
    <img src="/assets/img/organizers/vitus_benson.png" alt="Vitus Benson">
    <h4>Vitus Benson</h4>
    <p><strong>Max Planck Institute for Biogeochemistry</strong></p>
    <a href="https://vitusbenson.github.io/" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/nikhil_dadheech.png" alt="Nikhil Dadheech">
    <h4>Nikhil Dadheech</h4>
    <p><strong>University of Washington</strong></p>
    <a href="https://nd349.github.io/" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/elena_fillola.png" alt="Elena Fillola">
    <h4>Elena Fillola</h4>
    <p><strong>University of Bristol</strong></p>
    <a href="https://research-information.bris.ac.uk/en/persons/elena-fillola-mayoral" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/tailong_he.png" alt="Tai-Long He">
    <h4>Tai-Long He</h4>
    <p><strong>University of Washington</strong></p>
    <a href="https://tailonghe.github.io/" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/yuming_jin.png" alt="Yuming Jin">
    <h4>Yuming Jin</h4>
    <p><strong>NCAR</strong></p>
    <a href="https://www.linkedin.com/in/yuming-jin-306a7b126" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/sam_upton.png" alt="Sam Upton">
    <h4>Sam Upton</h4>
    <p><strong>Max Planck Institute for Biogeochemistry</strong></p>
    <a href="https://www.bgc-jena.mpg.de/person/supton/4955530" target="_blank">Profile →</a>
  </div>
</div>

## Advisory Board

<div class="people-grid">
  <div class="person-card">
    <img src="/assets/img/organizers/anna_agustipanareda.png" alt="Anna Agusti-Panareda">
    <h4>Anna Agusti-Panareda</h4>
    <p><strong>ECMWF & CAMS</strong></p>
    <a href="https://www.ecmwf.int/en/about/who-we-are/staff-profiles/anna-agusti-panareda" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/gianpaolo_balsamo.png" alt="Gianpaolo Balsamo">
    <h4>Gianpaolo Balsamo</h4>
    <p><strong>Global Greenhouse Gas Watch (G3W) & WMO</strong></p>
    <a href="https://wmo.int/profile/gianpaolo-balsamo" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/ana_bastos.png" alt="Ana Bastos">
    <h4>Ana Bastos</h4>
    <p><strong>Leipzig University</strong></p>
    <a href="https://www.bgc-jena.mpg.de/person/abastos/4680491" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/frederic_chevallier.png" alt="Frédéric Chevallier">
    <h4>Frédéric Chevallier</h4>
    <p><strong>LSCE & CAMS</strong></p>
    <a href="https://www.lsce.ipsl.fr/Phocea/Pisp/index.php?nom=frederic.chevallier" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/anna_michalak.png" alt="Anna Michalak">
    <h4>Anna Michalak</h4>
    <p><strong>Carnegie</strong></p>
    <a href="https://bse.carnegiescience.edu/dr-anna-michalak-0" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/wouter_peters.png" alt="Wouter Peters">
    <h4>Wouter Peters</h4>
    <p><strong>Wageningen University</strong></p>
    <a href="https://www.wur.nl/en/persons/wouter-peters.htm" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/markus_reichstein.png" alt="Markus Reichstein">
    <h4>Markus Reichstein</h4>
    <p><strong>Max Planck Institute for Biogeochemistry</strong></p>
    <a href="https://www.bgc-jena.mpg.de/en/reichstein.html" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/britt_stephens.png" alt="Britt Stephens">
    <h4>Britt Stephens</h4>
    <p><strong>NCAR</strong></p>
    <a href="https://staff.ucar.edu/users/stephens" target="_blank">Profile →</a>
  </div>
  <div class="person-card">
    <img src="/assets/img/organizers/alex_turner.png" alt="Alex Turner">
    <h4>Alex Turner</h4>
    <p><strong>University of Washington</strong></p>
    <a href="https://alexjturner.github.io/index.html" target="_blank">Profile →</a>
  </div>
</div>

## Contact

If you are interested in joining the collaborative effort, please reach out to vbenson (at) bgc-jena (dot) mpg (dot) de!
