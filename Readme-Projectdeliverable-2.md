# MSCS_634_ProjectDeliverable_2

👨‍💻 **Student Name**: Chandra Kiran Billingi  
📚 **Course**: MSCS 634 - Advanced Big Data and Data Mining  

---


## 📊 Dataset Summary

The dataset contains various features related to used cars such as:

- **Numerical**: `year`, `km_driven`, `mileage`, `engine`, `max_power`, `seats`
- **Categorical**: `fuel`, `seller_type`, `transmission`, `owner`
- **Target**: `selling_price` (continuous variable)

The goal is to build regression models to **predict the car selling price** using these features.

---

## 🔧 Modeling Process

The following steps were implemented in the notebook:

1. **Data Cleaning & Preprocessing**:
   - Handled missing values and outliers using IQR technique.
   - Converted mixed-type columns (e.g. mileage: "20.4 kmpl") to numeric.
   - Applied one-hot encoding to categorical features.
   - Scaled numerical features using `StandardScaler`.

2. **Feature Engineering**:
   - Extracted numerical values from string-based fields.
   - Identified most relevant features based on correlation matrix.

3. **Modeling Techniques Used**:
   - ✅ Simple Linear Regression (1 feature)
   - ✅ Multiple Linear Regression (all features)
   - ✅ Ridge Regression (L2 regularization)
   - ✅ Lasso Regression (L1 regularization)

4. **Cross-Validation**:
   - 5-Fold Cross Validation was used to ensure generalization.
   - Evaluation metrics computed across all folds.


---

## ✅ Evaluation Summary

| Model                   | MAE     | RMSE    | R²     | Notes                                   |
|------------------------|---------|---------|--------|-----------------------------------------|
| Simple Linear Regression | High    | High    | Low    | Underfit — uses only one feature        |
| Multiple Linear Regression | Moderate| Moderate| Higher | Better fit, but no regularization       |
| Ridge Regression         | Low     | Low     | Best   | Best generalization, handles collinearity |
| Lasso Regression         | Comparable | Slightly Higher | Good | Good feature selection, interpretable   |

---

## 💡 Key Insights & Observations

- **Engine**, **max_power**, and **year** are the most influential predictors.
- **Ridge Regression** consistently performed best across all metrics.
- **Lasso** helped identify and eliminate non-informative features.
- Regularization improved performance over plain linear regression.

---

## ⚠️ Challenges Faced

- Some columns (e.g. `mileage`, `engine`) had non-numeric units which required parsing.
- Missing values in important columns like `max_power` were handled via imputation.
- Outliers in `selling_price` and `km_driven` distorted early model results — resolved via IQR filtering.

---
