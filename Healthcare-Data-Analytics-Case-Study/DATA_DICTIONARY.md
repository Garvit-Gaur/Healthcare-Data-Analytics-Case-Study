# Data Dictionary

All source sheets from `HIMS.xlsx` are included as CSV files under `data/`. The source workbook has 19 relational tables and one data-quality audit sheet.

## `admission.csv`

- **Rows:** 45,001
- **Columns:** admission_id, admission_date, discharge_date, admission_type, admission_status, patient_id, department_id, ward_id, bed_id, disease_id

## `bed.csv`

- **Rows:** 415
- **Columns:** bed_id, bed_number, bed_status, ward_id, Bed_Number_Check, Corrected_Bed_Number

## `billing.csv`

- **Rows:** 45,000
- **Columns:** bill_id, bill_date, total_amount, insurance_covered_amount, patient_payable_amount, payment_status, payment_mode, admission_id

## `billing_details.csv`

- **Rows:** 112,402
- **Columns:** billing_detail_id, charge_type, reference_id, amount, bill_id, Reference_ID_Check, corrected reference id

## `department.csv`

- **Rows:** 11
- **Columns:** department_id, department_name, department_type, floor_number, status

## `diagnostic_test.csv`

- **Rows:** 9
- **Columns:** test_id, test_name, test_category, standard_cost, department_id

## `disease.csv`

- **Rows:** 20
- **Columns:** disease_id, disease_name, disease_category

## `doctor.csv`

- **Rows:** 98
- **Columns:** doctor_id, employee_id, specialization, qualification, experience_years

## `drug.csv`

- **Rows:** 250
- **Columns:** drug_id, drug_name, brand_name, drug_category, unit_cost, manufacturer_id

## `drug_inventory.csv`

- **Rows:** 250
- **Columns:** inventory_id, current_stock, reorder_level, inventory_status, last_restock_date, drug_id

## `drug_manufacturer.csv`

- **Rows:** 300
- **Columns:** manufacturer_id, manufacturer_name, country, reliability_rating, contract_status

## `employee.csv`

- **Rows:** 500
- **Columns:** employee_id, employee_name, gender, role, employment_type, date_of_joining, department_id

## `insurance_provider.csv`

- **Rows:** 50
- **Columns:** insurance_provider_id, provider_name, provider_type, contact_details, coverage_limit

## `patient.csv`

- **Rows:** 30,000
- **Columns:** patient_id, gender, date_of_birth, blood_group, city, contact_number, Contact_Type, Contact_Validation

## `patient_diagnostic.csv`

- **Rows:** 63,269
- **Columns:** patient_diagnostic_id, test_date, result_status, admission_id, test_id, doctor_id

## `patient_insurance.csv`

- **Rows:** 21,613
- **Columns:** patient_insurance_id, policy_number, coverage_percentage, policy_start_date, policy_end_date, patient_id, insurance_provider_id, Policy_Number_Check

## `prescription.csv`

- **Rows:** 73,109
- **Columns:** prescription_id, dosage, frequency, duration_days, admission_id, drug_id

## `staff_assignment.csv`

- **Rows:** 207
- **Columns:** assignment_id, employee_id, ward_id, shift

## `ward.csv`

- **Rows:** 27
- **Columns:** ward_id, ward_name, ward_type, total_beds, department_id

## `data_quality_audit.csv`

- **Rows:** 5
- **Columns:** Table, Issue, Excel Result

\n## Privacy handling\n\nDirect contact fields are masked in the repository copy (`REDACTED`), and employee names are replaced with neutral labels. No rows or relational IDs were removed.\n