# Data Card: UCI Student Performance Dataset

## Dataset Name

UCI Student Performance Dataset

## Dataset Source

- Repository: UCI Machine Learning Repository
- Dataset page: https://archive.ics.uci.edu/dataset/320/student+performance
- Direct ZIP download: https://archive.ics.uci.edu/static/public/320/student+performance.zip

## Intended Use

This dataset is used for a reproducible machine learning benchmark focused on early academic risk prediction and student success modeling.

## Project Use Case

The project uses this dataset to compare baseline and advanced machine learning models for predicting student academic success. The dataset also supports explainable AI analysis by identifying which features are most influential in student success prediction.

## Prediction Targets

The dataset supports two main target types:

1. Regression target: final grade G3.
2. Classification target: student_success, defined as 1 if G3 >= 10 and 0 otherwise.

## Important Leakage Note

The final grade column G3 should not be used as an input feature when it is used to create the binary target. Including G3 as a predictor would cause target leakage and unrealistically high model performance.

## Expected Raw Files

After download, the dataset is expected to include:

- student-mat.csv
- student-por.csv
- student.txt
- student-merge.R

## Data Limitations

This dataset is useful for reproducible benchmarking, but it has limitations:

- It is relatively small.
- It comes from a specific educational context.
- It may not generalize to all institutions or countries.
- It should not be used for real student intervention decisions without local validation.
- Sensitive student-support use cases require human oversight and fairness review.

## Reproducibility Notes

The project records the dataset source, target definition, cleaning process, modeling steps, and evaluation outputs. Raw and processed data files may be excluded from GitHub by .gitignore, but they should be reproducible through the documented download and processing steps.

## Selected for First GitHub Version

Yes. This dataset is selected as the first project dataset because it supports a complete end-to-end machine learning workflow in Google Colab.
