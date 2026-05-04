# 🦴 Global Taphonomy Research Network
### An Interactive Map & Environmental Profile Dashboard for Human Forensic Decomposition Research Facilities

[![Updated](https://img.shields.io/badge/Updated-April%202026-00d4aa?style=flat-square)](https://github.com/)
[![Facilities](https://img.shields.io/badge/Human%20HTFs-14-00d4aa?style=flat-square)](https://github.com/)
[![Non-Human Sites](https://img.shields.io/badge/Non--Human%20Sites-4-d4a017?style=flat-square)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

## 📖 Overview

This project is a self-contained, single-file interactive web dashboard that aggregates publicly available information on all known active **human forensic taphonomy research facilities (HTFs)** — commonly known as "body farms" — worldwide, as well as select non-human animal proxy taphonomy sites.

These secure, outdoor research laboratories study how human remains decompose under varying environmental conditions. The data they generate supports:

- **Postmortem interval (PMI) estimation** for forensic casework
- **Victim identification** in mass disaster and missing persons cases
- **Law enforcement training** in crime scene recovery and clandestine grave detection
- **Forensic entomology, soil science, and environmental forensics research**
- **Taphonomic database development** across diverse climates and geographies

The dashboard is designed to serve:
1. **General public & potential donors** — find facilities, donation paperwork, and program contacts
2. **Researchers & academics** — access facility profiles, donor metrics, environmental data, and published literature links

---

## 🌍 Facilities Covered

### Human Taphonomy Facilities (HTFs) — 14 Operational

| ID | Facility | Location | Opened |
|----|----------|----------|--------|
| 0 | UTK Anthropological Research Facility (ARF) | Knoxville, Tennessee | 1981 |
| 1 | Forensic Osteology Research Station (FOREST) | Cullowhee, North Carolina | 2007 |
| 2 | Forensic Anthropology Research Facility (FARF/FACTS) | San Marcos, Texas | 2008 |
| 3 | Southeast Texas Applied Forensic Science Facility (STAFS) | Huntsville, Texas | ~2010 |
| 4 | Complex for Forensic Anthropology Research (CFAR) | Carbondale, Illinois | 2010 |
| 5 | Forensic Investigation Research Station (FIRS) | Grand Junction, Colorado | 2013 |
| 6 | Facility for Outdoor Research and Training (FORT) | Tampa, Florida | ~2016 |
| 7 | Forensic Research Outdoor Station (FROST) | Marquette, Michigan | ~2017 |
| 8 | Forensic Science Research and Training Laboratory (FSRTL) | Manassas, Virginia | 2024 |
| 9 | Forensic Taphonomy Education and Research Facility (FTERF) | Baton Rouge, Louisiana | ~2018 |
| 10 | Australian Facility for Taphonomic Experimental Research (AFTER) | NSW, Australia | 2016 |
| 11 | Secure Site for Research in Thanatology (REST[ES]/SSRT) | Bécancour, Canada | 2018 |
| 12 | Amsterdam Research Initiative for Sub-surface Taphonomy (ARISTA) | Amsterdam, Netherlands | 2018 |
| 13 | Buckingham Environmental Forensics Facility (BEFF/FGCU) | Florida | ~2016 |

### Non-Human / Animal Proxy Sites — 4
> Shown as **▲ triangles** on the map. These use pig or other animal models and are valuable complements but cannot fully replicate human-specific taphonomic factors.

- Ticino-LEAFs (LABANOF) — Lombardy, Italy *(first Italian forensic taphonomy facility, 2009)*
- Keele University Forensic Taphonomy Site — Staffordshire, UK
- TRACES, University of Central Lancashire — Lancashire, UK
- Western Illinois University Taphonomic Research Sites — Macomb, Illinois

---

## ✨ Features

### 🗺 Interactive Map
- **Leaflet.js** powered global map with full zoom, pan, and click interactions
- **Color-coded markers** by region (● circles = human HTFs, ▲ triangles = non-human sites)
- **4 base layers**: Street, Satellite (Esri), Terrain (OpenTopoMap), Dark (CartoDB)
- **5 weather overlays**: Temperature, Precipitation, Cloud Cover, Wind, Atmospheric Pressure (OpenWeatherMap API)
- **USDA Soil overlay** (WMS tile layer from USDA Soil Data Mart)
- **Collapsible sidebar** with facility list, search, and regional filter chips
- **Toggleable map legend** with symbol key for both facility types

### 📌 Facility Side Panel (Accordion Layout)
Each facility opens a collapsible accordion panel with:
- 📍 Location, opened date, size
- 👤 Current director and full leadership history
- 🔬 Research focus and key studies
- 🤝 Donor program metrics, links, and eligibility info
- 🪨 **Soil Profile** — USDA soil series, texture, drainage, pH, organic matter, USDA order, taphonomic interpretation, live USDA data fetch button, SoilWeb and Web Soil Survey direct links
- 🌡 **Climate** — Köppen classification, USDA hardiness zone, annual temperature and precipitation, 12-month sparkline charts for temp and precipitation, Open-Meteo and NOAA links
- 🌿 **Vegetation** — Ecological system classification, NLCD land cover class, canopy coverage, dominant species tags, NLCD Viewer and USDA PLANTS links
- 📞 Contact and official website

### 📋 Full Profile Modal
Extended facility cards with all data including:
- Facility identity, coordinates, and type
- Complete leadership history
- Full research focus and unique aspects
- Facility infrastructure and climate
- Donor program details with eligibility and donation links
- **Facility-specific bonus cards** (e.g., FACTS includes Freeman Ranch, TXSTDSC demographics, Operation Identification/OpID, workshop accreditation, and research access protocols)

### 📂 Directory & About
- Full facility cards in a responsive grid
- Clearly separated human HTF and non-human proxy sections
- Network growth timeline (1981–2024)
- Ethics and access notice

### ⬇ Data Export
- **CSV download** of all 14 human HTF records (name, university, coordinates, climate, contacts, donor URL)

---

## 🛠 Tech Stack

| Layer | Technology | Cost |
|-------|-----------|------|
| Frontend | HTML5 / CSS3 / Vanilla JavaScript | Free |
| Mapping | [Leaflet.js](https://leafletjs.com/) v1.9.4 | Free |
| Base tiles | OpenStreetMap, Esri, OpenTopoMap, CartoDB | Free |
| Weather overlays | [OpenWeatherMap API](https://openweathermap.org/api) | Free tier |
| Soil overlay | [USDA Soil Data Mart WMS](https://SDMDataAccess.sc.egov.usda.gov/) | Free |
| Live soil data | [USDA Soil Data Access REST API](https://SDMDataAccess.sc.egov.usda.gov/) | Free |
| Soil maps | [UC Davis SoilWeb](https://casoilresource.lawr.ucdavis.edu/gmap/) | Free |
| Climate data | [Open-Meteo](https://open-meteo.com/) / [NOAA](https://www.noaa.gov/climate) | Free |
| Vegetation data | [USDA PLANTS](https://plants.usda.gov/) / [NLCD Viewer](https://www.mrlc.gov/) | Free |
| Hosting | [Netlify](https://netlify.com) (recommended) | Free tier |

---

## 🚀 Getting Started

### Run Locally (Instant)
1. Download `index.html`
2. Double-click to open in any modern browser (Chrome, Firefox, Edge, Safari)
3. The map loads immediately — no server required

---

## 📁 Project Structure

```
taphonomy-network/
│
├── index.html              # Complete self-contained application
│                           # (HTML + CSS + JavaScript in one file)
│
├── README.md               # This file
│
└── /docs                   # (Optional future)
    ├── CONTRIBUTING.md
    ├── DATA_SOURCES.md
    └── CHANGELOG.md
```

> **Note:** The entire application is intentionally a single `index.html` file for portability, simplicity of deployment on GitHub Pages or Netlify, and ease of sharing.

---

## 📊 Data Sources & Citations

All facility data is compiled from publicly available sources including:

- **Official facility websites** (UTK FAC, FACTS, STAFS/IFRTI, NMU FROST, etc.)
- **Peer-reviewed literature**, including:
  - Gocha, T.P., Mavroudas, S.R., & Wescott, D.J. (2022). The Texas State Donated Skeletal Collection at the Forensic Anthropology Center at Texas State. *Forensic Sciences*, 2, 7–19. https://doi.org/10.3390/forensicsci2010002
  - Oostra, R.J. et al. (2020). ARISTA: First European human taphonomy facility. *Forensic Science International*.
  - Haglund, W.D. & Sorg, M.H. (1997). *Forensic Taphonomy*. CRC Press.
  - Carter, D.O. & Tibbett, M. (2008). *Soil Analysis in Forensic Taphonomy*. CRC Press.
  - Pokines, J.T. & Symes, S.A. (2014). *Manual of Forensic Taphonomy*. CRC Press.
- **USDA NRCS SSURGO** — soil series and classification data
- **Köppen-Geiger climate classification** (Peel et al., 2007; updated 2023)
- **NOAA NCEI 1991–2020 Climate Normals**
- **USDA NLCD (National Land Cover Database)**

---

## 🔮 Roadmap

### Public Dashboard (Current)
- [x] Interactive global map with facility markers
- [x] Side panel with soil, climate, and vegetation profiles
- [x] Live USDA soil data fetching
- [x] Weather and soil map overlays
- [x] CSV export
- [x] Non-human proxy facility distinction


### Future Enhancements
- [ ] NOAA historical weather lookup per facility
- [ ] NASA GIBS satellite imagery viewer
- [ ] Facility comparison tool (side-by-side)
- [ ] Published research / theses / dissertations linked per facility
- [ ] Mobile-optimized layout improvements
- [ ] Netlify deployment with environment variables for API key security

---

## ⚖ Ethics & Legal Notice

> **All facilities listed are secure, fenced, and closed to the public.**
> Visits are by appointment only for qualified researchers and law enforcement personnel.
> This dashboard presents publicly available information for **research and educational purposes only.**
> This project is **not affiliated with any facility listed.**

All body donation programs operate under strict ethical oversight, informed consent protocols, and applicable legal frameworks (e.g., the Uniform Anatomical Gift Act in the US).

---

## 📄 License

This project is released under the [MIT License](LICENSE). You are free to use, modify, and distribute it with attribution.

---

## 🙏 Acknowledgments

- All facilities and their donor programs, faculty, and staff
- The donors and their families whose gift makes forensic science possible
- [Leaflet.js](https://leafletjs.com/) — open-source mapping
- [OpenStreetMap contributors](https://www.openstreetmap.org/) — map tiles
- USDA NRCS — public soil data APIs
- UC Davis SoilWeb — soil mapping tools
- Open-Meteo — open-source climate data

---

*Built for forensic science education, research, and the advancement of human identification.*
*Last updated: April 2026*
