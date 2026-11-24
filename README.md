# CIVIC TRACE — Fatal Police Encounters in the United States (2013–2025)

An auditable, restraint-driven empirical analysis of recorded fatal police encounters across the United States (`2013–2025`, `n = 15,325`), paired with an isolated `2026` year-to-date snapshot (`n = 1,136`), official U.S. Census Bureau resident population denominators, and a 10-year (`2015–2024`) cross-source benchmark against *The Washington Post* Fatal Force database (`n = 10,430`).

## Repository Structure

```text
CIVIC-TRACE/
├── data/
│   ├── raw/
│   │   ├── mapping_police_violence.csv         # Frozen raw MPV source (SHA-256 verified)
│   │   ├── washington_post_fatal_force.csv     # Frozen raw WaPo Fatal Force benchmark (2015–2024)
│   │   └── census_population.csv               # Official U.S. Census Bureau PEP state denominators
│   └── processed/
│       ├── civic_trace_clean_2013_2025.csv     # Canonical primary analytical dataset (n = 15,325)
│       ├── civic_trace_ytd_2026_isolated.csv   # Isolated 2026 YTD snapshot (n = 1,136)
│       └── civic_trace.db                      # Indexed SQLite database (4 analytical tables)
├── documentation/
│   ├── executive_report.md                     # Full Phase 8 report answering RQ1–RQ5 & limitations
│   ├── methodology.md                          # Governance rules, build logs & SHA-256 checksums
│   ├── source_register.md                      # Provenance & integrity hashes for all raw inputs
│   └── variable_dictionary.md                  # Schema definitions & epistemic coding rules
├── tables/                                     # Reconciled analytical tables (table_01 – table_17)
├── figures/                                    # Static PNG charts & interactive Plotly HTML dashboards
├── notebook/                                   # Place CIVIC_TRACE.ipynb here for GitHub archival
├── README.md
└── requirements.txt
```

## Key Headline Findings (`2013–2025`, `n = 15,325`)

* **Historical Trajectory & Seasonality (RQ1):** Recorded fatalities averaged `1,178.8`/year (`+20.06` deaths/year OLS slope, `R² = 0.86`), peaking in `Aug` (`1,365`) and reaching a trough in `Sep` (`1,161`). Date-aligned `2026` YTD deaths (`1,136`) track `-1.47%` below the same `2025` window (`1,153`).
* **Demographics (RQ2):** Recorded victims had a median age of `35.0` years (`IQR = 28–46`) and were `93.91%` Male (`14,391`).
* **Geography & Per-Capita Rates (RQ3):** While California (`2,111`), Texas (`1,466`), and Florida (`1,079`) recorded the highest raw totals, New Mexico (`1.270`/100k) and Alaska (`1.106`/100k) recorded the highest population-adjusted rates against the `0.347`/100k U.S. mean.
* **Circumstances & Completeness (RQ4 & RQ5):** Gunshot force accounted for `91.97%` (`14,094`) of fatalities. Mean 11-field record completeness improved from `86.96%` (`2013`) to `92.66%` (`2025`), and encounters with recorded video footage averaged `96.70%` completeness vs. `86.64%` without footage.
* **Cross-Source Alignment (`2015–2024`):** On-duty fatal shootings in MPV (`10,714`) align within `97.3%` of Washington Post Fatal Force (`10,430`).

## Reproducibility

```bash
pip install -r requirements.txt
```
All analytical tables in `tables/`, figures in `figures/`, and SQLite tables in `data/processed/civic_trace.db` are generated deterministically (`np.random.seed(42)`) from the frozen raw CSVs in `data/raw/`.
