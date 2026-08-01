# Lead Scoring Prediction System

## Overview

The Lead Scoring Prediction System is a Machine Learning web application developed to predict whether a potential customer (lead) is likely to convert into a paying customer.

The application analyzes customer interaction data such as website visits, time spent on the website, page views, occupation, lead source, and last activity to estimate the probability of conversion.

The system is built using a Scikit-learn Pipeline and deployed using Streamlit for real-time predictions through an interactive web interface.

---

## Features

- Predict lead conversion in real time
- Display conversion probability
- Generate lead score (0–100)
- Categorize lead quality (High, Medium, Low)
- Interactive prediction dashboard
- Model performance dashboard
- About page with application details
- Downloadable project report
- Responsive multi-page Streamlit application
- Modular project structure using the `src` package

---

## Technologies Used

### Programming Language

- Python

### Machine Learning

- Scikit-learn
- Logistic Regression
- Pipeline
- StandardScaler
- ColumnTransformer
- OneHotEncoder

### Data Processing

- Pandas
- NumPy

### Web Framework

- Streamlit

### Visualization

- Matplotlib

---

## Project Structure

```text
LEADSCORING_PROJECT
│
├── app
│   ├── app.py
│   └── pages
│       ├── About.py
│       ├── Model_Performance.py
│       └── Predict.py
│
├── data
│   └── Lead Scoring.csv
│
├── models
│   ├── frontend_columns.pkl
│   ├── frontend_model.pkl
│   ├── frontend_scaler.pkl
│   ├── lead_pipeline.pkl
│   ├── lead_scoring_model.pkl
│   └── scaler.pkl
│
├── notebooks
│   └── LeadScoring.ipynb
│
├── src
│   ├── __init__.py
│   ├── preprocessing.py
│   ├── predictor.py
│   ├── metrics.py
│   └── utils.py
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Machine Learning Workflow

```text
User Input
     │
     ▼
Data Preprocessing
     │
     ▼
Feature Scaling & Encoding
     │
     ▼
Logistic Regression Pipeline
     │
     ▼
Probability Prediction
     │
     ▼
Lead Score Generation
     │
     ▼
Prediction Result
```

---

## Application Pages

### Home

Displays:

- Project Overview
- Application Features
- Technologies Used
- Prediction Workflow

---

### About

Provides information about:

- Application Purpose
- Dataset
- Features Used
- Project Objectives
- Download Project Report

---

### Predict

Allows users to enter:

- Total Visits
- Time Spent on Website
- Page Views Per Visit
- Occupation
- Lead Source
- Last Activity

The application then displays:

- Prediction Result
- Conversion Probability
- Lead Score
- Lead Quality
- Lead Details

---

### Model Performance

Displays:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Classification Report
- Confusion Matrix
- Model Interpretation

---

## Model Performance

| Metric | Value |
|---------|-------|
| Accuracy | 93.01% |
| Precision | 92.06% |
| Recall | 89.61% |
| F1 Score | 90.82% |
| ROC-AUC | 92.38% |

---

## Dataset

The project uses the Lead Scoring dataset containing customer interaction and website engagement information.

### Input Features

- Total Visits
- Total Time Spent on Website
- Page Views Per Visit
- Occupation
- Lead Source
- Last Activity

### Target Variable

| Value | Description |
|------:|-------------|
| 1 | Converted |
| 0 | Not Converted |

---

## Installation

### Clone the repository

```bash
git clone https://github.com/<your-username>/LeadScoring_Project.git
```

### Navigate to the project

```bash
cd LeadScoring_Project
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the application

```bash
streamlit run app/app.py
```

---

## Prediction Output

The application generates:

- Lead Conversion Prediction
- Conversion Probability
- Lead Score
- Lead Quality Classification
- Input Summary

---

## Future Enhancements

- User Authentication
- Prediction History
- Database Integration
- Cloud Deployment
- Admin Dashboard
- Explainable AI (SHAP/LIME)
- Automated Model Retraining

---

## Author

**Mihir Anand**

Lead Scoring Prediction System

---

## License

This project is intended for educational and learning purposes.
