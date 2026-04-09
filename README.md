# Morocco WC2022 — Defensive Efficiency & Attacking Precision

**Quantifying the Blueprint: How Morocco Reached the 2022 World Cup Semifinals**

Using StatsBomb event and 360 data from FIFA World Cup 2022, this project analyses Morocco's
tournament run across all 7 matches through two complementary lenses: how their mid-block
defensive structure spatially suppressed opponent shot quality beyond what aggregate metrics
suggest, and whether their attacking output reflected genuine chance creation or clinical
finishing above expectation.

The project addresses a gap in existing Morocco WC2022 coverage — prior analyses (FIFA Technical
Study Group, MDPI, tactical blogs) describe defensive compactness qualitatively or via aggregate
stats, but none map opponent shot locations against StatsBomb xG values spatially to show *where*
Morocco forced opponents to shoot from and *what quality of chance* those positions produced.

## Analytical Questions

1. **Defensive structure → shot suppression:** What quality of chance did opponents generate
   against Morocco, and how did Morocco's spatial defensive positioning constrain opponent
   shooting locations and xG?
2. **Attacking efficiency vs. expectation:** Did Morocco's goals come from high-xG chances
   (structured attacking play) or low-xG chances (clinical finishing / set pieces)?
3. **Tournament progression:** How did Morocco's defensive and attacking profiles evolve across
   the group stage, knockout rounds, and semifinal?

## Current Progress

### Completed Sections
| Section | Description | Output |
|---|---|---|
| 1 | Setup, data ingestion, SQLite database | 25,971 events across 7 matches |
| 2 | Morocco matches overview | Match summary table, tournament timeline |
| 3a | Pressure & defensive intervention map | KDE heatmap (mplsoccer) — 1,945 defensive actions |
| 3b | Opponent shot quality map | Static scatter (mplsoccer) + interactive Plotly map with match/penalty filters |
| 3c | Individual defensive contributions | Stacked horizontal bar chart (Plotly) — top 10 defenders |

### Upcoming
| Section | Description |
|---|---|
| 3d | Defensive intensity over time (time-series by match period) |
| 4+ | Attacking efficiency vs. xG, tournament progression analysis |
| App | Streamlit interactive dashboard (second deliverable) |

## Data Source

StatsBomb Open Data — FIFA World Cup 2022
`competition_id=43` · `season_id=106` · 64 matches · 7 Morocco matches
[github.com/statsbomb/open-data](https://github.com/statsbomb/open-data)

## Tech Stack

| Tool | Purpose |
|---|---|
| `statsbombpy` | Data ingestion via StatsBomb Python SDK |
| `sqlite3` | Local relational database — all analysis reads from DB via `pd.read_sql()` |
| `pandas` 1.5.3 / `numpy` 1.24.3 | Data wrangling (pinned for `statsbombpy` compatibility) |
| `mplsoccer` | Pitch-based spatial visualizations (KDE heatmaps, shot maps) |
| `plotly` | Interactive charts with dropdown filters and hover tooltips |
| `seaborn` / `matplotlib` | Static charts and supporting plots |
| Jupyter Lab / VS Code | Analysis environment |

## Project Structure

morocco-wc22-analysis/
├── data/
│   ├── raw/                # StatsBomb JSON (gitignored)
│   └── processed/          # SQLite DB + cleaned data (gitignored)
├── notebooks/
│   └── 01_morocco_analysis.ipynb
├── reports/
│   └── figures/
│       ├── 3a_defensive_map.png
│       └── 3b_opponent_shot_map.png
├── src/                    # Helper modules (future)
├── REFERENCES.md           # Academic and analytical sources
├── requirements.txt
├── LICENSE
└── README.md

## References

See [REFERENCES.md](REFERENCES.md) for the full list of prior analyses, tactical reports,
and academic sources that informed this project's analytical framing.

## Status

🔄 Active development — April 2026