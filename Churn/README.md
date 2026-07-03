# Customer Churn Prediction using Logistic Regression

A complete machine learning project for predicting customer churn using Logistic Regression with a strong focus on model interpretation, feature engineering, hyperparameter stability, and decision threshold optimization.

---

## Project Overview

Customer churn prediction is a binary classification problem where the objective is to identify customers who are likely to leave a service.

Rather than only maximizing accuracy, this project emphasizes minimizing the business cost of misclassification by optimizing the decision threshold based on False Negative and False Positive costs.

---

## Dataset

- Customer Churn Dataset
- Binary Classification
- Target:
  - **0 → Active Customer**
  - **1 → Churned Customer**

---

## Project Workflow

### 1. Data Exploration

- Dataset inspection
- Missing value analysis
- Target distribution
- Feature statistics

---

### 2. Feature Selection

Features were analyzed before model training to reduce redundancy.

The project includes:

- Correlation Analysis
- Logistic Regression Coefficient Analysis
- Removal of redundant variables
- Feature comparison before and after removal

Removed features include:

- longten
- tollten
- cardten
- loglong
- logtoll
- lninc

---

### 3. Multicollinearity Analysis

# Customer Churn Prediction using Logistic Regression

A complete machine learning project for predicting customer churn using Logistic Regression with a strong focus on model interpretation, feature engineering, hyperparameter stability, and decision threshold optimization.

---

## Project Overview

Customer churn prediction is a binary classification problem where the objective is to identify customers who are likely to leave a service.

Rather than only maximizing accuracy, this project emphasizes minimizing the business cost of misclassification by optimizing the decision threshold based on False Negative and False Positive costs.

---

## Dataset

- Customer Churn Dataset
- Binary Classification
- Target:
  - **0 → Active Customer**
  - **1 → Churned Customer**

---

## Project Workflow

### 1. Data Exploration

- Dataset inspection
- Missing value analysis
- Target distribution
- Feature statistics

---

### 2. Feature Selection

Features were analyzed before model training to reduce redundancy.

The project includes:

- Correlation Analysis
- Logistic Regression Coefficient Analysis
- Removal of redundant variables
- Feature comparison before and after removal

Removed features include:

- longten
- tollten
- cardten
- loglong
- logtoll
- lninc

---
### 3. Feature Reduction

Highly correlated and transformed variables were identified through dataset inspection and Logistic Regression coefficient analysis. Redundant features were removed to simplify the model while maintaining predictive performance.
---

### 4. Data Preprocessing

Pipeline implementation:

- StandardScaler
- Logistic Regression

---

### 5. Hyperparameter Optimization

GridSearchCV was performed over multiple train/test splits to evaluate the stability of the selected hyperparameters.

The search included:

- C
- Solver
- Penalty
- Class Weight

Performance metric:

- ROC-AUC

---

### 6. Hyperparameter Stability Analysis

Instead of relying on a single train/test split, GridSearchCV was repeated across multiple random states.

The project reports:

- Best parameter frequency
- Mean ROC-AUC
- Standard deviation
- Maximum ROC-AUC
- Minimum ROC-AUC

This provides a more reliable estimate of model robustness.

---

### 7. Final Model

The final model was trained using the selected hyperparameters.

Pipeline:

- StandardScaler
- Logistic Regression

---

### 8. ROC Analysis

Model discrimination performance was evaluated using:

- ROC Curve
- ROC-AUC Score

---

### 9. Precision-Recall Analysis

Precision-Recall Curve was used to evaluate performance under class imbalance.

---

### 10. Feature Importance

Model interpretability was achieved using standardized Logistic Regression coefficients.

Feature importance rankings are reported for all variables.

---

### 11. Threshold Optimization

Instead of using the default threshold (0.50), the optimal threshold was selected using Out-of-Fold predictions obtained through cross-validation.

Custom Cost Function:

```
Cost = 30 × False Negatives + False Positives
```

Thresholds from:

```
0.01 → 0.99
```

were evaluated.

---

### 12. Threshold Stability

Threshold optimization was repeated across multiple random train/test splits.

The notebook reports:

- Optimal Threshold
- Cross-validation Cost
- Test Cost
- False Negatives
- False Positives

along with

- Average Threshold
- Threshold Distribution
- Average Test Cost

---

### 13. Threshold Comparison

Confusion matrices and classification reports were compared using:

- Default Threshold (0.50)
- Optimized Threshold

to demonstrate the business trade-off between False Positives and False Negatives.

---

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Machine Learning Techniques

- Logistic Regression
- Standardization
- Pipeline
- GridSearchCV
- Stratified K-Fold Cross Validation
- Repeated Stratified K-Fold Cross Validation
- Cross-Validated Threshold Optimization
- Hyperparameter Stability Analysis
- ROC Analysis
- Precision-Recall Analysis
- Feature Importance Analysis
- Cost-Sensitive Classification
---

## Project Structure

```text
Churn/
│
├── Images/                                           # Figures used in the README
│   ├── Confusion Matrix (Default Threshold) and Confusion Matrix (Threshold=0.4).png
│   ├── False Negative and False Positive.png
│   ├── False Negative and False Positive Across Different Splits.png
│   ├── Feature Importance in Logistic Regression.png
│   └── ROC Curve (BestModel).png
│
├── Customer_Churn_Analysis.ipynb                                       # Complete machine learning workflow
├── ChurnData.csv                                     # Customer churn dataset
├── grid_search_stability.pkl                         # Cached GridSearchCV results
└── README.md                                         # Project documentation
```

---

## Results

The project demonstrates that:

- Hyperparameter selection is stable across different train/test splits.
- Feature reduction simplifies the model while preserving predictive performance.
- Decision threshold optimization significantly reduces costly False Negatives.
- Model evaluation should consider business objectives rather than accuracy alone.

---


---

## Author

**Dinyad Tavakoli**

Machine Learning Enthusiast

---

