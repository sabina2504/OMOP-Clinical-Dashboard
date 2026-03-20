# OMOP-Clinical-Dashboard
OMOP CDM v5.4 Clinical Dashboard for Eunomia Dataset Analysis
A Power BI Desktop dashboard built on a synthetic [OMOP Common Data Model v5.4](https://ohdsi.github.io/CommonDataModel/cdm54.html) dataset, designed to explore patient demographics and clinical activity.
 
---
 
## Dataset
 
Synthetic data — not real patient records. 2,694 patients, spanning 1908–2019.
 
| Domain | Records |
|---|---|
| Conditions | 65,332 |
| Drug Exposures | 63,323 |
| Procedures | 37,409 |
| Measurements | 41,870 |
| Observations | 1,471 |
| Visits | 1,037 |
 
---
 
## Report Pages
 
**Page 1 — Patient Demographics**
Patient counts by age group, gender, race, and ethnicity. Includes comorbidity KPIs: patients with 10+ conditions overall, and patients with 3+ conditions in a single calendar year.
 
**Page 2 — Clinical Activity**
Top diagnoses, procedures, medications, observations, and measurements by frequency. KPI ribbon shows total record counts across all clinical domains.
 
---
 
## Model Highlights
 
- **Date table** — custom calculated table covering 1908–2019, marked as official Date table
- **50 DAX measures** — organized into display folders: Patients, Conditions, Drugs, Visits, Measurements, Procedures, Observations, Comorbidity
- **Calculated columns** — `Age Group` + `Age Group Sort` on Person; `condition_start_year` (hidden helper) on Condition_occurrence
- All numeric columns set to **Don't Summarize**
- All tables and columns documented with descriptions from the OMOP CDM v5.4 spec
 
---
 
## Known Limitations
 
- All visits are Inpatient only — Outpatient/ER measures return 0
- Measurements have no numeric values — range comparison measures return blank
- Date table is related to `Visit_occurrence` only, not other clinical tables
 
---
 
## Requirements
 
Power BI Desktop (latest recommended). No gateway needed — fully imported model.
 
---
 
## References
 
- [OMOP CDM v5.4 Specification](https://ohdsi.github.io/CommonDataModel/cdm54.html)
- [The Book of OHDSI](https://ohdsi.github.io/TheBookOfOhdsi/)
- [OHDSI Community](https://www.ohdsi.org/)
- [Eunomia Dataset](https://github.com/OHDSI/EunomiaDatasets)
