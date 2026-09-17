# Machine Learning Capstone Project

## 1. Project Overview

This project is developed as part of the 23CSE301 Machine Learning Capstone Project.
The project implements machine learning techniques for Regression and Classification
problems using Python and Scikit-learn.

The project covers data preprocessing, exploratory data analysis, feature engineering,
model training, hyperparameter tuning, evaluation, and comparison of machine learning
algorithms.

---

# 2. Regression Track

## 2.1 Problem Statement

The Regression task focuses on predicting household appliance energy consumption
using environmental and temporal features from the household energy dataset.

### Target Variable
- `Appliances`

### Dataset
The dataset contains household energy consumption measurements along with
temperature, humidity, weather, and time-related features.

## 2.2 Data Preprocessing

The following preprocessing steps were performed:

- Missing-value checking
- Duplicate checking
- Date-time conversion
- Temporal feature extraction
- Cyclic time feature engineering
- Outlier detection and treatment
- Train-test splitting
- Feature scaling where required

An 80:20 train-test split with `random_state=42` was used.

## 2.3 Regression Algorithms

The following regression algorithms were implemented:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. ElasticNet Regression
5. Polynomial Regression
6. Decision Tree Regressor
7. Random Forest Regressor
8. Gradient Boosting Regressor
9. Support Vector Regressor (SVR)
10. K-Nearest Neighbors Regressor

All ten algorithms are evaluated using the same preprocessed dataset and held-out
test set as required by the project guidelines. 

## 2.4 Regression Evaluation Metrics

The models are evaluated using:

- R² Score
- RMSE
- MAE
- 5-Fold Cross-Validated R² for the two best-performing models

## 2.5 Regression Results

| Algorithm | R² Score | RMSE | MAE |
|-----------|----------|------|-----|
| Linear Regression | | | |
| Ridge Regression | | | |
| Lasso Regression | | | |
| ElasticNet | | | |
| Polynomial Regression | | | |
| Decision Tree | | | |
| Random Forest | | | |
| Gradient Boosting | | | |
| SVR | | | |
| KNN Regressor | | | |

---

# 3. Classification Track

## 3.1 Problem Statement

The Classification task focuses on predicting the class/category of the given
dataset using supervised machine learning classification algorithms.

## 3.2 Classification Preprocessing

The classification pipeline includes:

- Data loading and inspection
- Missing-value handling
- Duplicate checking
- Feature engineering
- Encoding of categorical features where required
- Feature scaling for distance- and margin-based models
- Train-test splitting

The same dataset and preprocessing approach are used for comparing the
classification algorithms.

## 3.3 Classification Algorithms – Part A

The following five classification algorithms are implemented for Review 1:

### 1. Logistic Regression

Logistic Regression is used as the baseline classification model.
It predicts class probabilities and can be used to interpret the effect of
features through model coefficients.

### 2. K-Nearest Neighbors (KNN)

KNN classifies a sample based on the classes of its nearest neighbours.
The value of `k` can be tuned, and feature scaling is important because
KNN uses distance calculations.

### 3. Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classifier based on Bayes' theorem.
It assumes conditional independence between features and models continuous
features using Gaussian distributions.

### 4. Decision Tree Classifier

Decision Tree Classifier predicts classes by recursively splitting the data
based on feature values. The `max_depth` parameter can be tuned to control
tree complexity.

### 5. Support Vector Machine (SVC)

Support Vector Classifier finds a decision boundary that separates classes.
The `C` and `kernel` parameters can be tuned. Feature scaling is applied
before training.

## 3.4 Classification Evaluation Metrics

For Part A, the models are evaluated using:

- Accuracy
- Weighted F1-score
- Confusion Matrix

The assignment specifically requires these metrics for the five Part-A
classification algorithms. :contentReference[oaicite:1]{index=1}

## 3.5 Classification Results – Part A

| Algorithm | Accuracy | Weighted F1 |
|-----------|----------|-------------|
| Logistic Regression | | |
| KNN | | |
| Gaussian Naive Bayes | | |
| Decision Tree | | |
| SVM (SVC) | | |

---

# 4. Hyperparameter Tuning

Hyperparameter tuning is performed using GridSearchCV or RandomizedSearchCV
where applicable.

The tuned parameters include:

- Regression model parameters such as `alpha`, `max_depth`, `n_estimators`,
  `learning_rate`, `C`, and `k`
- Classification parameters such as `k`, `max_depth`, `C`, and `kernel`

---

# 5. Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 6. Project Structure

ML_CaseStudy/
│
├── README.md
├── requirements.txt
├── data/
│   └── dataset files
│
└── notebooks/
    ├── regression.ipynb
    └── classification.ipynb









