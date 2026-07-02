# PySpark Employee Data Analysis

This project implements a data processing and analytical pipeline using the PySpark DataFrame API. It focuses on data transformation, window functions, and complex aggregations to extract business intelligence from an employee dataset.

## Dataset & Project Origin

The analysis is performed on the Employee![https://www.kaggle.com/datasets/nisargjagtap/employee](dataset) Dataset. 
The project challenges were curated in collaboration with Google Gemini, which framed 15 progressive-difficulty questions to test core PySpark capabilities. These questions span from basic data cleaning to advanced analytical techniques

## Technical Operations & Functions

The project utilizes the pyspark.sql module to execute high-performance transformations:

## 1. Data Cleaning & Schema Management

String Manipulation: Leveraged concat_ws for efficient string concatenation of First Name and Last Name.

Schema Standardization: Employed withColumnRenamed to enforce snake_case naming conventions across the dataset.

Temporal Processing: Used to_date with specific format strings ('dd-MM-yyyy') to cast string data into native Spark DateType for chronological filtering.

## 2. Analytical Queries & Aggregations

Grouping & Aggregation: Utilized groupBy combined with agg to perform multi-metric calculations (count, avg, sum, max).

Pivoting: Implemented pivot on categorical columns (Gender) to create cross-tabulation reports for salary distribution.

Conditional Logic: Applied when and otherwise to create the Leave_Utilization derived feature, demonstrating proficiency in vectorized conditional processing.

## 3. Advanced Window Functions

The project demonstrates mastery of the pyspark.sql.window.Window object for contextual analysis:

Ranking: Used dense_rank() partitioned by Department to identify the top earners in each group.

Running Totals: Implemented cumulative salary calculations using sum() over an ordered window.

Lead Analysis: Leveraged lead() to compare an employee's salary against the "next" highest earner within a Country partition, effectively calculating salary gaps.
