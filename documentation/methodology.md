# CIVIC TRACE — Methodology & Build Log

## 6. Canonical Dataset Build Verification Log (Populated in Step 20)

- **Build & Latest Sync Timestamp (UTC):** `2026-11-24 20:07:58 UTC`
- **Frozen Raw Input Verified:** `/content/CIVIC-TRACE/data/raw/mapping_police_violence.csv` (`SHA-256`: `12319e0c4693d0e3c6ded50ebfa3708075db6aaf84b273ec758253f405a7ecf1`)
- **Canonical Primary Dataset:** `/content/CIVIC-TRACE/data/processed/civic_trace_clean_2013_2025.csv`
  - **Dimensions:** `15,325` rows × `87` columns (`2013–2025` complete calendar years)
  - **File Size (Bytes):** `20,259,032`
  - **SHA-256 Checksum:** `2e29e671fdd32db069aa5fce0e7aee61f417322472288c4776fb969c1f7795a7`
- **Isolated 2026 YTD Snapshot:** `/content/CIVIC-TRACE/data/processed/civic_trace_ytd_2026_isolated.csv`
  - **Dimensions:** `1,136` rows × `87` columns (`2026` YTD)
  - **File Size (Bytes):** `1,751,284`
  - **SHA-256 Checksum:** `51e89a4309fe6a6e495cbc48181fb46f09813f331d3c37f0a6b00311230fe1bc`
- **Round-Trip & Pre-Execution Readiness Check:** `[PASSED]` Verified with `record_completeness_score` (`87` columns).

---

## 7. Analytical Execution Log (Live Amendments)

- **Full-History Rebuild Sync:** Rebuilt `2013–2025` primary dataset (`n = 15,325`) and isolated `2026` YTD (`n = 1,136`).
- **Step 5 Complete (`RQ5 Data Completeness & Schema Audit`):** Generated variable completeness profile (`table_15`), July 13, 2026 schema-era audit (`table_16`), `record_completeness_score` (`87` columns), and `fig_09`.
- **Step 6 Complete (`Statistical Diagnostics & 2013–2025 Harmonization`):** Harmonized `table_01`, `table_02`, `table_05`, and `table_06` (`2015–2024` 10-year WaPo benchmark) to `n = 15,325`, and exported `table_17` & `fig_10`.
- **Step 7 Complete (`Phase 6 Visual Suite & 2013–2025 State Rates`):** Exported `table_11_state_per_capita_rates_2013_2025.csv`, Matplotlib/Seaborn figures (`fig_11`, `fig_13`, `fig_15`), and interactive Plotly HTML dashboards (`fig_12`, `fig_14`) for `n = 15,325`.
- **Step 8 Complete (`Phase 8 Reproducibility & Executive Report`):** Built SQLite database `data/processed/civic_trace.db` (`SHA-256`: `03e3844a1ef308031359a83b2f313d6b193fc53919681829b64ec1155c11621d`), `documentation/executive_report.md`, `README.md`, and `requirements.txt`.
