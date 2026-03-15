## ETL Process – Data Transformation and Automated Reporting

This project demonstrates a simple ETL (Extract, Transform, Load) process combined with automated reporting.

### Data Sources
The process starts with **three source tables** stored in **CSV and Excel files**.  
These files contain operational data used to calculate weekly performance metrics.

### Data Transformation (Power Query in Excel)
The data is transformed using **Power Query in Excel**, where the following steps are applied:

- Data cleaning
- Filtering unnecessary records
- Standardizing columns
- Grouping and aggregating data
- Combining multiple tables

The result of the transformation is **one clean, structured output table** containing the final metrics.

### Automation (Power Automate)
After the data is prepared, **Power Automate** is used to automate the reporting process.

The flow performs the following steps:

1. Reads rows from the final output table.
2. Processes each row individually.
3. Sends an **individual HTML email** to each agent.

Each email contains the **agent's personal weekly performance metrics**, automatically generated based on the data from the output table.

### Outcome
This solution demonstrates how to combine:
- **Excel (Power Query)** for data transformation
- **Power Automate** for workflow automation
- **HTML email formatting** for personalized reporting

The result is an automated pipeline that transforms raw data into clean insights and delivers them directly to the relevant recipients.
