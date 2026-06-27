# Data Cleaning and Preparation Report

## Project

Student Success AI: A Reproducible Benchmark for Early Academic Risk Prediction Using Explainable Machine Learning, with Public Educational Data

## Date Created

2026-06-27 20:28:32

## Dataset

UCI Student Performance Dataset

## Purpose of This Step

This step cleaned and prepared the selected public educational dataset for machine learning.

## Data Cleansing Process

Data cleansing for machine learning is the process of converting raw data into a reliable, consistent, and model-ready dataset. In this project, the workflow loaded the raw UCI Student Performance files, standardized column names, checked missing values, removed duplicate records, handled missing values, created a student-success target variable, removed target-leakage columns, encoded categorical variables, and saved reproducible train/test datasets.

## Raw Dataset Shape

- Rows: 1044
- Columns: 34

## Cleaned Documentation Dataset Shape

- Rows: 1044
- Columns: 36

## Strict Clean Modeling Dataset Shape

- Rows: 1044
- Columns: 32

## Encoded ML-Ready Dataset Shape

- Rows: 1044
- Columns: 59

## Duplicate Records Removed

- 0

## Missing Values After Cleaning

- 0

## Target Variable

The target variable is `student_success`.

Definition:

- `student_success = 1` if final grade `G3 >= 10`
- `student_success = 0` if final grade `G3 < 10`

## Target Distribution

 student_success  count  percent
               0    230    22.03
               1    814    77.97

## Leakage Columns Removed

The following grade columns were removed from the machine learning feature set:

- G1
- G2
- G3
- final_grade

This supports a strict early academic-risk prediction setup.

## Train/Test Split

- Training rows: 835
- Testing rows: 209
- Test size: 20%
- Random seed: 42
- Stratified split: True

## Files Created

| File | Purpose |
|---|---|
| `data/processed/student_ml_clean.csv` | Strict clean modeling dataset before one-hot encoding |
| `data/processed/student_ml_ready.csv` | Strict encoded machine-learning-ready dataset |
| `data/processed/student_success_clean_documentation_only.csv` | Documentation-only cleaned dataset containing original grade columns |
| `data/processed/student_success_ml_ready.csv` | Additional encoded ML-ready dataset |
| `data/processed/student_success_train.csv` | Training dataset |
| `data/processed/student_success_test.csv` | Testing dataset |
| `reports/preprocessing/data_cleaning_report.md` | Cleaning and preparation report |
| `reports/preprocessing/step_g_preprocessing_metadata.json` | Machine-readable preprocessing metadata |

## Important Leakage Control

The file `student_success_clean_documentation_only.csv` is not intended for modeling because it contains the original grade columns. The files `student_ml_clean.csv` and `student_ml_ready.csv` should be used for Step H modeling.

## Status

Step G is completed successfully. The dataset is cleaned, leakage-controlled, encoded, split, documented, and ready for exploratory data analysis and baseline modeling.
