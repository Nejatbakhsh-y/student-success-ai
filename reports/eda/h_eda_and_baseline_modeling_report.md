# H. Exploratory Data Analysis and Baseline Machine Learning Modeling Report

## H1. Purpose

This report documents exploratory data analysis and baseline machine learning modeling for the strict leakage-controlled student-success dataset created in Step G.

## H2. Dataset Information

- Dataset path: `/content/student-success-ai/data/processed/student_ml_clean.csv`

- Dataset type: `strict_clean_before_encoding`

- Number of rows: 1044

- Number of columns: 32

- Duplicate rows: 0

- Total missing values: 0

## H3. Leakage Control

The modeling dataset was checked for forbidden leakage columns. No G1, G2, G3, final_grade, or direct final-outcome columns were found.

## H4. Target Variable

- Target column: `student_success`

- Task type: binary classification

- Rule inherited from Step G: `student_success = 1 if G3 >= 10 else 0`


Target distribution:


|   student_success |   count |   percent |
|------------------:|--------:|----------:|
|                 0 |     230 |     22.03 |
|                 1 |     814 |     77.97 |



## H5. Feature Summary

- Modeling features: 31

- Numerical modeling features: 13

- Categorical modeling features: 18

## H6. Top Missing-Value Columns

| column     |   missing_count |   missing_percent |
|:-----------|----------------:|------------------:|
| absences   |               0 |                 0 |
| activities |               0 |                 0 |
| address    |               0 |                 0 |
| age        |               0 |                 0 |
| dalc       |               0 |                 0 |
| failures   |               0 |                 0 |
| famrel     |               0 |                 0 |
| famsize    |               0 |                 0 |
| famsup     |               0 |                 0 |
| fedu       |               0 |                 0 |
| fjob       |               0 |                 0 |
| freetime   |               0 |                 0 |
| goout      |               0 |                 0 |
| guardian   |               0 |                 0 |
| health     |               0 |                 0 |



## H7. Baseline Model Results

| model                        |   accuracy |   balanced_accuracy |   precision_weighted |   recall_weighted |   f1_weighted |   f1_macro |   roc_auc |
|:-----------------------------|-----------:|--------------------:|---------------------:|------------------:|--------------:|-----------:|----------:|
| GradientBoosting             |   0.794258 |            0.602827 |             0.764627 |          0.794258 |      0.763201 |   0.617851 |  0.778208 |
| RandomForest                 |   0.794258 |            0.579421 |             0.763217 |          0.794258 |      0.750913 |   0.587317 |  0.77614  |
| LogisticRegression           |   0.703349 |            0.653774 |             0.753434 |          0.703349 |      0.721239 |   0.626096 |  0.732995 |
| DummyClassifier_MostFrequent |   0.779904 |            0.5      |             0.608251 |          0.779904 |      0.683465 |   0.438172 |  0.5      |
| DecisionTree                 |   0.617225 |            0.645372 |             0.753406 |          0.617225 |      0.650015 |   0.576237 |  0.731795 |



## H8. Best Baseline Model

- Best model: `GradientBoosting`

- Selection metric: `f1_weighted`

- Saved model path: `/content/student-success-ai/models/h_best_baseline_model.joblib`

## H9. Performance Warning Check

No near-perfect performance warning was triggered.

## H10. Saved Outputs

- Target distribution figure: `/content/student-success-ai/figures/h_target_distribution.png`

- Correlation heatmap: `/content/student-success-ai/figures/h_numeric_correlation_heatmap.png`

- Confusion matrix figure: `/content/student-success-ai/figures/h_best_baseline_confusion_matrix.png`

- Baseline model results CSV: `/content/student-success-ai/reports/modeling/h_baseline_model_results.csv`

- Best baseline model file: `/content/student-success-ai/models/h_best_baseline_model.joblib`

- Missing-value summary CSV: `/content/student-success-ai/reports/eda/h_missing_value_summary.csv`

- Data-type summary CSV: `/content/student-success-ai/reports/eda/h_dtype_summary.csv`

- Target summary CSV: `/content/student-success-ai/reports/eda/h_target_summary.csv`

- Classification reports JSON: `/content/student-success-ai/reports/modeling/h_classification_reports.json`

- Feature importance CSV: `/content/student-success-ai/reports/modeling/h_feature_importance.csv`

- Feature importance figure: `/content/student-success-ai/figures/h_feature_importance_top20.png`


## H11. Step H Completion Statement

Step H is completed. The strict leakage-controlled dataset was inspected, EDA outputs were generated, baseline machine learning models were trained, results were saved, and the best baseline model was stored for later comparison.
