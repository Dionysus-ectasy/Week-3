# Hospital Operations & Cost Intelligence

**AnalystLab Africa Experience Lab | Week 3 | Track A: Data Analytics**
Author: Divine Okezie Nwaoha

A 7-page Power BI dashboard analysing 27,891 hospital encounters (974 patients, 47,701 procedures, Jan 2011 to 5 Feb 2022, one hospital): volume trends, encounter classes, cost and payer coverage, procedures and patient flow.

## Headline finding

48.7% of encounters show zero recorded payer coverage and hold 62.2% of the $101.5M total claim cost. Split by payer, five private insurers record about 0% coverage while Medicaid, Medicare, Dual Eligible and BCBS record 69% to 94%. This points to a likely data-capture gap, not necessarily a funding gap.

## Repository contents

| # | Deliverable | File |
|---|---|---|
| 1 | Power BI dashboard (7 pages) | `Hospital_Operations_and_Cost_Intelligence.pbix` |
| 2 | Data-quality assessment | `02_Data_Quality_Assessment.pdf` |
| 3 | KPI definition sheet | `03_KPI_Definition_Sheet.pdf` |
| 4 | Dashboard screenshots | `04_Dashboard_Screenshots.pdf` |
| 5 | Validation evidence | `05_Validation_Evidence.pdf` |
| 6 | Executive summary (key findings and recommendations) | `06_Executive_Summary.pdf` |

## Tools

Power BI, Power Query, DAX, with SQL (in-memory) and Python used to validate key figures independently against the raw data.

## Method in brief

1. Profiled all source files and documented data-quality issues before cleaning anything.
2. Modelled encounters to patients, payers, organizations, procedures and a date table.
3. Built KPIs as DAX measures (see the KPI definition sheet).
4. Checked key figures independently with SQL/Python and compared them with the dashboard (see the validation evidence).

## Limitations

- Single hospital; 2011 is a ramp-up year and 2022 covers only 5 February.
- Claim costs are not clinical outcomes; there are no diagnoses, so no clinical claims are made.
- A 30-day return flags any later encounter, not a clinical readmission.

## Privacy

Patient names, addresses, birthplace, coordinates and zip codes were removed in Power Query and are not shown in any visual. No raw patient data is committed to this repository.

## Not included on purpose

- The raw CSV files.
- `create_hospital_db.sql`: it drops and recreates a database, it was not executed, and it contains patient names.
