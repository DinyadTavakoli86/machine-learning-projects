# Breast Cancer Classification using Logistic Regression

Machine Learning project for breast cancer diagnosis using the Wisconsin Breast Cancer Dataset.

The project focuses not only on building a high-performance classifier, but also on selecting robust hyperparameters, optimizing the decision threshold, and minimizing False Negatives (FN), which are particularly important in medical diagnosis.

---

# Dataset

- **Wisconsin Breast Cancer Diagnostic Dataset**
- Source: `sklearn.datasets.load_breast_cancer`
- The `breast_cancer.csv` file included in this repository is an exported version of the original scikit-learn dataset for easier inspection.
- Binary Classification
- Target:
  - `0` → Benign
  - `1` → Malignant
---

# Project Workflow

### 1. Data Preprocessing

- Train / Validation / Test Split
- StandardScaler
- Feature Scaling

---

### 2. Model Comparison

Several machine learning algorithms were evaluated using **5-Fold Cross Validation** with **ROC-AUC** as the evaluation metric.

Models compared:

- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)

Logistic Regression achieved the highest ROC-AUC score and was therefore selected as the final model.

---

### 3. Hyperparameter Tuning

GridSearchCV was applied using **ROC-AUC** scoring.

The search included:

- Solver
- Penalty
- Class Weight
- ElasticNet parameters
- Regularization Strength (C)

To reduce the influence of a single train/test split, experiments were repeated using **20 different random states**.

Average performance across all splits was used to evaluate model robustness.

---

### 4. Final Model Selection

The following Logistic Regression model achieved the best overall balance between:

- Accuracy
- ROC-AUC
- False Negatives
- False Positives

```python
LogisticRegression(
    C=1,
    solver="liblinear",
    penalty="l2",
    class_weight={0:1,1:3},
    max_iter=10000
)
```

---

### 5. Feature Importance

Feature importance was analyzed using the magnitude of Logistic Regression coefficients.

The most influential features were identified by sorting the absolute coefficient values.

---

### 6. Threshold Optimization

The default decision threshold (0.5) was compared against optimized thresholds using two different approaches.

#### • Youden's J Statistic

Threshold selected by maximizing

TPR − FPR

This method improves the balance between sensitivity and specificity.

---

#### • Cost-Sensitive Threshold

Because missing a cancer patient is much more serious than generating a false alarm, a custom cost function was used.

```
Cost = 100 × FN + 1 × FP
```

Thresholds were selected on the validation set by minimizing this cost.

---

### 7. Robustness Evaluation

Threshold optimization was evaluated across **20 different train/test splits**.

Average False Negatives and False Positives were compared between:

- Default Threshold
- Cost-Sensitive Threshold

Results showed that:

- False Negatives decreased on average.
- False Positives increased slightly.
- Since this is a medical diagnosis problem, reducing False Negatives is considered more important than minimizing False Positives.

---

# Evaluation Metrics

The following metrics were used throughout the project:

- Accuracy
- ROC-AUC
- Confusion Matrix
- Precision
- Recall
- F1-score
- False Positive (FP)
- False Negative (FN)

---

# Libraries

- NumPy
- Pandas
- Matplotlib
- Scikit-Learn

---

## Project Structure

```text
Breast_Cancer_Classification/
│
├── breast_cancer_classification.ipynb   # Complete machine learning workflow
├── breast_cancer.csv                    # Breast Cancer Wisconsin dataset
├── grid_search_results.pkl              # Saved experimental results
├── README.md                            # Project documentation
│
└── Images/
    ├── feature_importance.png
    ├── confusion_matrix.png
    ├── roc_curve.png
    ├── fn_default_vs_fn_cost.png
    └── fn_fp_comparison.png
```

---

# Key Takeaways

- Logistic Regression outperformed the other evaluated models.
- Hyperparameters were selected using GridSearchCV with ROC-AUC scoring.
- Model robustness was verified across multiple random train/test splits.
- Cost-Sensitive threshold optimization successfully reduced False Negatives.
- In medical diagnosis, minimizing False Negatives is more important than minimizing False Positives.

---

## Conclusion

### Logistic Regression achieved the best overall performance among the evaluated models.

Through repeated train/test splits, hyperparameter tuning, threshold optimization, and cost-sensitive evaluation, the final model demonstrated stable performance while minimizing False Negatives, making it suitable for breast cancer classification tasks where missing a positive case is particularly costly.
---

## Author

Dinyad Tavakoli