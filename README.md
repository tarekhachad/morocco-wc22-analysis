# Morocco WC2022 — Spatial Defensive Analysis

**Quantifying the Blueprint: How Morocco Reached the 2022 World Cup Semifinals**

Using StatsBomb event and 360 data from FIFA World Cup 2022, this project 
analyses Morocco's defensive spatial efficiency across 7 matches — examining 
how their mid-block structure suppressed opponent xG, the spatial footprint 
of Amrabat's pressing role, and whether their counter-attacking efficiency 
reflected genuine chance quality or clinical finishing above expectation.

## Data Source
StatsBomb Open Data — FIFA World Cup 2022  
`competition_id=43`, `season_id=106`  
[github.com/statsbomb/open-data](https://github.com/statsbomb/open-data)

## Tech Stack
| Tool | Purpose |
|---|---|
| `statsbombpy` | Data ingestion via StatsBomb SDK |
| `pandas` / `numpy` | Data wrangling and aggregation |
| `mplsoccer` | Pitch-based spatial visualisations |
| `plotly` | Interactive charts |
| `seaborn` / `matplotlib` | Static charts and heatmaps |
| `sqlite3` | Local database storage |
| `jupyterlab` | Analysis environment |

## Project Structure
\```
morocco-wc2022-analysis/
├── data/processed/     # Cleaned player/event DataFrames
├── notebooks/          # Analysis notebooks
├── reports/figures/    # Exported visualisations
└── src/                # Helper functions
\```

## Status
🔄 In progress — March 2026