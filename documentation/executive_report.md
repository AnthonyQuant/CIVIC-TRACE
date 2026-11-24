# CIVIC TRACE: Fatal Police Encounters in the United States (2013–2025)
### Executive Analytical Report, Empirical Findings & Reproducibility Record

- **Generated (UTC):** `2026-11-24 20:36:53 UTC`
- **Primary Analytical Scope:** `2013–2025` Complete Calendar Years (`n = 15,325` recorded victim fatalities)
- **Isolated Year-to-Date Snapshot:** `2026-01-01` through `2026-11-10` (`n = 1,136` recorded victim fatalities; excluded from complete-year totals)
- **Secondary Cross-Source Benchmark:** Washington Post Fatal Force (`2015–2024`, `n = 10,430` fatal line-of-duty shootings)
- **Population Denominator Source:** U.S. Census Bureau Population Estimates Program (`50` states + `District of Columbia`)

---

## 1. Executive Summary

**CIVIC TRACE** examines recorded fatal police encounters across the United States from **2013 through 2025** using incident-level records from **Mapping Police Violence (MPV)** (`n = 15,325` complete-year records), anchored against **U.S. Census Bureau** resident population denominators and benchmarked over the 10-year `2015–2024` overlap against **The Washington Post's Fatal Force** database (`n = 10,430`). Because neither database captures the denominator of nonfatal police stops, arrests, or use-of-force encounters, this investigation enforces **methodological restraint**: all findings describe recorded fatalities, population-adjusted mortality incidence rates, and reporting completeness rather than encounter-level fatality probabilities or causal determinations.

Across the 13 complete calendar years (`2013–2025`), recorded fatalities averaged **`1,178.8` deaths per year**, rising from **`1,027` in `2014`** to a peak of **`1,387` in `2024`** before moderating to **`1,317` in `2025`**. Firearms were the primary use-of-force mechanism in **`14,094` cases (`91.97%`)**. Adjusting for state resident population exposes a sharp structural divergence: while **California**, **Texas**, and **Florida** recorded the highest raw death counts, smaller-population Mountain West and Southern jurisdictions—led by **New Mexico (`1.270` per 100k)** and **Alaska (`1.106` per 100k)**—experienced per-capita mortality incidence rates roughly **3.2× to 3.7×** the national mean (**`0.347` per 100,000 resident-years**) and **18× to 21×** the lowest-rate states (**Rhode Island** and **Massachusetts**).

---

## 2. Research Questions & Empirical Answers (RQ1–RQ5)

### RQ1 — Historical & Seasonal Trends: How have recorded fatal police encounters changed over time?
* **13-Year Trajectory (`2013–2025`):** Annual recorded fatalities increased at an OLS trend of **`+20.06` deaths/year** (`R² = 0.86`, `p = 4.30e-06`), growing from `1,027` (`2013`) to `1,387` (`2024`) and `1,317` (`2025`). This upward trajectory reflects both real-world incident volume and post-2013 improvements in public records transparency and media tracking.
* **Seasonal Pattern:** Across all 156 complete calendar months (`2013–2025`), recorded fatalities peaked in warm-weather months—led by **Aug (`1,365` deaths)**—and reached their annual trough in **Sep (`1,161` deaths)**.
* **Date-Aligned YTD Benchmark (`Jan 1 – Nov 10`):** Comparing identical calendar windows shows **`1,136` recorded deaths in `2026` YTD** versus **`1,153` during the same window in `2025`** (`-1.47%`), confirming that `2026` YTD volume tracks slightly below `2025`.

### RQ2 — Demographics: What do recorded cases reveal about the age, race, and gender of victims?
* **Age Concentration:** Among `14,792` records with valid age (`533` missing `NaN`), victim age was concentrated in young-to-middle adulthood with a **median of `35.0` years** (`IQR = 28–46` years) and a **mean of `37.52` years** (`SD = 13.35`).
* **Gender:** Recorded victims were overwhelmingly **Male (`14,391`, `93.91%`)**, with **Female** accounting for **`888` (`5.79%`)**, and remaining records classified as `Unknown`, `Transgender Female`, `Transgender Male`, or `Non-Binary`.
* **Coded Race/Ethnicity:** Across `2013–2025`, **White** victims accounted for **`7,087` (`46.24%`)**, **Black** victims for **`3,972` (`25.92%`)**, **Hispanic** victims for **`2,815` (`18.37%`)**, and explicit **Unknown race** for **`888` (`5.79%`)**.

