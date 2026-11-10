# Healthcare Data Analytics Case Study

**Author:** Garvit Gaur

## Overview
An exploratory analysis of a Hospital Information Management System (HIMS) dataset. The project examines hospital revenue, department performance, patient revisit patterns, bed occupancy, doctor workload, and diagnostic activity.

## Dataset
The supplied `HIMS.xlsx` workbook contains **19 relational data tables and one data-quality audit sheet**. All sheets are preserved as CSV files in `data/`.

| Table | Rows |
|---|---:|
| patient | 30,000 |
| admission | 45,001 |
| billing | 45,000 |
| patient_diagnostic | 63,269 |
| employee | 500 |
| doctor | 98 |
| ward | 27 |
| bed | 415 |
| department | 11 |
| diagnostic_test | 9 |

Additional tables retained: `billing_details`, `disease`, `drug`, `drug_inventory`, `drug_manufacturer`, `insurance_provider`, `patient_insurance`, `prescription`, and `staff_assignment`. The `data_quality_audit.csv` file preserves the workbook's audit sheet.

## Repository Structure
```text
Healthcare-Data-Analytics-Case-Study/
├── data/                  # All 19 source tables + data quality audit
├── notebooks/
│   └── Healthcare_Case_Study.ipynb
├── DATA_DICTIONARY.md
├── README.md
├── requirements.txt
└── .gitignore
```

## Run the Project
```bash
pip install -r requirements.txt
jupyter notebook notebooks/Healthcare_Case_Study.ipynb
```

The notebook reads the CSV files from `data/` and contains the original analysis workflow. Run it from the repository root or its `notebooks/` folder.

## Analysis Areas
- Data quality checks: missing values, duplicates, ID uniqueness, and date parsing
- Hospital revenue and department-level billing performance
- Unique, repeat, and one-time patient analysis
- Bed availability and occupancy by ward/department
- Doctor distribution and patient workload
- Diagnostic result status and test utilization
- Monthly revenue trends and visual analysis

## Verified Headline Findings
The notebook was executed successfully against the supplied workbook:
- **Total hospital revenue:** 1,684,246,109 (source currency/unit not specified in the workbook)
- **Unique patients with admissions:** 23,275
- **Repeat patient rate:** 56.92%
- **Occupied beds:** 270 of 415
- **Bed occupancy rate:** 65.06%

These values are calculated directly from the supplied tables using the notebook's original logic.

## Data Notes
- The CSVs were exported from the workbook supplied for this project; no rows were intentionally filtered during export.
- Original column names are preserved, including columns with data-quality correction notes.
- The workbook includes a `Data Quality Audit` sheet, exported as `data_quality_audit.csv`.
- For safer public sharing, `patient.contact_number` and `insurance_provider.contact_details` are masked as `REDACTED`; employee names are replaced with neutral employee labels. The row counts and relational IDs are retained.

## Limitations
This repository preserves the source workbook's tables and the existing notebook analysis. Findings should be interpreted after running the notebook and validating any data-quality issues documented in the workbook.

## Visualizations
Rendered notebook charts are also available in `visualizations/` for quick review without running the notebook.
