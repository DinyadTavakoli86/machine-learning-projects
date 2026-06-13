# Drug200 Decision Tree Classification

## Overview

This project uses the Drug200 dataset to build a Decision Tree classifier capable of predicting the appropriate drug based on patient characteristics.

The notebook covers the complete machine learning workflow, including data preprocessing, feature encoding, model training, hyperparameter tuning, evaluation, and model persistence.

---

## Dataset

The dataset contains the following features:

* Age
* Sex
* Blood Pressure (BP)
* Cholesterol
* Na_to_K ratio

Target variable:

* Drug

The objective is to predict the prescribed drug category for a patient.

---

## Techniques Used

* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Label Encoding
* One-Hot Encoding
* Decision Tree Classifier
* GridSearchCV
* Pipeline
* Joblib

---

## Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report
* Feature Importance Analysis

Hyperparameter tuning was performed using GridSearchCV.

### Best Parameters

* max_depth = 4
* min_samples_split = 2
* min_samples_leaf = 1

The final model achieved approximately **98% accuracy** on the test dataset.

---

## Project Workflow

1. Data Exploration
2. Data Preprocessing
3. Feature Encoding
4. Train-Test Split
5. Hyperparameter Tuning
6. Model Training
7. Model Evaluation
8. Feature Importance Analysis
9. Model Persistence

---

## Files

* `Drug200_portfolio_enhanced.ipynb` – Main notebook
* `drug_model.pkl` – Trained model
* `README.md` – Project documentation

---

## Author

Dinyad Tavakoli

