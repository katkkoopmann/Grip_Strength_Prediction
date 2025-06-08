Grip Strength Prediction using Regression and PCA

Project Overview

This project aims to predict **grip strength** using personal and lifestyle data. The dataset includes gender, age, height, weight, hand dominance, BMI, physical activity, and smoking habits.

Steps Performed

1. ** Data Preprocessing**

   * Removed the ID column.
   * Encoded categorical features.
   * Handled ordinal variables properly (physical activity & smoking).
   * Scaled continuous features.

2. ** Exploratory Data Analysis (EDA)**

   * Visualized distributions and correlations.
   * Checked multicollinearity.
   * Confirmed target (grip strength) had meaningful variance.

3. ** Dimensionality Reduction**

   * Applied **PCA** to reduce features and test model impact.

4. **Regression Models Tested**

   * Random Forest
   * K-Nearest Neighbors
   * ElasticNet Regression
   * XGBoost
   * Linear Regression
   * Gradient Boosting

5. ** Evaluation Metrics**

   * Mean Squared Error (MSE)
   * R² Score (Coefficient of Determination)

---

## Results Summary (with PCA)

| Model                 | MSE       | R² Score  |
| --------------------- | --------- | --------- |
| Linear Regression     | **45.38** | **0.588** |
| ElasticNet Regression | 54.50     | 0.505     |
| KNN                   | 59.25     | 0.462     |
| SVR                   | 62.56     | 0.432     |
| Random Forest         | 69.56     | 0.368     |
| Gradient Boosting     | 69.42     | 0.370     |
| XGBoost               | 98.76     | 0.103     |

---

## Short Analysis

* **Linear Regression** performed the best with PCA, achieving the lowest MSE and highest R² (≈0.59).
* **ElasticNet** also showed competitive performance and was more robust to overfitting.
* **Tree-based models (Random Forest, XGBoost)** did not benefit from PCA and performed worse.
* **PCA** helped improve performance for linear models but degraded performance in ensemble models due to information loss in high-dimensional splits.


