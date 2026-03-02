# Information and Data Quality Project AY 2025-2026 at Politecnico di Milano
Project on assessing, cleaning, and standardizing a heavily denormalized dataset.

Notebook written in collaboration with:
- Alessio Tagab


## **Project Overview**
This repository contains a Jupyter Notebook-based data preparation and cleaning pipeline developed for the Data and Information Quality course at Politecnico di Milano. The project focuses on assessing, cleaning, and standardizing a heavily denormalized dataset containing approximately 3,900 records of personal service businesses in Milan.


## **Core Techniques Applied**
To transform this fragmented data into a structured and reliable resource, the following data quality techniques were implemented:
- Data Profiling: Utilized the ydata_profiling library to generate comprehensive HTML and JSON reports to assess the initial and final states of the dataset.
- Parsing & Atomization: Leveraged Regular Expressions (Regex) to extract structured atomic address components (street name, number, zone) from unstructured text strings.
- Taxonomy Standardization: Built custom dictionary mappings to normalize heterogeneous and unstructured business activity descriptions into a clean, standardized classification system.
- Smart Imputation: Addressed missing values using spatial mode imputation for geographic attributes and group-mean imputation for numerical features.
- Outlier Detection: Applied Interquartile Range (IQR) and Z-Score statistical methods to identify and assess anomalies in numerical data distributions.
- Entity Resolution & Deduplication: Implemented probabilistic Record Linkage with a custom blocking strategy to detect fuzzy duplicates. Used conflict resolution logic, including majority voting and "Smart Merge" set unions, to combine duplicate records without losing valid data.
