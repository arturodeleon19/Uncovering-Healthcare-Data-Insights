# Uncovering-Healthcare-Data-Insights
An end-to-end data science project exploring healthcare datasets using Python, Pandas, Seaborn, and Jupyter Notebooks. It features comprehensive exploratory data analysis (EDA), custom visualizations, and a memory-optimized scikit-learn machine learning pipeline accelerated on A100 GPUs

# Healthcare Dataset Analysis & Cost Anomaly Exploration

## Overview
This repository contains a Python Jupyter Notebook designed to analyze a comprehensive healthcare dataset. The project demonstrates data ingestion, database integration using SQLite, advanced SQL querying within Pandas, and statistical data visualization using Seaborn.

---

## Dataset Details
* **Source Dataset**: `healthcare_dataset.csv` (extracted from `Health Dataset by Prasad Patil.zip`) source:'https://www.kaggle.com/datasets/prasad22/healthcare-dataset?select=healthcare_dataset.csv'.
* **Total Volume**: 55,500 patient records.
* **Core Features**: Patient demographics (Name, Age, Gender, Blood Type), clinical details (Medical Condition, Medication, Test Results, Doctor, Hospital), and administrative data (Date of Admission, Discharge Date, Room Number, Insurance Provider, Billing Amount, Admission Type).

---

## Tech Stack & Dependencies
* **Python**
* **Pandas** (Data manipulation and dataframe handling).
* **SQLite3** (Relational database operations).
* **Matplotlib & Seaborn** (Data visualization and heatmaps).

---

## Notebook Workflow
1. **Data Extraction**: Unzips the raw dataset archive directly into the working directory.
2. **Data Loading & Inspection**: Loads the CSV file into a Pandas DataFrame to inspect initial rows and schema structures.
3. **Database Population**: Migrates the 55,500 records from the DataFrame into a local SQLite database (`my_database.db`) table named `my_table`.
4. **SQL Aggregation**: Executes a custom SQL query to calculate and group average billing amounts by `Medical Condition` and `Insurance Provider`.
5. **Visualization**: Pivots the aggregated dataset and builds a customized 2D heatmap (`YlOrRd` palette) to map cost intensity across conditions and insurers.

---

## Key Insights & Findings
* **Tight Billing Compression**: Average billing amounts are tightly clustered between \$24,857 and \$26,117, showing minimal overall variance.
* **Obesity as the Highest Cost Driver**: Obesity consistently commands the highest billing averages across multiple insurance providers, peaking with Cigna at \$26,117.00 and Blue Cross at \$26,100.79.
* **Cancer Exhibiting Lower Averages**: Conversely, Cancer records lower tier averages in this dataset, bottoming out with UnitedHealthcare at \$24,857.85 and Aetna at \$24,923.41.
* **Minimal Inter-Provider Discrepancy**: Within any single medical condition, the cost delta between the highest and lowest insurance provider is narrow (typically \$400 to \$600), suggesting insurance type has minimal impact on average billing within this scope.

---

## Usage
To run this notebook, ensure you have the required libraries installed and place the `Health Dataset by Prasad Patil.zip` file in your `/content/` directory (or update the file path accordingly).
