# Week 2 Assignment – Tesla Deliveries Machine Learning Pipeline

## Overview

This project was completed as part of the **Celebal Technologies Data Science Internship – Week 2 Assignment**. The objective was to design and implement an end-to-end Machine Learning pipeline using a Tesla deliveries dataset. The project covers the complete workflow from data preprocessing and exploratory data analysis (EDA) to feature engineering, regression modeling, hyperparameter tuning, and time series analysis.

---

## Objectives

- Load and explore the Tesla deliveries dataset.
- Perform data cleaning and preprocessing.
- Conduct Exploratory Data Analysis (EDA) using visualizations.
- Engineer new features to improve model performance.
- Train and evaluate Linear Regression and Random Forest models.
- Optimize the Random Forest model using GridSearchCV.
- Perform 5-Fold Cross Validation.
- Analyze feature importance.
- Test time series stationarity using the Augmented Dickey-Fuller (ADF) Test.
- Compare model performance and generate delivery forecasts.

---

## Dataset

**Dataset:** `tesla_deliveries_dataset_2015_2025.csv`

The dataset contains Tesla delivery-related information, including:

- Year
- Month
- Region
- Model
- Estimated Deliveries
- Production Units
- Average Price (USD)
- Battery Capacity
- Vehicle Range
- CO₂ Saved
- Source Type
- Charging Stations

---

## Project Workflow

### 1. Data Loading
- Loaded the dataset using Pandas.
- Explored dataset shape, columns, and summary statistics.

### 2. Data Preprocessing
- Checked for missing values.
- Removed duplicate records.
- Encoded categorical variables using LabelEncoder.

### 3. Exploratory Data Analysis (EDA)
Created the following visualizations:

- Deliveries by Model
- Deliveries by Region
- Correlation Heatmap
- Production Units vs Estimated Deliveries
- Tesla Deliveries Time Trend

### 4. Feature Engineering
Created new features:

- Deliveries_Lag1
- Rolling_Mean_3

### 5. Machine Learning Models

#### Linear Regression
- Chronological 80:20 Train-Test Split
- Model Training
- Model Evaluation

#### Random Forest Regression
- GridSearchCV Hyperparameter Tuning
- Best Model Selection
- Feature Importance Analysis

### 6. Model Evaluation

Evaluation Metrics:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### 7. Cross Validation

- 5-Fold Cross Validation
- Mean R² Score
- Standard Deviation

### 8. Time Series Analysis

- Augmented Dickey-Fuller (ADF) Stationarity Test
- Interpretation of p-value

### 9. Forecasting

Generated a comparison table containing:

- Actual Values
- Predicted Values
- Error Percentage

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels

---

## Files Included

- `week2_Mihir_Anand.ipynb` – Complete Google Colab Notebook
- `tesla_deliveries_dataset_2015_2025.csv` – Dataset used for analysis

---

## Learning Outcomes

Through this project, I gained practical experience in:

- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- Regression Modeling
- Hyperparameter Tuning
- Cross Validation
- Time Series Analysis
- Model Evaluation
- Forecasting

---

## Conclusion

This project demonstrates a complete end-to-end machine learning workflow for predicting Tesla deliveries. By combining data preprocessing, feature engineering, regression modeling, hyperparameter tuning, and time series analysis, the project provides valuable insights into delivery trends and model performance. The Random Forest model achieved better predictive performance compared to Linear Regression, making it the preferred model for this dataset.
