# ❤️ Heart Disease Prediction using Support Vector Machine (SVM)

A complete end-to-end Machine Learning project for predicting heart disease using the **Heart Disease Dataset**.

The project follows a real-world machine learning workflow, including data exploration, preprocessing, model comparison, hyperparameter optimization, threshold tuning, and model explainability.

---

# Project Workflow

- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Scaling with Pipeline
- Baseline Model Comparison
- Hyperparameter Optimization (GridSearchCV)
- Model Stability Analysis
- Threshold Optimization
- Final Model Evaluation
- SHAP Explainability

---

# Dataset

**Task:** Binary Classification

**Target**

- **0 → No Heart Disease**
- **1 → Heart Disease**

The dataset contains clinical features commonly used for heart disease prediction, including patient demographics, laboratory measurements, and medical examination results.

---

# Models Evaluated

The following machine learning algorithms were compared:

- K-Nearest Neighbors (KNN)
- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (Linear Kernel)
- LinearSVC
- Support Vector Machine (RBF Kernel)

Evaluation metric:

- **F1-Score**

| Model | F1-Score |
|--------|---------:|
| KNN | 0.8633 |
| Logistic Regression | 0.8599 |
| Random Forest | 0.8595 |
| SVM (RBF) | 0.8629 |
| LinearSVC | 0.8571 |
| SVM (Linear) | 0.8503 |
| Decision Tree | 0.7915 |

Although KNN achieved the highest F1-Score, the difference between KNN and the RBF SVM was negligible. The Support Vector Machine with the RBF kernel was selected for the remainder of the project because of its strong generalization ability and suitability for binary medical classification.

---

# Hyperparameter Optimization

Hyperparameters were optimized using:

- GridSearchCV
- Repeated Stratified Cross Validation

The optimization process explored different values of:

- C
- Kernel
- Gamma
- Class Weight

The best model was selected based on the cross-validated performance.

---

# Threshold Optimization

Instead of using the default probability threshold of, multiple thresholds were evaluated.

A custom cost function was used to reduce **False Negatives**, since missing a patient with heart disease is significantly more costly than producing a False Positive.

---

# Model Explainability

The final SVM model was interpreted using **SHAP (SHapley Additive exPlanations)**.

SHAP was used to:

- Explain individual predictions
- Measure feature contributions
- Improve model transparency

---

# Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- SHAP

---

# Repository Structure

```
Heart-Disease/
│
├── Images/                                          
│   ├── Calibrated Model (Optimized Threshold =0.21) VS Default Model (Default Threshold).png
│   ├── Cost Curve.png
│   ├── SHAP Beeswarm Plot.png
│   ├── SHAP Bar Plot.png
│   └── ROC Curve (Default Model).png
│
├── Heart-Disease.ipynb
├── svm_grid_search_stability.pkl
├── README.md
├──
```

---

# Key Features

- Complete Machine Learning Pipeline
- Multiple Model Comparison
- Cross Validation
- GridSearchCV
- Pipeline-based Preprocessing
- Threshold Optimization
- SHAP Explainability
- Medical Classification Workflow

---


## Thank You

Thank you for visiting this repository.

I hope you found this project useful. Feedback and suggestions are always appreciated.