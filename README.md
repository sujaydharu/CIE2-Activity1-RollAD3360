# CIE 2 - Activity 1: Multiple Linear Regression Worksheet

**Student Name:** SujayRajendra Dharu  
**Roll Number:** [AD3360]  
**Course:** Regression and Classification Algorithms (T.Y. B.Tech AI & DS, Semester V)  
**Department:** Artificial Intelligence & Data Science, Zeal College of Engineering and Research, Pune  
**Submission GitHub ID:** [https://github.com/complexiota](https://github.com/complexiota)

---

# 📱 Mobile Phone Price Prediction

A Machine Learning project using **Linear Regression** to predict mobile phone prices based on hardware specifications and brand metadata. The pipeline features automated data cleaning, regular expression feature extraction, categorical encoding via `scikit-learn` Pipelines, and performance evaluation.

---

## 📌 Project Overview

This model processes unstructured metadata from modern mobile phone listings (such as multi-camera setup strings and formatted currency values) to build an end-to-end regression pipeline.

### Key Highlights:
- **Data Preprocessing**: Regular expressions to extract numerical values from strings (RAM, Storage, Screen Size, Camera Megapixels, and Price).
- **Feature Engineering**: Standardized extraction of primary camera specs from multi-lens configurations (e.g., `12 + 12 + 12`).
- **Scikit-Learn Pipeline**: Integrated `ColumnTransformer` with `OneHotEncoder` for categorical features (`Brand`) and `LinearRegression` estimation.
- **Evaluation**: Evaluated using $R^2$ Score, MAE, and RMSE metrics along with Actual vs. Predicted visualizations.

---

## 📊 Model Performance

Evaluated on a 20% hold-out test set ($80/20$ train-test split):

| Metric | Score / Value |
| :--- | :--- |
| **$R^2$ Score** | **0.7895** (78.95% variance explained) |
| **Mean Absolute Error (MAE)** | **\$89.88** |
| **Root Mean Squared Error (RMSE)** | **\$138.69** |

---

## 📁 Dataset & Features

The dataset (`Mobile phone price.csv`) consists of hardware specifications and pricing details across multiple smartphone brands.

- **Data Source**: [MobilePhonePrice.csv on GitHub (Senka2112/VIS2023-datasets)](https://github.com/Senka2112/VIS2023-datasets/blob/main/MobilePhonePrice.csv)

### Features Used:
- **`Brand`** *(Categorical)*: Manufacturer name (One-Hot Encoded).
- **`Storage`** *(Numerical, GB)*: Internal storage capacity extracted as float.
- **`RAM`** *(Numerical, GB)*: Memory capacity extracted as float.
- **`Screen Size (inches)`** *(Numerical)*: Display diagonal size in inches.
- **`Primary_Camera_MP`** *(Numerical)*: Primary sensor resolution extracted from raw camera specs.
- **`Battery Capacity (mAh)`** *(Numerical)*: Battery power capacity.

### Target Variable:
- **`Price ($)`** *(Numerical)*: Retail price in USD cleaned from string formatting.

---

## 🛠️ Technology Stack

- **Python 3.x**
- **Pandas** & **NumPy** for data manipulation and regular expression extraction.
- **Scikit-Learn** for modeling, preprocessing pipelines, and evaluation metrics.
- **Matplotlib** & **Seaborn** for data visualization.

---

## ⚙️ Installation & Usage

### 1. Requirements
Ensure you have the required dependencies installed:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
