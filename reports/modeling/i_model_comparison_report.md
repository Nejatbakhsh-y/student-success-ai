# Step I Model Comparison Report

## 1. Purpose

Step I compares multiple machine learning algorithms for early academic risk / student-success prediction.

The main research question is:

**Which machine learning algorithm performs best for early academic risk / student-success prediction?**

## 2. Dataset

- Dataset used: `data/processed/student_success_ml_ready.csv`
- Number of rows: `1,044`
- Number of columns: `59`
- Target column: `student_success`
- Target classes: `[np.int64(0), np.int64(1)]`
- Encoded class mapping: `{'0': 0, '1': 1}`

## 3. Leakage Audit Status

The updated Step H leakage audit was completed before Step I.

**Leakage audit result: PASSED**

No direct leakage columns were detected in the feature set.

Audit file:

`reports/modeling/h_updated_leakage_audit_before_step_i.md`

## 4. Features

- Number of numeric features: `58`
- Number of categorical features: `0`
- Total model features: `58`

## 5. Algorithms Compared

The following scikit-learn algorithms were compared:

- Dummy Classifier
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Support Vector Machine
- K-Nearest Neighbors
- Neural Network / MLP

## 6. Cross-Validation Design

- Cross-validation folds: `5`
- Tuning cross-validation folds: `3`
- Primary tuning metric: `f1`
- Test size: `0.2`
- Random state: `42`

## 7. Cross-Validation Results

| model                  |   cv_accuracy_mean |   cv_accuracy_std |   cv_balanced_accuracy_mean |   cv_balanced_accuracy_std |   cv_precision_mean |   cv_precision_std |   cv_recall_mean |   cv_recall_std |   cv_f1_mean |   cv_f1_std |   cv_roc_auc_mean |   cv_roc_auc_std |
|:-----------------------|-------------------:|------------------:|----------------------------:|---------------------------:|--------------------:|-------------------:|-----------------:|----------------:|-------------:|------------:|------------------:|-----------------:|
| Random Forest          |             0.7892 |            0.0139 |                      0.5625 |                     0.0225 |              0.8026 |             0.0074 |           0.9677 |          0.0102 |       0.8774 |      0.0081 |            0.8139 |           0.0534 |
| Dummy Classifier       |             0.7796 |            0.0024 |                      0.5    |                     0      |              0.7796 |             0.0024 |           1      |          0      |       0.8762 |      0.0015 |            0.5    |           0      |
| K-Nearest Neighbors    |             0.7844 |            0.0076 |                      0.579  |                     0.0247 |              0.8096 |             0.0096 |           0.9462 |          0.0098 |       0.8725 |      0.0039 |            0.6541 |           0.0515 |
| Gradient Boosting      |             0.782  |            0.0241 |                      0.6299 |                     0.0388 |              0.8328 |             0.0155 |           0.9017 |          0.0246 |       0.8657 |      0.0157 |            0.7844 |           0.0328 |
| Neural Network / MLP   |             0.7713 |            0.0241 |                      0.567  |                     0.0403 |              0.8054 |             0.0168 |           0.9324 |          0.0301 |       0.8639 |      0.0154 |            0.7218 |           0.0718 |
| Decision Tree          |             0.7569 |            0.0111 |                      0.6417 |                     0.0331 |              0.8422 |             0.018  |           0.848  |          0.022  |       0.8446 |      0.0072 |            0.6417 |           0.0331 |
| Support Vector Machine |             0.7617 |            0.0289 |                      0.7146 |                     0.0581 |              0.8853 |             0.0314 |           0.7988 |          0.0131 |       0.8396 |      0.0175 |            0.807  |           0.0474 |
| Logistic Regression    |             0.7222 |            0.0269 |                      0.699  |                     0.0444 |              0.8849 |             0.0243 |           0.7404 |          0.0211 |       0.806  |      0.0185 |            0.7762 |           0.0479 |

