# ETL Agent Performance Reporting

## Project Overview

This project demonstrates a simple **ETL (Extract, Transform, Load) pipeline** combined with automated reporting.

The workflow processes raw operational data from multiple sources, transforms it into a structured dataset using **Power Query in Excel**, and automatically sends **personalized performance reports** to agents using **Power Automate**.

The goal of the project is to show how raw data can be transformed into actionable insights and distributed automatically.

---

## Data Sources (Extract)

The process starts with **three source tables** stored in **CSV and Excel files**.

These datasets contain operational information used to calculate agent performance metrics.

The raw files are stored in the repository in the `data/raw` folder.

---

## Data Transformation (Transform)

Data transformation is performed in **Excel using Power Query**.

The three source tables are imported into Power Query and processed through several transformation stages.

Each dataset is first cleaned and prepared individually before being combined with the others.

Main transformation steps include:

* Cleaning and standardizing raw data
* Removing incomplete or irrelevant records
* Filtering datasets
* Creating aggregated versions of the source tables
* Merging multiple datasets into one combined table
* Grouping and calculating performance metrics

The transformation process contains multiple **intermediate query steps**, such as cleaned tables, aggregated datasets, and merged tables.

These steps ultimately produce **one final structured output table** used for reporting.

---

## Final Output (Load)

The transformation process results in a **single clean output table** containing performance metrics for each agent.

This table serves as the input dataset for the automated reporting process.

The final table is stored in the `data/output` folder.

---

## Automation (Power Automate)

After the dataset is prepared, **Power Automate** is used to automate the reporting process.

The automation flow performs the following steps:

1. Reads rows from the final output table
2. Processes each row individually
3. Generates a personalized HTML report
4. Sends an **individual email to each agent** containing their weekly performance metrics

This ensures that each agent receives a **custom report based on their own weekly data**.

---

## ETL Pipeline Summary

1. **Extract** – Import raw data from three source tables (CSV and Excel).
2. **Transform** – Clean, filter, aggregate, and merge datasets using Power Query.
3. **Load** – Produce a final structured table containing agent metrics.
4. **Automate** – Use Power Automate to send personalized HTML email reports.

---

## Technologies Used

* Excel
* Power Query
* Power Automate
* HTML email formatting

---

## Repository Structure

data
│
├── raw → source CSV and Excel files
├── transformed → Excel file containing Power Query transformations
└── output → final metrics table used for reporting

automation
└── Power Automate flow / screenshots

---

## Outcome

This project demonstrates a practical example of a **data workflow combining data transformation and process automation**.

Raw operational data is transformed into a clean analytical dataset and automatically delivered to end users through personalized email reports.
