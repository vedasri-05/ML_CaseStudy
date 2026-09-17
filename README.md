# Machine Learning Capstone Project

## 1. Project Overview

This project is developed as part of the 23CSE301 Machine Learning Capstone Project
for the academic year 2026-27.

The project implements machine learning techniques for both Regression and
Classification problems. The complete workflow includes data loading, exploratory
data analysis, preprocessing, feature engineering, model training, hyperparameter
tuning, evaluation, and comparison.

---

# 2. Regression Track

## 2.1 Problem Statement

The Regression task focuses on predicting household appliance energy consumption
using environmental and temporal features from the Household Energy Consumption
dataset.

### Target Variable

`Appliances`

## 2.2 Dataset

The dataset contains household energy consumption measurements together with
environmental and temporal features such as:

- Temperature measurements
- Humidity measurements
- Weather-related measurements
- Wind speed
- Visibility
- Pressure
- Time-related features

## 2.3 Data Preprocessing

The following preprocessing steps were performed:

- Missing-value checking
- Duplicate checking
- Date-time conversion
- Temporal feature extraction
- Cyclic feature engineering
- Outlier detection and treatment
- Train-test splitting
- Feature scaling where required

An 80:20 train-test split with `random_state=42` was used.

## 2.4 Regression Algorithms

The following ten regression algorithms were implemented:

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

## 2.5 Regression Evaluation Metrics

The regression models are evaluated using:

- R² Score
- RMSE
- MAE
- 5-Fold Cross-Validated R² for the two best-performing models

## 2.6 Regression Results

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

The Classification task focuses on identifying the type of network attack based
on network traffic flow characteristics.

The model learns patterns from network-flow features and predicts the corresponding
attack category.

### Target Variable

`Attack_type`

## 3.2 Dataset Description

The classification dataset contains **123,117 records and 85 columns**.

The dataset consists of network traffic flow features describing characteristics
of communication between network endpoints.

Important feature categories include:

- Source and destination port information
- Network protocol
- Service type
- Flow duration
- Forward and backward packet statistics
- Packet rates
- Header sizes
- TCP flag counts
- Packet payload statistics
- Inter-arrival time (IAT) statistics
- Payload bytes per second
- Subflow statistics
- Bulk traffic statistics
- Active and idle time statistics
- TCP window size features

The target column is:

`Attack_type`

## 3.3 Classification Preprocessing

The classification preprocessing pipeline includes:

- Dataset loading and inspection
- Checking missing values
- Checking duplicate records
- Identifying numerical and categorical features
- Encoding categorical features
- Feature scaling where required
- Train-test splitting
- Feature preparation for classification models

Care is taken to fit preprocessing transformations using the training data to
avoid data leakage.

## 3.4 Classification Algorithms – Part A

The following five classification algorithms are implemented for Review 1.

### 1. Logistic Regression

Logistic Regression is used as the baseline classification algorithm.
It predicts the probability of each class and provides model coefficients
that can be used to understand feature relationships with the predicted class.

### 2. K-Nearest Neighbors (KNN)

KNN classifies a data point based on the classes of its nearest neighbours.
The value of `k` is tuned during model development.

Since KNN is distance-based, feature scaling is important for obtaining
meaningful distance calculations.

### 3. Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classification algorithm based on
Bayes' theorem.

It assumes conditional independence between features and models continuous
features using Gaussian distributions.

### 4. Decision Tree Classifier

Decision Tree Classifier predicts the attack category by recursively splitting
the dataset according to feature values.

The `max_depth` parameter can be tuned to control the complexity of the tree.

### 5. Support Vector Machine (SVC)

Support Vector Classifier separates classes by finding an appropriate decision
boundary.

Feature scaling is applied before training. The `C` and `kernel` parameters
can be tuned to improve classification performance.

## 3.5 Classification Evaluation Metrics

The first five classification algorithms are evaluated using:

- Accuracy
- Weighted F1-score
- Confusion Matrix

The assignment specifically requires these metrics for Classification
Part A. 

## 3.6 Classification Results – Part A

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

For Regression, parameters such as:

- `alpha`
- `l1_ratio`
- `max_depth`
- `n_estimators`
- `learning_rate`
- `C`
- `kernel`
- `k`

are considered depending on the algorithm.

For Classification, parameters such as:

- `n_neighbors`
- `max_depth`
- `C`
- `kernel`

are tuned where applicable.

---

# 5. Technologies Used

- Python 3
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 6. Project Structure

```text
ML_CaseStudy/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── energydata.csv
│   └── classification_dataset.csv
│
└── notebooks/
    ├── regression.ipynb
    └── classification.ipynb