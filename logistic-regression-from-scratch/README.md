# Logistic Regression from Scratch

A complete implementation of **Logistic Regression** from scratch using **NumPy**, without relying on machine learning libraries such as Scikit-learn.

This project was created for educational purposes to demonstrate the mathematical foundations of Logistic Regression, Gradient Descent optimization, and different regularization techniques.

---

# Features

- Logistic Regression implemented from scratch
- Batch Gradient Descent optimization
- Binary Classification
- Sigmoid Activation
- Cross-Entropy Loss
- L1 Regularization (Lasso)
- L2 Regularization (Ridge)
- Elastic Net Regularization
- Adjustable `lambda` (regularization strength)
- Adjustable `l1_ratio` for Elastic Net
- Configurable decision threshold
- Decision Function
- Probability Prediction (`predict_proba`)
- Accuracy Score
- Confusion Matrix
- Precision
- Recall
- F1 Score
- Training Loss Visualization
- Early Stopping
- Input Validation & Error Handling

---

# Dataset

- Wisconsin Breast Cancer Dataset
- Built-in dataset from **scikit-learn**
- Binary Classification

Target labels:

- **0 → Benign**
- **1 → Malignant**

---

# Regularization Experiments

The notebook compares three regularization techniques:

- No Regularization
- L1 Regularization
- L2 Regularization
- Elastic Net

Different values of **λ (lambda)** and **l1_ratio** are evaluated to compare:

- Accuracy
- Weight Norm
- Coefficient Sparsity
- Generalization Performance

---

# Results

The experiments show the expected behavior of each regularization method:

- **L2** reduces coefficient magnitude while preserving predictive performance.
- **L1** encourages sparse solutions by shrinking many coefficients toward zero.
- **Elastic Net** combines both approaches and achieved the best balance between model simplicity and classification accuracy.

The best configuration achieved:

- **Accuracy: 97.37%**
- Reduced coefficient norm
- Better generalization compared to using L1 or L2 alone.

---

# Project Structure

```
LogisticRegression.ipynb
README.md
```

---

# Requirements

```bash
pip install numpy matplotlib scikit-learn
```

---

# Example

```python
model = LogisticRegression(
    penalty="elasticnet",
    lambda_=100,
    l1_ratio=0.7
)

model.fit(X_train, y_train)

predictions = model.predict(X_test)

accuracy = model.score(X_test, y_test)
```

---

# Learning Objectives

This project demonstrates:

- Logistic Regression mathematics
- Gradient Descent optimization
- Cross-Entropy Loss
- L1 Regularization (Lasso)
- L2 Regularization (Ridge)
- Elastic Net Regularization
- Decision Thresholds
- Model Evaluation Metrics
- Generalization vs Overfitting
- Numerical Stability
- Object-Oriented Programming (OOP)

---


# License

This project is intended for educational purposes.