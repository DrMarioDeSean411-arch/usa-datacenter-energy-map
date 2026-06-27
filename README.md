# 🌍 Global Datacenters Intelligence Map

Interactive visualization of 45+ hyperscaler datacenters worldwide with 50-year energy and water projections (2024–2074).

## 🗺️ Live Map

**[Open the interactive map →](https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/index_hybrid.html)**

---

## ✨ Features

- **Dual-view mapping:** Toggle between global and USA detail views
- **Interactive timeline:** Drag to explore 2024–2074 projections
- **Facility details:** Click any marker for power, water, operator, and capacity data
- **Regional analysis:** Visualize energy distribution by continent and state
- **Growth projections:** 7.5% CAGR with facility-specific forecasts

---

## 📊 Data at a Glance

| Metric | 2024 | 2050 | 2074 |
|--------|------|------|------|
| **Power (GW)** | 81.8 | 204.5 | 427.3 |
| **Water (MGD)** | 30.3 | 68.4 | 118.8 |
| **Facilities** | 26 existing | 32 total | 45 total |

**Facilities by region:**
- North America: 13 existing + 8 predicted
- Europe: 6 existing + 2 predicted
- Asia-Pacific: 4 existing + 5 predicted
- Other: 3 existing + 4 predicted

---

## 🗂️ Repository Contents

| File | Purpose |
|------|---------|
| **index_hybrid.html** | Primary map with global + USA toggle (recommended) |
| **index.html** | USA detail view only |
| **index_global.html** | Global view only |
| **FORECAST_MODEL.md** | Technical methodology for 50-year projections |
| **facilities.geojson** | GIS data (coordinates, capacity, operators) |
| **energy_regional.csv** | Historical and projected power consumption |

---

## 🔬 Methodology

### Growth Model
- **Existing facilities:** 7.5% compound annual growth rate (CAGR)
- **New facilities:** Linear ramp to 2.5× capacity by 2074
- **Regional variation:** 6.9%–8.6% CAGR depending on region

### Data Sources
- Google 2024 Environmental Report
- AWS 2024 Sustainability Report
- Azure global infrastructure data

For complete technical details, see **FORECAST_MODEL.md**.

---

## 🎯 Use Cases

- **Research:** Academic studies on AI infrastructure and energy consumption
- **Policy:** Regulatory analysis of datacenter expansion
- **Business:** Strategic facility planning and competitive positioning
- **Education:** Teaching materials on cloud infrastructure and environmental impact

---

## 📖 Map Guide

### Global View
- Red, orange, yellow, cyan, pink, and tan clusters show regional distribution
- Marker size represents facility power capacity
- Click any marker for detailed metrics

### USA View
- 50 state labels with regional clustering (Pacific NW, California, Southwest, etc.)
- 13 existing + 8 predicted US datacenters
- Zoom in for facility-level detail

### Timeline Slider
- Drag left/right to move through 2024–2074
- Watch power and water consumption scale dynamically
- Predicted facilities appear on their opening year

---

## 📌 Citation

```bibtex
@misc{desean2026datacenters,
  author = {DeSean, Mario},
  title = {Global Datacenters Intelligence Map},
  year = {2026},
  url = {https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/},
  note = {Interactive visualization with 50-year projections}
}
```

Or in APA format:

```
DeSean, M. (2026). Global datacenters intelligence map. Retrieved from 
https://DrMarioDeSean411-arch.github.io/usa-datacenter-energy-map/
```

---

## 📧 Contact

**Dr. Mario Booker**  
Western Governors University  
mario.booker@wgu.edu

---

## 📄 License

This project is provided for research and educational purposes.

---

## 🔗 Related Links

- [AWS Sustainability Report 2024](https://sustainability.aboutamazon.com/)
- [Google Environmental Report 2024](https://environmental-report.withgoogle.com/)
- [Microsoft Datacenter Energy Dashboard](https://datacenters.microsoft.com/)

---

**Last updated:** June 2026  
**Data period:** 2024–2074 projections
