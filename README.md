# Healthcare Medallion Architecture Project

## Overview
This project demonstrates a Medallion Architecture using Databricks, PySpark, and Delta Lake.

## Bronze Layer
Raw healthcare data ingestion:
- Admissions
- Patients
- Doctors
- Billing
- Hospitals
- Procedures

## Silver Layer
Data quality and validation:
- Null validation
- Duplicate validation
- Business key validation
- Financial integrity validation
- Data standardization

## Technologies
- Databricks
- PySpark
- Delta Lake
- GitHub

## Project Structure

scripts/
├── bronze/
├── silver/
└── gold/

## Next Phase
Build Gold-layer business analytics:
- Revenue by Hospital
- Revenue by State
- Revenue by Specialty
- Admissions by Year
- Top Procedures