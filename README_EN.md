# Project: Income Statement Report in Power BI

## Description
This repository documents the process of extracting, transforming, and loading (ETL) data used to build an Income Statement (DRE) report in Power BI. The project addresses the challenges encountered, the solutions applied, and the results obtained.

---

## Repository Structure
```
|
|-- DRE_Final/                 # Processed SQLite database
|   |-- dre_tratado_final.db   # Final file after cleaning and adjustments
|
|-- Tratamento_e_Validação/    # Processing in Colab
|   |-- Notebook_Colab.ipynb   # ETL code with validations and fixes
|
|-- Dashboard/                 # Power BI file
|   |-- Dashboard.pbix         # Final report with DAX measures and visualizations
|
|-- Documentação.md            # Process details and solutions applied
|-- README_EN.md               # Project overview
```

---

## Challenge Context
The task was to develop an Income Statement (DRE) report in Power BI, starting with raw files that contained issues in the ETL process. The challenge involved fixing discrepancies in the final values of the "Gerencial Result for the Period" and validating data consistency to ensure reliable analysis.

---

## Solution Implemented
1. **ETL in Colab:**
   - Removed duplicate records from the database.
   - Fixed inconsistencies in values and date formats.
   - Standardized dimensional tables (units and structure).
   - Validated calculations by comparing with the original spreadsheets.

2. **Processed Database:**
   - Exported the adjusted database to a SQLite file.

3. **Report in Power BI:**
   - Developed DAX measures for Gross Revenue.
   - Created vertical and horizontal analyses to monitor variations.
   - Added dynamic filters by month and unit type.

---

## Results
The process resulted in a functional and detailed Income Statement report with consistent values after fixing ETL issues.

This repository includes all necessary files to reproduce the process and further develop the analyses.

---

## How to Reproduce
1. **Database:**
   - Open the SQLite file using Power BI or any compatible tool.

2. **Colab:**
   - Run the notebook to review or adjust the ETL processes.

3. **Power BI:**
   - Load the .pbix file into Power BI Desktop to edit or view the report.

---

## Author
William Volpato

