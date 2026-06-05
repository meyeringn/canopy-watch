# 🌳 CanopyWatch — Urban Tree Equity Mapper

> *Visualizing the green gap — and the heat gap — across Philadelphia neighborhoods.*

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Data: Open](https://img.shields.io/badge/Data-Open%20Source-52b788)](https://opendataphilly.org)
[![Tool: Self-Contained](https://img.shields.io/badge/Tool-Single%20HTML-1a3a2a)](index.html)
[![Accessibility: WCAG 2.1](https://img.shields.io/badge/Accessibility-WCAG%202.1-blue)](https://www.w3.org/WAI/WCAG21/quickref/)

-----

## What Is CanopyWatch?

CanopyWatch is an open-source, browser-based data tool that maps urban tree canopy coverage against income, race, disability prevalence, and heat risk across Philadelphia’s 36 neighborhoods. It turns a complex environmental justice problem into something you can *see, compare, and act on* — in one HTML file, with no install required.

**The core argument:** Tree canopy is not a luxury amenity. It is climate infrastructure — and its inequitable distribution is a public health crisis that disproportionately harms Disabled people, low-income residents, and communities of color.

-----

## The Problem

Philadelphia’s citywide tree canopy averages ~20% — far below the 30% urban forestry benchmark. But that average conceals a 3:1 equity gap:

|Neighborhood Type                      |Canopy Coverage|Heat Premium|Disabled Pop.|
|---------------------------------------|---------------|------------|-------------|
|Affluent (e.g., Chestnut Hill)         |38–42%         |−3 to −4°F  |8–10%        |
|Middle-income                          |20–30%         |±0–2°F      |10–14%       |
|Low-income (e.g., Kensington, Fairhill)|3–8%           |+7 to +10°F |24–30%       |

The neighborhoods with the least shade are also the hottest, the poorest, and have the highest concentration of Disabled residents who face the greatest heat-health risk.

This is not coincidence. It is the geography of disinvestment.

-----

## Features

### 🗺️ Neighborhood Map

- Color-coded canopy grid for 36 Philadelphia neighborhoods
- Click any neighborhood to see: canopy coverage, equity score (0–100), heat premium, median income, % Disabled residents, CO₂ captured, stormwater managed
- Animated equity ring and priority intervention chips per neighborhood

### ⚖️ Equity Dashboard

- Ranked bar chart: all neighborhoods vs. 30% canopy goal
- Income vs. canopy scatter plot (dot size = disability prevalence; color = heat risk level)
- Top 3 “Critical Action” neighborhoods with equity framing
- Projected citywide impact of reaching the 30% goal

### 📊 Side-by-Side Compare

- Select any two neighborhoods for a 6-dimension comparison
- Metrics: canopy, equity score, heat premium, disabled residents, income, CO₂

### 📋 Policy Action Generator

- Select: neighborhood + intervention type + budget scale ($100K → $10M+)
- Generates: rationale, impact metrics, equity framing, and immediate next steps
- One-click copy for council testimony or grant applications
- 5 intervention types: Street Tree Planting, Pocket Park, Green Infrastructure, Shade at Transit, Cooling Corridors

### ♿ Disability & Heat Vulnerability

- Six illustrated reasons canopy is a disability justice issue
- Canopy deficit × Disabled population bubble chart
- Heat-Health Risk Index ranked for 16 most vulnerable neighborhoods

-----

## Two Standout Features

### 1. Policy Action Generator

Most data tools stop at *describing* the problem. CanopyWatch goes further: it generates ready-to-use policy language, scaled to a real budget, for a specific neighborhood intervention — suitable for City Council testimony, grant applications, or organizational advocacy. This bridges the gap between data and action.

### 2. Disability × Heat Vulnerability Layer

Urban tree canopy tools almost never center disability. CanopyWatch builds this in as a first-class data dimension, surfacing how mobility barriers, medication thermosensitivity, income constraints, and lack of AC access create compounding risk for Disabled Philadelphians in low-canopy neighborhoods. It frames tree planting not as a green amenity but as a health equity intervention.

-----

## Data Sources

All data is modeled from publicly available sources for planning and advocacy purposes. Not for regulatory use.

|Dataset                             |Source                                               |Use                                 |
|------------------------------------|-----------------------------------------------------|------------------------------------|
|Urban Tree Canopy Assessment        |Philadelphia Parks & Recreation / USDA Forest Service|Canopy % by neighborhood            |
|EnviroAtlas                         |U.S. EPA                                             |Heat surface temperature, stormwater|
|American Community Survey (ACS)     |U.S. Census Bureau                                   |Income, disability prevalence, race |
|Philadelphia Neighborhood Boundaries|OpenDataPhilly / PCPC                                |Geographic boundaries               |
|Urban Heat Island Effect            |NOAA / Climate Central                               |Heat premium estimates              |
|Tree Benefits Estimator             |i-Tree (USDA Forest Service)                         |CO₂ capture, stormwater management  |


> **Methodology note:** Equity Score is a composite index combining income (30%), canopy deficit relative to 30% goal (35%), heat premium (20%), and disability prevalence (15%). Heat-Health Risk Index weights canopy deficit (40%), heat premium (30%), and disability prevalence (30%).

-----

## Getting Started

### Use Immediately (No Install)

1. Download or clone this repo
1. Open `index.html` in any modern browser
1. No server, no API keys, no build step required

```bash
git clone https://github.com/meyeringn/canopy-watch.git
cd canopy-watch
open index.html   # macOS
# or: start index.html (Windows)
# or: xdg-open index.html (Linux)
```

### GitHub Pages (Recommended for Sharing)

```bash
# 1. Push to GitHub
git init
git add .
git commit -m "Initial commit: CanopyWatch MVP"
git remote add origin https://github.com/YOUR_USERNAME/canopy-watch.git
git push -u origin main

# 2. In your repo: Settings → Pages → Source: main branch / root
# Live at: https://YOUR_USERNAME.github.io/canopy-watch
```

-----

## Repository Structure

```
canopy-watch/
├── index.html          # Complete tool — single self-contained file
├── README.md           # This file
├── LICENSE             # MIT License
└── data/
    └── methodology.md  # Detailed data modeling methodology (see below)
```

-----

## Connection to Civic Tech Portfolio

CanopyWatch is part of a growing open-source civic tech portfolio at the intersection of environmental justice, disability equity, and data literacy:

|Project                             |Description                                                                            |Link                                                                                      |
|------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
|**SustAInable** (`sustainable-heat`)|XGBoost ML model predicting neighborhood heat illness risk by ZIP code                 |[github.com/meyeringn/sustainable-heat](https://github.com/meyeringn/sustainable-heat)    |
|**UpLift** (`uplift-transit`)       |Predictive maintenance for SEPTA elevators/escalators — disability equity focus        |[github.com/meyeringn/uplift-transit](https://github.com/meyeringn/uplift-transit)        |
|**DCVI**                            |Disability Climate Vulnerability Index — composite scoring with Philadelphia case study|[github.com/meyeringn/dcvi](https://github.com/meyeringn/dcvi)                            |
|**ClimateReady Score**              |Municipal climate resilience rubric with equity as non-negotiable dimension            |[github.com/meyeringn/climateready-score](https://github.com/meyeringn/climateready-score)|
|**CanopyWatch**                     |This tool — urban tree equity visualization and policy action generator                |You are here                                                                              |

These tools are designed to work together. CanopyWatch’s heat premium data feeds into SustAInable’s heat illness risk model. DCVI’s methodology informs CanopyWatch’s disability vulnerability index. UpLift addresses the mobility side of the same transit-equity problem.

-----

## Who This Is For

- **City planners and policymakers** looking for equity-centered data to prioritize tree planting investments
- **Community organizations and neighborhood advocates** who need data to make the case to electeds
- **Environmental justice researchers** studying the intersection of green space, income, race, and disability
- **Climate funders** (Climatebase, EPA, USFS, foundations) evaluating municipal resilience investments
- **Journalists and data communicators** covering Philadelphia’s urban environment

-----

## Accessibility

CanopyWatch is built with accessibility as a design requirement, not an afterthought:

- ✅ Skip navigation link
- ✅ Full keyboard navigation (Tab, Enter, Space) on all interactive elements
- ✅ ARIA roles and labels throughout (`role="grid"`, `aria-label`, `aria-live`)
- ✅ `aria-selected` on tab buttons
- ✅ Canvas charts include `role="img"` and `aria-label` descriptions
- ✅ Color is never the sole indicator (values shown numerically)
- ✅ Sufficient color contrast ratios (WCAG AA compliant)
- ✅ Identity-first disability language throughout

-----

## Contributing

Contributions welcome, especially:

- **Updated data**: More granular canopy coverage from PCPC or satellite imagery
- **Additional cities**: Adapting the model for other U.S. cities with canopy equity gaps
- **Spanish translation**: Philadelphia’s Latino communities are heavily represented in low-canopy neighborhoods
- **Screen reader testing**: Feedback from blind/low-vision users on canvas chart accessibility

Please open an issue before submitting a pull request.

-----

## License

MIT License. Use freely, credit appreciated.

-----

## Author

**Nico Meyering, MPA**
Philadelphia, PA

Civic technologist, transit equity advocate, and Disabled person building tools for communities — not customers.

- GitHub: [@meyeringn](https://github.com/meyeringn)
- LinkedIn: [linkedin.com/in/nicomeyering](https://linkedin.com/in/nicomeyering)
- Organizations: Net Impact Philadelphia · Transit Forward Philadelphia · Mayor’s Commission on People with Disabilities · Disability Pride Pennsylvania · Awesome Foundation (Disability Chapter)

-----

*“The neighborhoods that need shade the most are the ones that have the least of it. That’s not a tree problem. That’s a justice problem.”*