## 8. Hyperparameter Tuning Results

| model                  |   best_cv_score | primary_metric   | best_params                                                                                                                     | tuned   |
|:-----------------------|----------------:|:-----------------|:--------------------------------------------------------------------------------------------------------------------------------|:--------|
| Gradient Boosting      |          0.8808 | f1               | {"model__subsample": 0.8, "model__n_estimators": 150, "model__max_depth": 2, "model__learning_rate": 0.01}                      | True    |
| Random Forest          |          0.8807 | f1               | {"model__n_estimators": 300, "model__min_samples_leaf": 1, "model__max_features": "log2", "model__max_depth": 10}               | True    |
| K-Nearest Neighbors    |          0.8797 | f1               | {"model__weights": "distance", "model__p": 1, "model__n_neighbors": 21}                                                         | True    |
| Neural Network / MLP   |          0.8782 | f1               | {"model__learning_rate_init": 0.005, "model__hidden_layer_sizes": [32, 16], "model__alpha": 0.001, "model__activation": "relu"} | True    |
| Support Vector Machine |          0.866  | f1               | {"model__kernel": "rbf", "model__gamma": "scale", "model__C": 10}                                                               | True    |
| Decision Tree          |          0.8263 | f1               | {"model__min_samples_split": 2, "model__min_samples_leaf": 2, "model__max_depth": null, "model__criterion": "entropy"}          | True    |
| Logistic Regression    |          0.811  | f1               | {"model__solver": "lbfgs", "model__penalty": "l2", "model__C": 0.01}                                                            | True    |
| Dummy Classifier       |        nan      | f1               | {}                                                                                                                              | False   |

## 9. Test-Set Model Comparison

| model                  |   test_accuracy |   test_balanced_accuracy |   test_precision |   test_recall |   test_f1 |   test_roc_auc |
|:-----------------------|----------------:|-------------------------:|-----------------:|--------------:|----------:|---------------:|
| K-Nearest Neighbors    |          0.7943 |                   0.5404 |           0.7941 |        0.9939 |    0.8828 |         0.7342 |
| Gradient Boosting      |          0.7943 |                   0.5638 |           0.803  |        0.9755 |    0.8809 |         0.7573 |
| Dummy Classifier       |          0.7799 |                   0.5    |           0.7799 |        1      |    0.8763 |         0.5    |
| Neural Network / MLP   |          0.7751 |                   0.4969 |           0.7788 |        0.9939 |    0.8733 |         0.6799 |
| Random Forest          |          0.7751 |                   0.5593 |           0.8021 |        0.9448 |    0.8676 |         0.7887 |
| Support Vector Machine |          0.7656 |                   0.6234 |           0.8314 |        0.8773 |    0.8537 |         0.7374 |
| Decision Tree          |          0.756  |                   0.6329 |           0.8373 |        0.8528 |    0.845  |         0.6366 |
| Logistic Regression    |          0.7033 |                   0.6616 |           0.8633 |        0.7362 |    0.7947 |         0.7402 |

## 10. Final Model Selection

The final saved model was selected using tuned cross-validation performance, not only test-set performance.

- Best final model selected by tuned CV `f1`: **Gradient Boosting**
- Top model on test F1: **K-Nearest Neighbors**
- Top test F1 score: `0.8828`

## 11. Saved Outputs

Step I created the following outputs:

- `reports/modeling/i_model_comparison_results.csv`
- `reports/modeling/i_cross_validation_results.csv`
- `reports/modeling/i_hyperparameter_tuning_results.csv`
- `reports/modeling/i_model_comparison_report.md`
- `models/i_best_tuned_model.joblib`
- `figures/i_model_comparison_f1.png`
- `figures/i_model_comparison_auc.png`

## 12. Conclusion

Step I completed advanced model comparison and hyperparameter tuning. The next recommended step is:

**J. Explainable AI and feature importance analysis**
