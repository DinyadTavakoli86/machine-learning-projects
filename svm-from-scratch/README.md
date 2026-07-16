# Support Vector Machine (SVM) From Scratch

A complete implementation of a **Linear Soft Margin Support Vector Machine (SVM)** from scratch using **NumPy** and **Stochastic Gradient Descent (SGD)**.

This project demonstrates the mathematical foundations of SVM, implements the optimization algorithm without using machine learning libraries, and compares the results with Scikit-learn's implementation.

---

## Features

* Linear Soft Margin SVM
* Hinge Loss
* L2 Regularization
* Stochastic Gradient Descent (SGD)
* Decision Function
* Prediction
* Accuracy Evaluation
* Decision Boundary Visualization
* Training Loss Visualization
* Comparison with Scikit-learn

---

## Mathematical Background

The notebook explains the core concepts behind Support Vector Machines, including:

* Hyperplane
* Margin
* Soft Margin
* Hinge Loss
* Objective Function
* Gradient Computation
* SGD Optimization

---

## Project Structure

* Theory and mathematical intuition
* SVM implementation from scratch
* Model training
* Performance evaluation
* Comparison with Scikit-learn
* Training Loss visualization
* Decision Boundary visualization

---

## Technologies

* Python
* NumPy
* Matplotlib
* Scikit-learn (only for comparison)

---

## Dataset

The project uses the **Iris** dataset from Scikit-learn.

For simplicity, the third class is removed, resulting in a binary classification problem.

---
## Project Structure

```text
svm-from-scratch/
│
├── images/
│   ├── SVM Decision Boundary.png
│   └── Training Loss (iris).png
├── README.md
└── svm_from_scratch.ipynb
```
---

## Results

The custom implementation achieves performance comparable to Scikit-learn's Linear SVM on the binary Iris dataset.

---

## Learning Objectives

This project was built to better understand:

* Maximum Margin Classification
* Support Vector Machines
* Convex Optimization
* Hinge Loss
* Gradient-Based Optimization
* Machine Learning Algorithms from Scratch

---

## Repository

This implementation is intended for educational purposes to demonstrate how a Linear Soft Margin SVM works internally without relying on high-level machine learning libraries.
