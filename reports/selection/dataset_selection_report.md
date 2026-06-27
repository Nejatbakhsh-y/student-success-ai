# E. Public Educational Dataset Selection Report

## E1. Selected Dataset

The selected dataset for the first GitHub version of this project is the UCI Student Performance Dataset.

## E2. Project Title

Student Success AI: A Reproducible Benchmark for Early Academic Risk Prediction Using Explainable Machine Learning, with Public Educational Data

## E3. Dataset Source

- Dataset name: UCI Student Performance Dataset
- Repository: UCI Machine Learning Repository
- Dataset page: https://archive.ics.uci.edu/dataset/320/student+performance
- Direct ZIP download URL: https://archive.ics.uci.edu/static/public/320/student+performance.zip

## E4. Reason for Selection

The UCI Student Performance Dataset is selected because it is public, well-known in educational data mining, compact enough for Google Colab, and suitable for supervised machine learning.

This dataset is appropriate for the first version of the GitHub project because it allows the project to focus on reproducibility, clean machine learning workflow design, model comparison, and explainability without the heavy complexity of very large international datasets.

## E5. Research Suitability

The dataset supports the main goals of this project:

1. Early academic risk prediction.
2. Student success classification.
3. Final-grade regression.
4. Benchmark comparison across multiple machine learning algorithms.
5. Explainable machine learning analysis.
6. Reproducible documentation for GitHub and research development.

## E6. Recommended First Modeling Target

For the first classification benchmark, the recommended target is:

student_success = 1 if G3 >= 10, otherwise 0

The column G3 represents the final grade. It may be used to create the target, but it must be removed from the predictor variables before model training to avoid target leakage.

## E7. Recommended Raw File

The recommended first file for modeling is student-mat.csv.

The Portuguese-language course file, student-por.csv, may also be used later.

## E8. Future Research Extension

For a stronger research-level benchmark, the project can later be expanded to the PISA 2022 public-use dataset. PISA 2022 is more complex and more suitable for publication-level benchmarking, but the UCI dataset is better for the first complete GitHub version.

## E9. Step E Completion Statement

Step E is completed. The public educational dataset has been selected and documented. The dataset source manifest, dataset configuration file, dataset selection report, and data card have been created.