### RQ3 — Geography: How are recorded encounters distributed across states and counties?
* **Raw Volume Leaders (`2013–2025`):** **California (`2,111`)**, **Texas (`1,480`)**, and **Florida (`1,079`)** recorded the highest raw death totals.
* **Population-Adjusted Rate Leaders (`2013–2025`, U.S. Mean = `0.347` per 100k):** **New Mexico (`1.106`/100k)**, **Alaska (`0.885`/100k)**, and **Oklahoma (`0.722`/100k)** led all jurisdictions on a per-capita basis, whereas **Rhode Island (`0.069`/100k)**, **Massachusetts (`0.106`/100k)**, and **Connecticut (`0.132`/100k)** recorded the lowest annualized rates.

### RQ4 — Encounter Circumstances: What patterns appear across force mechanisms, alleged weapons, and encounter context?
* **Alleged Weapon Involvement:** **`11,500` (`75.04%`)** were classified as `Allegedly Armed`, **`2,322` (`15.15%`)** as `Allegedly Unarmed` (`Unarmed/did not have a weapon`), and **`1,503` (`9.81%`)** as `Unknown / Undetermined Weapon` (plus `0` `NaN`).
* **Initial Encounter Context:** Among coded encounter reasons, **`Part 1 Violent Crime` (`4,027`, `26.28%`)** and **`Person with a Weapon` (`2,672`, `17.44%`)** were the most frequent initial attendance categories.
* **Incident Video Footage:** Video footage was confirmed recorded in **`4,911` (`32.05%`)** of cases across `2013–2025`.

### RQ5 — Data Completeness & Schema Governance: How complete are the records across years and variables?
* **Substantive Completeness Improvement:** Across `11` core substantive fields, mean record completeness rose from **`86.96%` in `2013`** to **`92.66%` in `2025`** (13-year mean **`89.86%`**, median **`90.91%`**, with **`3,409` records at `100.0%`**).
* **Video Footage & Documentation Richness:** Records with confirmed video footage achieved **`96.70%` mean completeness** compared with **`86.64%`** when footage was absent or unrecorded (`t = 95.91`, `p < 1e-16`).
* **July 13, 2026 Schema Transition:** Auditing `2026` YTD records confirmed a clean schema boundary on `2026-07-13` (`723` pre-shift records; `413` post-shift records), preventing silent conflation of legacy `wapo_threat_level` and post-shift `threat_perception`.

---

## 3. Independent Cross-Source Benchmark (`2015–2024`)

Over the full 10-year overlap (`2015–2024`) tracked by both datasets:
* **Mapping Police Violence (All Force Mechanisms):** `11,912` recorded deaths
* **Mapping Police Violence (All Fatal Shootings):** `10,970` recorded shooting deaths (`10,714` on-duty + `256` off-duty)
* **Washington Post Fatal Force (On-Duty Fatal Shootings):** `10,430` recorded shooting deaths
* **Reconciled Alignment:** Restricting MPV to on-duty fatal shootings reconciles **`97.3%`** of the decade-wide count (`10,714` vs. `10,430`), with the remaining `+284` difference attributable to MPV's broader inclusion of fatal pursuits/non-firearm gunshot classifications and ongoing retrospective updates after WaPo closed collection on `2024-12-31`.

---

## 4. Methodological & Statistical Limitations

1. **Absence of Nonfatal Encounter Denominators:** Neither MPV nor WaPo tracks total nonfatal police stops, arrests, or non-lethal uses of force. Consequently, no predictive classification model can estimate the probability that a routine police encounter becomes fatal, and per-capita state rates represent **population-based mortality incidence**, not individual encounter risk.
2. **Observational & Media-Sourced Reporting Lag:** Both datasets rely on public reporting, FOIA requests, and official disclosures. Recent records (`2025–2026`) exhibit higher shares of `Unknown` weapon or footage classifications until investigations conclude.
3. **Preservation of Epistemic Uncertainty:** Explicit `"Unknown"` / `"Undetermined"` values were never merged with true `NaN` cells or imputed as negative outcomes (e.g., `"Unknown weapon"` is never treated as `"Unarmed"`).
4. **Descriptive & Ecological Scope:** Two-group tests (`H1–H3`) and state-level correlations (`E1`) quantify descriptive associations within compiled fatality records and do not establish individual-level causation or legal culpability.

---

## 5. Recommendations for Further Investigation

1. **Integrate Agency-Level Encounter & Arrest Denominators:** Pair `civic_trace.db` with FBI National Incident-Based Reporting System (NIBRS) arrest totals and state use-of-force registries (e.g., California DOJ URSUS) to estimate encounter-adjusted force ratios in high-reporting states.
2. **County-Level Socioeconomic & Rural-Urban Stratification:** Join county FIPS identifiers with Census American Community Survey (ACS) poverty, urbanization, and demographic tables to investigate why smaller Mountain West jurisdictions exhibit elevated per-capita rates.
3. **Post-2026 Schema Harmonization:** Monitor post-`2026-07-13` MPV releases as `threat_perception` coverage matures across full calendar years.
