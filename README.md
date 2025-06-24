# MSCS 634 - Lab 4: Regression Analysis with Regularization Techniques

## 👨‍💻 Student Name
Chandra Kiran Billingi

## 📚 Course
MSCS 634 - Advanced Big Data and Data Mining

## 🧪 Lab Overview

In this lab, I have explored a variety of regression techniques using the **Diabetes dataset** from `sklearn.datasets`. The primary objective was to understand how different types of regression models behave, compare their predictive performance, and analyze the impact of **regularization techniques** on model complexity and overfitting.

I have  implemented:

- Simple Linear Regression (with one feature)
- Multiple Linear Regression (with all features)
- Polynomial Regression (degree 2 and higher)
- Ridge Regression (L2 regularization)
- Lasso Regression (L1 regularization)

Performance was evaluated using common regression metrics:  
**MAE**, **MSE**, **RMSE**, and **R² (coefficient of determination)**.

---

## 🧾 Step-by-Step Breakdown

### 📌 Step 1: Data Preparation
- Loaded the Diabetes dataset using `load_diabetes()` from scikit-learn.
- Explored the features and target distribution.
- Checked for missing values (none found, so no cleaning required).
- Split the dataset into training and testing sets.

---

### 📌 Step 2: Simple Linear Regression
- Used a single feature: `'bmi'`, based on its strong correlation with the target.
- Trained a basic linear regression model.
- Visualized predictions vs actual values.
- Observed limited performance due to underfitting.

---

### 📌 Step 3: Multiple Linear Regression
- Used all 10 features in the dataset to train the model.
- Performance significantly improved compared to simple linear regression.
- Demonstrated better generalization and lower error metrics.

---

### 📌 Step 4: Polynomial Regression
- Extended the linear regression model using polynomial features (degree = 2).
- Helped capture non-linear relationships in the data.
- Showed improved R² score compared to linear models.
- Also demonstrated how higher-degree polynomials (3–5) can lead to **overfitting**.

---

### 📌 Step 5: Ridge and Lasso Regression
- Implemented both Ridge (L2) and Lasso (L1) regularization methods.
- Trained models using `alpha = 1.0` for both.
- Ridge helped shrink coefficients without setting them to zero, reducing overfitting.
- Lasso provided feature selection by eliminating less important features.
- Compared visually and with evaluation metrics.

---

### 📊 Step 6: Model Comparison & Analysis

- **Best General Performance**: Multiple Linear Regression / Ridge
- **Best Feature Reduction**: Lasso Regression
- **Worst Performance**: Simple Linear Regression (underfitting)

---

## 💡 Key Insights

- The `'bmi'` feature alone has predictive power, but not enough to build a strong model.
- Using all features significantly improves model performance.
- Polynomial features (degree = 2) enhance model flexibility, but require caution to avoid overfitting.
- Regularization (especially Ridge) can help stabilize models and reduce overfitting.
- Lasso is useful for **automatic feature selection**, especially with sparse or high-dimensional data.

---

## 🛠️ Errors & Troubleshooting

- **Understanding Lasso and Ridge Regularization**: Initially, it was challenging to grasp how L1 and L2 penalties work internally. The concept of **shrinking coefficients** and the effect of `alpha` required extra study.
- **Lasso Regression Code**: While implementing Lasso, several errors occurred due to convergence issues and incorrect parameter usage.
- **Alpha Parameter**: Choosing the right `alpha` value required experimentation. Too high an alpha caused underfitting, while too low made regularization ineffective.
- **Polynomial Regression**: Trying higher degrees (e.g., 4 or 5) caused overfitting and high variance. Best results came from degree 2.

---

## 📁 Files in this Repository

- `Lab4_Regression_Models.ipynb` – Main Jupyter Notebook with all code, graphs, and results.
- `README.md` – This file summarizing the lab work, results, and reflections.

---
