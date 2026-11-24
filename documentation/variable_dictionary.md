# CIVIC TRACE — Variable Dictionary

- **Unit of Analysis:** 1 row = 1 recorded victim.
- **`armed_status_category`:** Separates `Allegedly Armed`, `Allegedly Unarmed` (`Unarmed/did not have a weapon`), `Unknown / Undetermined Weapon`, and `Missing (NaN)`.
- **`footage_status_category`:** Separates `Footage Recorded`, `Confirmed No Footage` (`No`), `Footage Missing`, `Not Recorded`, and `Missing (NaN)`.

---

## Engineered Data-Quality Feature (`Step 5 Amendment`)

- **`record_completeness_score` (`float64`, `0.00–100.00`):** Percentage of `11` core substantive fields (`age, gender, race, county, agency_responsible, use_of_force_clean, allegedly_armed_with_clean, encounter_type, call_for_service, flee_clean, incident_footage_clean`) containing a resolved substantive value (excluding both `NaN` and explicit `Unknown/Undetermined` tokens).
