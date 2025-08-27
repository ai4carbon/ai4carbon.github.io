---
layout: page
title: CarbonBench
description: Benchmark dataset for Eulerian atmospheric transport models
img: assets/img/datasets/carbonbench_logo_small.png
importance: 1
---

![CarbonBench](/assets/img/datasets/carbonbench_logo.png)


# CarbonBench Dataset

The **CarbonBench** dataset is a benchmark for machine learning emulators of atmospheric CO₂ tracer transport. It was introduced in  
**Benson et al. (2024): [Atmospheric Transport Modeling of CO₂ with Neural Networks](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2024MS004655)**.

---

## GitHub Repository

<div class="github-card">
  <div class="github-header">
    <i class="fa-brands fa-github"></i>
    <a href="https://github.com/vitusbenson/carbonbench" target="_blank">
      <strong>vitusbenson/carbonbench</strong>
    </a>
  </div>
  <div class="github-description">
    <p>Official implementation and tools for the CarbonBench dataset - a benchmark for machine learning emulators of atmospheric CO₂ tracer transport.</p>
  </div>
  <div class="github-stats">
    <span class="stat">
      <i class="fa-solid fa-star"></i> 
      <span class="stat-text">Stars</span>
    </span>
    <span class="stat">
      <i class="fa-solid fa-code-fork"></i>
      <span class="stat-text">Forks</span>
    </span>
    <span class="stat">
      <i class="fa-solid fa-circle-dot"></i>
      <span class="stat-text">Python</span>
    </span>
  </div>
  <div class="github-links">
    <a href="https://github.com/vitusbenson/carbonbench" class="btn btn-outline-primary btn-sm" target="_blank">
      <i class="fa-brands fa-github"></i> View on GitHub
    </a>
    <a href="https://github.com/vitusbenson/carbonbench/archive/refs/heads/main.zip" class="btn btn-outline-secondary btn-sm" target="_blank">
      <i class="fa-solid fa-download"></i> Download
    </a>
  </div>
</div>

<style>
.github-card {
  border: 1px solid #d1d5da;
  border-radius: 6px;
  padding: 16px;
  margin: 20px 0;
  background-color: #fafbfc;
}

.github-header {
  margin-bottom: 8px;
}

.github-header i {
  margin-right: 8px;
  font-size: 1.2em;
}

.github-header a {
  text-decoration: none;
  color: #0366d6;
}

.github-header a:hover {
  text-decoration: underline;
}

.github-description {
  margin-bottom: 12px;
  color: #586069;
}

.github-stats {
  display: flex;
  gap: 16px;
  margin-bottom: 12px;
  font-size: 0.9em;
  color: #586069;
}

.stat {
  display: flex;
  align-items: center;
  gap: 4px;
}

.github-links {
  display: flex;
  gap: 8px;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  padding: 6px 12px;
  border-radius: 4px;
  text-decoration: none;
  font-size: 0.875em;
  transition: all 0.2s;
}

.btn-outline-primary {
  color: #0366d6;
  border: 1px solid #0366d6;
  background-color: transparent;
}

.btn-outline-primary:hover {
  background-color: #0366d6;
  color: white;
}

.btn-outline-secondary {
  color: #586069;
  border: 1px solid #d1d5da;
  background-color: transparent;
}

.btn-outline-secondary:hover {
  background-color: #f6f8fa;
}
</style>

---

## Dataset Contents

The dataset contains 3D CO₂ concentrations together with meteorological drivers and flux fields.  
All variables are provided as **Zarr arrays** chunked per timestep.

| Variable         | Description                                   | Units                         |
|------------------|-----------------------------------------------|-------------------------------|
| `co2massmix`     | CO₂ mass mixing ratio                         | 10⁻⁶ kgCO₂ / kgDryAir         |
| `airmass`        | Dry air mass                                  | Pg dry air                    |
| `gph_bottom`     | Geopotential height at lower level            | km                            |
| `gph_top`        | Geopotential height at upper level            | km                            |
| `p_bottom`       | Pressure at lower level                       | hPa                           |
| `p_top`          | Pressure at upper level                       | hPa                           |
| `q`              | Specific humidity                             | kg/kg                         |
| `t`              | Air temperature                               | K                             |
| `u`              | Zonal (eastward) wind speed                   | m/s                           |
| `v`              | Meridional (northward) wind speed             | m/s                           |
| `co2flux_anthro` | Anthropogenic surface CO₂ flux                | kg CO₂ m⁻² s⁻¹                |
| `co2flux_land`   | Land biosphere surface CO₂ flux               | kg CO₂ m⁻² s⁻¹                |
| `co2flux_ocean`  | Ocean surface CO₂ flux                        | kg CO₂ m⁻² s⁻¹                |
| `blh`            | Planetary boundary layer thickness            | m                             |
| `tisr`           | Incoming solar radiation                      | J m⁻²                         |
| `cell_area`      | Surface grid-cell area                        | m²                            |
| `orography`      | Surface geopotential                          | m²/s²                         |

**Output variable:**  
- `co2massmix` at the next timestep (same unit as input)

---

## Baseline Model Results

Performance of the baseline emulators trained on CarbonBench:

| Model                | Parameters (M) | Decorrelation Time | R²    | RMSE |
|----------------------|----------------|--------------------|-------|------|
| UNet               | 9.6            | >90                | 0.98  | 0.52 |
| GraphCast        | 5.2            | >90                | 0.96  | 0.86 |
| SFNO            | 35.7           | >90                | 0.98  | 0.58 |
| SwinTransformer   | 37.9           | >90                | 0.99  | 0.34 |


---

## Downloading & Preparing the Dataset

You can build the dataset locally using the **CarbonBench** tools:

```bash
# Clone the repo
git clone https://github.com/vitusbenson/carbonbench.git
git clone https://github.com/vitusbenson/neural_transport.git
cd carbonbench

# Install requirements (including neural_transport)
pip install -e ../neural_transport

# Create CarbonTracker-based dataset (example LowRes)
python data/create_carbontracker_dataset.py \
  --save_dir /path/to/data \
  --gridname "latlon5.625" \
  --vertical_levels "l10" \
  --freq "6h"

# Create ObsPack evaluation dataset
python data/create_obspack_dataset.py \
  --save_dir /path/to/data \
  --freq "3h"
```



## Citation

```
@article{benson2024neuraltransport,
  title = {Atmospheric Transport Modeling of CO2 with Neural Networks},
  author = {Vitus Benson, Ana Bastos, Christian Reimers, Alexander J. Winkler,
 Fanny Yang and Markus Reichstein},
  eprint={2408.11032},
  archivePrefix={arXiv},
  primaryClass={cs.LG},
  url={https://arxiv.org/abs/2408.11032}, 
}
```