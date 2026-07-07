# 📘 Naming Conventions

This document defines the naming conventions used throughout the Healthcare Data Engineering Pipeline. These standards ensure consistency, readability, and maintainability across the Databricks Lakehouse.

---

# Table of Contents

- General Principles
- Schema Naming
- Bronze Layer
- Silver Layer
- Gold Layer
- Column Naming
- Primary and Foreign Keys
- Notebook Naming
- File Naming

---

# General Principles

- Use **snake_case** for all object names.
- Use **lowercase letters**.
- Separate words using underscores (`_`).
- Use meaningful business names.
- Avoid SQL reserved keywords.
- Use English for all object names.

### Examples

✅ `hospital_name`

✅ `procedure_cost`

✅ `admission_date`

❌ `HospitalName`

❌ `ProcedureCost`

❌ `Hospital Name`

---

# Schema Naming

The project follows the Medallion Architecture.

| Schema | Purpose |
|---------|---------|
| bronze | Raw ingested data |
| silver | Cleaned and validated data |
| gold | Business-ready datasets |

Examples

```
health.bronze
health.silver
health.gold
```

---

# Bronze Layer

Bronze tables preserve the original source structure.

### Naming Pattern

```
<entity>
```

Examples

```
patients

doctors

hospitals

procedures

admissions_2021

billing_2025
```

---

# Silver Layer

Silver tables contain cleaned and standardized data.

### Naming Pattern

```
<entity>
```

Examples

```
patients

doctors

hospitals

procedures

billing

admissions
```

---

# Gold Layer

Gold tables use descriptive business names representing KPIs.

### Naming Pattern

```
<business_metric>
```

Examples

```
revenue_by_hospital

revenue_by_state

revenue_by_specialty

admissions_by_year

procedure_performance
```

---

# Column Naming

Columns follow snake_case.

Examples

```
patient_id

doctor_id

hospital_name

procedure_cost

total_revenue

times_performed
```

---

# Primary Keys

Primary keys follow the pattern

```
<entity>_id
```

Examples

```
patient_id

doctor_id

hospital_id

procedure_id

admission_id

billing_id
```

---

# Foreign Keys

Foreign keys use the same name as the referenced primary key.

Examples

```
patient_id

doctor_id

hospital_id

procedure_id

admission_id
```

---

# Notebook Naming

Notebook names describe the business entity or business metric.

Bronze

```
bronze_layer
```

Silver

```
patients

doctors

billing

hospitals

procedures

admissions
```

Gold

```
revenue_by_hospital

revenue_by_state

revenue_by_specialty

admissions_by_year

procedure_performance
```

---

# File Naming

Raw source files retain their original names.

Examples

```
patients.csv

doctors.csv

hospitals.csv

procedures.csv

admissions_2021.csv

billing_2025.csv
```

---

# Technologies

- Databricks Lakehouse
- Delta Lake
- PySpark
- Spark SQL
- GitHub

---

# Notes

- Bronze stores raw data.
- Silver stores validated and standardized data.
- Gold stores business-ready analytical datasets.
- All tables are stored as Delta Tables.
