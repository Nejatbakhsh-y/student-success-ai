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
