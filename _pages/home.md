---
layout: home
title: home
permalink: /
page_title: "AI4Carbon: Machine Learning meets Atmospheric Transport"
page_subtitle: >
  A side event at <a href="https://www.icdc11.com/">ICDC 11</a>,
  31 July 2024, Manaus (Brazil) & Online
news: true # includes a list of news items
---

## Aims and scope

In 2023, AI has enabled a step-change in Medium-Range Numerical Weather Prediction skill. The large deep neural networks GraphCast and PanguWeather, trained to emulate the climate reanalysis dataset ERA-5, outperform the state-of-the-art HRES forecast at ECMWF, with significant margin.

Conversely, in the realm of inverse modeling of the Carbon Cycle—a process integral to deducing surface fluxes from atmospheric concentrations—challenges persist due to the employment of relatively coarse-resolution transport models. These models are hindered by inherent transport errors, attributed to limitations such as imprecise sub-grid-scale parameterizations and numerical discrepancies spawned by partial differential equation (PDE) solvers operating at diminished resolutions. The conventional approach of enhancing model fidelity through increased resolution in inverse modeling is hampered by prohibitive computational demands.

In light of these constraints, an alternative proposition emerges, advocating for the strategic application of artificial intelligence to ameliorate model accuracy even at lower resolutions. This innovative approach entails the training of an AI system using outputs from high-resolution transport models. Through this training process, the AI is envisioned to acquire the capability to autonomously identify and rectify the erroneous parameterizations and numerical inaccuracies inherent in lower-resolution models, thereby offering a promising avenue to circumvent computational limitations while elevating model precision.
Yet, in contrast to NWP, which has ERA-5, there is currently no consensus on a good training dataset for CO2 transport emulation.

The **AI4Carbon side event at ICDC11** is a community effort aiming to alleviate this bottleneck and build a benchmark dataset as well as a thorough evaluation framework. Since the endeavor is broad, it requires collaboration from the experienced transport and inverse modeling community as well as machine learning researchers. Together we can achieve AI-based CO2 transport, thereby supporting the Global Greenhouse Gas Watch (G3W) of WMO.

## Schedule

| Time  | What?                                                                       | Who?      |
| ----- | --------------------------------------------------------------------------- | --------- |
| 14:00 | Welcome                                                                     | Conveners |
| 14:15 | Invited Talk: AI for Science                                                | TBA       |
| 14:45 | Invited Talk: Atmospheric Transport                                         | TBA       |
| 15:15 | Lightning Talk                                                              | TBA       |
| 15:35 | Lightning Talk                                                              | TBA       |
| 16:00 | Coffee Break                                                                |           |
| 16:15 | Breakout Groups: Towards a Community Effort on AI for Atmospheric Transport |           |
| 17:45 | Plenary Session                                                             | Conveners |
| 19:00 | Closing                                                                     |           |

## Organizers

<div class="row row-cols-2 projects pt-3 pb-3">
  {% include people_horizontal.liquid name="Vitus Benson" affiliation="ELLIS Unit Jena" url="https://vitusbenson.github.io/" img="assets/img/organizers/vitus_benson.png" %}
  {% include people_horizontal.liquid name="Sam Upton" affiliation="Max Planck Institute for Biogeochemistry" url="https://www.bgc-jena.mpg.de/person/supton/4955530" img="assets/img/organizers/sam_upton.png" %}
  {% include people_horizontal.liquid name="Markus Reichstein" affiliation="Max Planck Institute for Biogeochemistry" url="https://www.bgc-jena.mpg.de/en/reichstein.html" img="assets/img/organizers/markus_reichstein.png" %}
  {% include people_horizontal.liquid name="Gianpaolo Balsamo" affiliation="Global Greenhouse Gas Watch (G3W) / World Meteorological Organization" url="https://www.cvernade.com/" img="assets/img/organizers/gianpaolo_balsamo.png" %}

</div>
