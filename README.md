# Capstone-messilovers

**Organization:** [itd-messilovers](https://github.com/itd-messilovers)  
**Course:** TI2006B – Fall 2026  
**Team Capstone home** for Messi Lovers

License: Original educational content adapted from the TI2006B course materials is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). Code, third-party datasets, APIs, trademarks, and quoted material retain their own licenses and terms.

## Project question

> Using public Pokémon species, type, and base-stat tables, which Pokémon types show the strongest average total base stats, and how should a beginner analytics team communicate that finding without overstating Pokémon GO competitive claims?

## Intended audience

Capstone teammates, course reviewers, and classmates who need a reproducible first analysis they can clone, run, and extend.

## Data source

Public community-maintained Pokédex CSV tables from [`veekun/pokedex`](https://github.com/veekun/pokedex) (species, types, and base stats). This is **not** Pokémon GO player telemetry, account data, location history, encounters, captures, or battle logs.

## Expected output

- A tidy joined analysis table from the public source CSVs
- Interactive Plotly charts (base-stat distribution, top totals, type counts, weight vs. total stats)
- Documented limitations so reviewers know what the charts do and do not support

## Current limitation

The first notebook is descriptive and teaching-oriented. It does not model Pokémon GO CP caps, move sets, meta tiers, or official tournament legality. Results must not be treated as a battle ranking or event registration recommendation.

## How to start

```bash
git clone https://github.com/itd-messilovers/Capstone-messilovers.git
cd Capstone-messilovers
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

Open and run [`notebooks/01-pokemon-go-analysis.ipynb`](notebooks/01-pokemon-go-analysis.ipynb) from top to bottom. Read [`notebooks/README.md`](notebooks/README.md) and [`data/README.md`](data/README.md) before interpreting the charts.

## Persistent repository structure

```text
.
├── .github/workflows/       # automated notebook checks
├── data/
│   ├── raw/                 # source snapshots when permitted
│   ├── processed/           # reproducible derived tables
│   └── README.md            # provenance and limitations
├── notebooks/               # exploratory analysis
├── reports/                 # figures and written findings
├── src/                     # reusable Python code
├── assignments/             # later activity evidence
├── requirements.txt
├── .gitignore
└── README.md
```

## Organization and access

- Organization: https://github.com/itd-messilovers
- Capstone repository: https://github.com/itd-messilovers/Capstone-messilovers
- Members and permissions are managed in the organization People settings with least-privilege access for contributors and maintainers.

## Working agreement

- Make one focused commit per meaningful change.
- Do not commit passwords, API keys, private student data, or unlicensed company data.
- Keep notebooks runnable from the repository root.
- Put provenance and limitations in Markdown, not only in code cells.

## Reflection

This repository would be hard for another student to use if the project question, data source, and start steps were missing, or if folders mixed raw data, notebooks, and reports without labels. We prevent that by keeping a clear README, the standard TI2006B folder layout, data notes, and a runnable first notebook with documented limitations.

## Class repository

Course materials and templates live in the class repository: https://github.com/tec-research/ti2006b
