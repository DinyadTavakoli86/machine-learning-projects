# Machine Learning Projects

This repository contains machine learning projects implemented using Python and scikit-learn. The projects cover the implementation of machine learning algorithms, classification tasks, data preprocessing, and model evaluation.

## Projects

### 1. KNN From Scratch

* Implementation of the K-Nearest Neighbors (KNN) algorithm without using machine learning libraries.
* Demonstrates distance calculation, neighbor selection, and majority voting.
* Built to understand the core concepts behind the KNN algorithm.

### 2. Iris Classification

* Classification using the Iris dataset.
* Train-test split and model evaluation.
* Investigation of the effect of feature scaling on KNN performance.
* Comparison of different distance metrics, including Euclidean, Manhattan, and Cosine distance.

### 3. MNIST KNN Classification

* Handwritten digit classification using the MNIST dataset.
* Comparison of different values of K.
* Evaluation of multiple distance metrics:

  * Euclidean
  * Manhattan
  * Cosine
  * Chebyshev
* Comparison of search algorithms:

  * Auto
  * Brute Force
  * KD-Tree
* Best Accuracy: 93.37%

## Dataset

This project uses the MNIST dataset in CSV format.

Dataset source:

https://github.com/phoebetronic/mnist

Required files:

* mnist_train.csv
* mnist_test.csv

After downloading the dataset, place both files in the project directory before running the notebook.

**Note:** To reduce computation time, only 10,000 samples from the original 60,000 training images were used in the experiments.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
