# Dataset Inspection Report

## Dataset

**Name:** UCI Student Performance Dataset

**Source:** https://archive.ics.uci.edu/dataset/320/student+performance

**UCI Dataset ID:** 320

## Files Downloaded

- `student-mat.csv`: Mathematics course dataset
- `student-por.csv`: Portuguese language course dataset
- `student.txt`: Original dataset documentation, if included in extraction

## Canonical Raw Files Created

- `data/raw/student-mat.csv`
- `data/raw/student-por.csv`

## Dataset Shape

| Dataset | Rows | Columns |
|---|---:|---:|
| Math | 395 | 33 |
| Portuguese | 649 | 33 |

## Column Consistency

The two files have the same columns: **True**

## Target Variable

The main target variable is:

- `G3`: final grade, numeric scale from 0 to 20.

For later binary early-risk prediction, the planned target definition is:

- `student_success = 1` if `G3 >= 10`
- `student_success = 0` if `G3 < 10`

## Target Summary

| Dataset | Mean G3 | Median G3 | Risk Count: G3 < 10 | Risk Percent | Success Count: G3 >= 10 | Success Percent |
|---|---:|---:|---:|---:|---:|---:|
| Math | 10.415 | 11.000 | 130 | 32.91% | 265 | 67.09% |
| Portuguese | 11.906 | 12.000 | 100 | 15.41% | 549 | 84.59% |

## Missing Values

- Math missing values: 0
- Portuguese missing values: 0

## Duplicate Rows

- Math duplicate rows: 0
- Portuguese duplicate rows: 0

## Variable Types

- Categorical variable count: 17
- Numerical variable count: 16

## Important Modeling Warning

`G3` is the final target outcome. It should never be used as an input feature when `student_success` is created from `G3`.

`G1` and `G2` are prior-period grades and are strongly related to `G3`.

For a realistic early academic risk prediction benchmark, later modeling should include two versions:

1. **Full information model:** includes available predictors except `G3`.
2. **Strict early-risk model:** excludes `G1`, `G2`, and `G3` to avoid near-target grade information.

## Inspection Outputs Created

- `reports/inspection/dataset_source_metadata.json`
- `reports/inspection/column_consistency_check.json`
- `reports/inspection/dtype_summary.csv`
- `reports/inspection/missing_values_summary.csv`
- `reports/inspection/duplicate_rows_summary.json`
- `reports/inspection/target_G3_summary.csv`
- `reports/inspection/variable_type_summary.json`
- `reports/inspection/descriptive_summary_math.csv`
- `reports/inspection/descriptive_summary_portuguese.csv`
- `reports/inspection/preview_math_first_10_rows.csv`
- `reports/inspection/preview_portuguese_first_10_rows.csv`

## Step F Completion Statement

Step F is completed. The selected dataset was downloaded, extracted, inspected, documented, and prepared for Step G data cleaning.