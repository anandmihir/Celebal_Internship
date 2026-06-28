# 🌍 Customer Intelligence System using Unsupervised Learning

## 📌 Overview

This project was completed as part of the **Celebal Technologies Data Science Internship**. The objective is to analyze socio-economic indicators of different countries using **Unsupervised Machine Learning** techniques to discover meaningful patterns and group similar countries based on their development characteristics.

The project includes data preprocessing, feature scaling, K-Means clustering, DBSCAN clustering, PCA visualization, and cluster evaluation using the Silhouette Score.

---

## 🎯 Problem Statement

Develop an end-to-end Customer Intelligence System using clustering techniques to identify meaningful country segments based on socio-economic indicators. The project focuses on data preprocessing, cluster optimization, visualization, and generating actionable insights.

---

## 📂 Dataset

**Dataset:** Country-data.csv

The dataset contains socio-economic and health-related indicators such as:

- Child Mortality
- Exports
- Health Spending
- Imports
- Income
- Inflation
- Life Expectancy
- Total Fertility
- GDP per Capita (GDPP)

---

## 🛠️ Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📊 Machine Learning Techniques

### Data Preprocessing

- Removed duplicate records
- Trimmed column names
- Converted columns to numeric values
- Handled missing values using median imputation
- Standardized features using StandardScaler

### Clustering Algorithms

- K-Means Clustering
- DBSCAN Clustering

### Dimensionality Reduction

- Principal Component Analysis (PCA)

### Model Evaluation

- Elbow Method
- Silhouette Score

---

## 📈 Workflow

1. Import required libraries
2. Load the dataset
3. Clean and preprocess the data
4. Scale numerical features
5. Determine the optimal number of clusters using the Elbow Method
6. Train the K-Means model
7. Evaluate clustering performance using the Silhouette Score
8. Compare results with DBSCAN
9. Reduce dimensions using PCA
10. Visualize country clusters
11. Generate socio-economic insights

---

## 📊 Results

- Optimal number of clusters: **3**
- Clustering Algorithm: **K-Means**
- Comparative Model: **DBSCAN**
- Evaluation Metric: **Silhouette Score**
- Visualization: **2D PCA Scatter Plot**

The clustering successfully grouped countries into three major development categories:

- Developed Countries
- Developing Countries
- Underdeveloped Countries

---

## 🔍 Key Insights

- Cluster 1 contains countries with the highest child mortality and lowest economic indicators.
- Cluster 0 represents highly developed countries with the highest income and GDP per capita.
- Cluster 2 consists of developing countries with moderate socio-economic performance.
- Underdeveloped countries identified through clustering can be prioritized for international aid and policy planning.

---

## 🚀 How to Run

1. Clone this repository.

```
git clone https://github.com/your-username/your-repository-name.git
```

2. Open the notebook in Google Colab or Jupyter Notebook.

3. Install the required libraries.

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Upload the dataset.

5. Run all notebook cells sequentially.

---

## 📚 Learning Outcomes

- Data Cleaning
- Feature Engineering
- Data Standardization
- K-Means Clustering
- DBSCAN Clustering
- PCA
- Cluster Evaluation
- Data Visualization
- Socio-economic Data Analysis

---

## 👨‍💻 Author

**Mihir Anand**

Data Science Intern  
Celebal Technologies

---

## ⭐ Acknowledgements

This project was completed as part of the **Celebal Technologies Data Science Internship Program** to gain practical experience in **Unsupervised Machine Learning**, **Customer Intelligence**, and **Data Analytics**.
