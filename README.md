# 🛍️ Prediction-of-Product-Sales

## Introduction

## 📌 Project Overview

This project focuses on predicting sales for a retail chain using historical data on products and outlet characteristics. The goal is to identify key factors that influence `Item_Outlet_Sales` to assist the business in inventory planning, pricing, and store strategy.

performed **exploratory data analysis (EDA)**, **data cleaning**, and prepared the dataset for machine learning models to help optimize sales across different products and store types.

## 🗂️ Dataset Description

The dataset includes the following key features:


- `Item_Weight`: Weight of the product
- `Item_Fat_Content`: Whether the product is low fat or regular
- `Item_Visibility`: The percentage of total display area of all products in a store allocated to 
                     the particular product
- `Item_Type`: Category to which the product belongs
- `Item_MRP`: Maximum retail price of the product
- `Outlet_Identifier`: Unique ID of the store
- `Outlet_Establishment_Year`: Year when the store was established
- `Outlet_Size`: Size of the store  in terms of ground area covered
- `Outlet_Location_Type`: The type of area in which the store is located
- `Outlet_Type`: Whether the store is a grocery store or supermarket
- `Item_Outlet_Sales`: **Target** variable — sales of the product in the given store

---

## 📊 Exploratory Data Analysis (EDA)

We used visualizations to better understand the relationships between variables and to identify data issues such as missing values or skewed distributions.

### 🔹 Histogram – `Item_MRP' (Item Maximum Retail Price)`
![Distribution of Item MRP](https://github.com/user-attachments/assets/54e5843f-5561-433d-b36b-d3911d49acee)

> **Interpretation**:Shows a multimodal distribution, revealing that products fall into several pricing tiers.

### 🔹 Histogram – `Item_Visibility`
![Distribution of Item Visibility](https://github.com/user-attachments/assets/0c1989cb-d83c-4e0e-95a0-b5f276893d27)

> **Interpretation**: The distribution of Item_Visibility is right-skewed, with many items having very low visibility and some even with values close to zero. This could suggest data entry errors or products not actively displayed, which might affect sales.

---

### 🔹 Boxplot – `Item_Outlet_Sales` by `Outlet_Type`
![Sales by Outlet Type](https://github.com/user-attachments/assets/4668a71e-4e4b-498d-b5ef-008243eeb67c)

> **Interpretation**: Boxplot of Sales by Outlet Type Reveals that “Supermarket Type 3” outlets generate higher median sales compared to other types.

---

### 🔹 Boxplot – `Item_Outlet_Sales` by `Outlet_Location_Type`
![Sales Distribution by Outlet Location Type](https://github.com/user-attachments/assets/0c714c1a-15e2-4bc7-8f52-045da63e35eb)


> **Interpretation**: Outlets in Tier 3 locations show higher variability and generally higher median sales than Tier 1 or 2. This might indicate greater customer traffic or purchasing power in Tier 3 regions, which can be useful for predictive modeling.

---

### 🔹 Countplot – `Outlet_Size`
![Outlet Size Distribution](https://github.com/user-attachments/assets/12d1ba82-81ae-4a7c-9fcd-37e04804d2ca)


> **Interpretation**: Most outlets are labeled as Medium, while Small outlets are slightly less common, and High size outlets are rare. There are also a significant number of missing values, which may require imputation or a dedicated category like 'Unknown .

---

### 🔹 Heatmap – Correlation Matrix
![Correlation Matrix](https://github.com/user-attachments/assets/b82f582f-2cf1-4c82-b20d-d04556ed0b7e)


> **Interpretation**: Item_MRP has a moderate positive correlation with Item_Outlet_Sales, making it a likely predictor. Other features like Item_Weight and Item_Visibility show weak or negligible correlations, suggesting they might need transformation or interaction terms to be predictive.

---

## 📓 Model Summary

A range of models were tested, including Linear Regression, Decision Trees, Random Forests, with extensive hyperparameter tuning. The final model was selected based on Root Mean Squared Error (RMSE) and its ability to generalize across store types.

---

## 📈 Evaluation Metrics

- Best Model: Random Forest model (tuned)

------------------------------------------------------------
Regression Metrics: Training Data
------------------------------------------------------------
- MAE = 653.621
- MSE = 868,731.344
- RMSE = 932.058
- R^2 = 0.706

------------------------------------------------------------
Regression Metrics: Test Data
------------------------------------------------------------
- MAE = 734.518
- MSE = 1,118,752.629
- RMSE = 1,057.711
- R^2 = 0.595













