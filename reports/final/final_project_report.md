
# Final Project Report

## Project Title

Student Success AI: A Reproducible Benchmark for Early Academic Risk Prediction Using Explainable Machine Learning, with Public Educational Data

## Project Objective

The objective of this project is to build a reproducible machine learning benchmark for early academic-risk and student-success prediction using a public educational dataset. The project compares multiple machine learning algorithms, documents preprocessing decisions, checks for target leakage, evaluates model performance, and prepares the repository for GitHub-based reproducibility.

## Dataset

The project uses a public educational dataset prepared for machine learning.

Cleaned modeling dataset:

data/processed/student_ml_clean.csv

Target variable:

student_success

## Workflow Summary

The project workflow includes:

1. GitHub repository creation and structure setup.
2. Dataset download and inspection.
3. Data cleaning and machine-learning preparation.
4. Leakage audit.
5. Exploratory data analysis.
6. Preprocessing pipeline construction.
7. Baseline and advanced model training.
8. Model comparison.
9. Explainability preparation.
10. Report, table, and figure generation.

## Leakage Audit

The updated leakage audit confirmed that no numeric feature had a near-perfect correlation with the target. The target column itself was correctly detected and excluded from the feature matrix.

## Model Development

The project is designed to compare multiple machine learning algorithms, including baseline and stronger models. The main goal is to determine which algorithm performs best for early academic-risk and student-success prediction under a strict non-leakage workflow.

## Reproducibility

The repository includes notebooks, source-code folders, data folders, report folders, and GitHub synchronization checks. The project is intended to be reproducible in Google Colab and GitHub.

## Current Completion Status

This report was generated as part of the final completion audit workflow.

Generated on: 2026-06-27 21:39:19
