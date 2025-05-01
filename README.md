# SVM Optimization Using Gradient and Subgradient Descent

This project demonstrates the implementation of a Support Vector Machine (SVM) from scratch using both gradient descent and subgradient descent optimization techniques. The notebook includes data preprocessing, model training, hyperparameter tuning, and performance evaluation.

## Table of Contents
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Model Implementation](#model-implementation)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Performance Evaluation](#performance-evaluation)
- [Results](#results)
- [How to Run](#how-to-run)

## Dataset
The dataset used in this project is the **Banknote Authentication Dataset** from the UCI Machine Learning Repository. It contains features extracted from images of banknotes and their corresponding class labels.

- **Features**: Variance, skewness, kurtosis, and entropy of wavelet-transformed images.
- **Target**: Binary classification (authentic or forged).

## Project Workflow
1. **Data Import**: The dataset is fetched using the `ucimlrepo` library.
2. **Data Exploration**: Includes visualization of feature distributions and correlations.
3. **Data Preprocessing**:
   - Normalization of features.
   - Conversion of labels to {-1, +1} for SVM compatibility.
4. **Train-Test-Validation Split**: The dataset is split into training, validation, and test sets.

## Model Implementation
The SVM is implemented from scratch with the following features:
- **Loss Functions**:
  - Hinge loss for subgradient descent.
  - Smooth hinge loss for gradient descent.
- **Optimization Techniques**:
  - Subgradient descent.
  - Gradient descent.
- **Hyperparameters**:
  - Regularization parameter (λ).
  - Learning rate.
  - Maximum iterations.
  - Delta (for smooth hinge loss).

## Hyperparameter Tuning
A grid search is performed to find the best combination of hyperparameters for both optimization techniques. The best configuration is selected based on validation accuracy.

## Performance Evaluation
The model is evaluated using:
- Training, validation, and test accuracy.
- Loss curves for both optimization techniques.
- Confusion matrices.
- Precision and recall metrics.

## Results
- Subgradient descent achieves better stability and generalization on the test set.
- Gradient descent converges faster but has higher loss variance.
- Comparative analysis of decision boundaries and performance metrics is provided.

## How to Run
1. Install the required dependencies:
   ```bash
   pip install ucimlrepo numpy pandas matplotlib seaborn
