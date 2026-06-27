# Student Success AI

## Project Title

Student Success AI: A Reproducible Benchmark for Early Academic Risk Prediction Using Explainable Machine Learning, with Public Educational Data

## Project Overview

This project develops a reproducible machine learning benchmark for early academic risk prediction using public educational data. The goal is to compare multiple machine learning algorithms, evaluate predictive performance, and explain model behavior using interpretable and explainable AI methods.

## Repository Structure

```text
student-success-ai/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_loading_colab.ipynb
│   ├── 02_eda_colab.ipynb
│   ├── 03_preprocessing_colab.ipynb
│   ├── 04_model_training_colab.ipynb
│   ├── 05_model_comparison_colab.ipynb
│   └── 06_explainability_colab.ipynb
├── src/
│   ├── data_loader.py
│   ├── preprocessing.py
│   ├── train_models.py
│   ├── evaluate_models.py
│   └── explainability.py
├── reports/
│   ├── figures/
│   ├── tables/
│   └── final/
└── docs/
    ├── model_card.md
    ├── data_card.md
    └── reproducibility.md
```

## Main Goals

1. Use a public educational dataset.
2. Build reproducible Google Colab notebooks.
3. Compare multiple machine learning algorithms.
4. Identify the best-performing algorithm.
5. Apply explainable AI methods.
6. Prepare GitHub-ready documentation for research and publication.

## Planned Algorithms

The project will compare logistic regression, decision tree, random forest, gradient boosting, support vector machine, K-nearest neighbors, and neural network models.

## Reproducibility

All experiments will be organized through Google Colab notebooks and reusable Python scripts.


## Open in Google Colab

Use the links below to open the main project notebooks in Google Colab.

| Notebook | Colab Link |
|---|---|
| Notebook 1: Data Loading | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/01_data_loading_colab.ipynb) |
| Notebook 2: EDA | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/02_eda_colab.ipynb) |
| Notebook 3: Preprocessing | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/03_preprocessing_colab.ipynb) |
| Notebook 4: Model Training | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/04_model_training_colab.ipynb) |
| Notebook 5: Model Comparison | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/05_model_comparison_colab.ipynb) |
| Notebook 6: Explainability | [Open in Colab](https://colab.research.google.com/github/Nejatbakhsh-y/student-success-ai/blob/main/notebooks/06_explainability_colab.ipynb) |


## Results and Model Discussion

This project builds a reproducible machine learning benchmark for early academic-risk and student-success prediction. The modeling workflow uses a strict cleaned dataset, excludes target-leakage columns, applies preprocessing through a machine-learning pipeline, and compares multiple algorithms.

The main research question is:

Which machine learning algorithm performs best for early academic risk and student-success prediction?

The repository is structured to save model-comparison tables, figures, final reports, and explainability outputs under the reports directory.

Key generated outputs include:

- reports/tables/project_workflow_summary.csv
- reports/tables/project_completion_audit.csv
- reports/figures/project_completion_status.png
- reports/final/final_project_report.md
- reports/final/project_completion_audit.md

## Reproducible Workflow

The project is organized for Google Colab and GitHub. The recommended workflow is:

1. Run the data-loading notebook.
2. Run EDA.
3. Run preprocessing.
4. Run model training.
5. Run model comparison.
6. Run explainability.
7. Save tables and figures.
8. Update reports.
9. Commit and push results to GitHub.
