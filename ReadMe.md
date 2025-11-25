
# Customer Segmentation Project (Unsupervised Learning)

Final Project — Unsupervised Algorithms in Machine Learning
Name: Alexander Voit

---

# Table of Contents

1. Problem Statement
2. Dataset Overview
3. Project Structure
4. Methods Used
5. EDA Summary
6. Results and Findings
7. How to Run
8. Deliverables
9. Final Thoughts

---

# 1. Problem Statement

The goal of this project is to identify meaningful customer segments using unsupervised learning.
Since the dataset contains no labels, the objective is to uncover natural patterns in customer behavior using three features:

* Age
* Annual Income
* Spending Score

After clustering the customers, I used simple supervised models to validate whether spending behavior can be predicted from age and income.
This step helps confirm that the unsupervised clusters reflect real behavioral structure in the dataset.

This project includes:

* EDA
* Multiple unsupervised models
* Model comparison
* Hyperparameter tuning
* Conclusions and interpretation
* Notebook, video presentation, and GitHub repository

---

# 2. Dataset Overview

Dataset: Mall Customers
Rows: 200
Columns: 5

Features used for modeling:

* Age
* Annual Income (k$)
* Spending Score (1–100)

There are no missing values.
The dataset is clean and appropriate for clustering tasks.

---

# 3. Project Structure

project/

* mall_customers_clustering.ipynb (main notebook)
* Mall_Customers.csv (dataset)
* README.md (project documentation)
* video_presentation.mp4 (final presentation)

The notebook contains:

* Exploratory Data Analysis
* K-Means clustering
* Elbow method
* Silhouette score analysis
* PCA visualization
* Hierarchical Clustering
* DBSCAN
* Cluster summary
* Supervised validation
* GridSearchCV tuning

---

# 4. Methods Used

Unsupervised learning models:

1. K-Means Clustering

   * Scaled features
   * Elbow method
   * Silhouette score
   * PCA for visualization
   * Best value: k = 4

2. Hierarchical Clustering

   * Ward linkage
   * Dendrogram inspection

3. DBSCAN

   * Density-based clustering
   * Demonstrates that dataset does not form clear density clusters

Supervised learning (for validation):

* Logistic Regression
* Random Forest Classifier

Both models used a binary target: high spenders vs everyone else.
Both achieved high accuracy, showing the spending score correlates with age and income.
This confirms that the clusters discovered earlier are meaningful.

GridSearchCV was used to demonstrate a basic hyperparameter tuning step.

---

# 5. EDA Summary

Main findings:

* Age ranges from 18 to 70
* Income distribution is slightly right-skewed
* Spending score is evenly distributed
* No missing values
* Scaling was needed due to different numeric ranges

These observations helped guide model selection and expectations.

---

# 6. Results and Findings

Best model: K-Means with k = 4.
Clusters discovered represent intuitive customer groups:

1. Young, high spending
2. Older, low spending
3. High income, low spending
4. Middle income, moderate spending

Hierarchical clustering showed a similar grouping.
DBSCAN did not produce meaningful separation.
Supervised validation proved that spending behavior is predictable and aligned with the clusters.

---

## 7. How to Run

This project requires only standard Python data-science libraries
(Numpy, Pandas, Matplotlib, Seaborn, Scikit-Learn).

### Run the notebook:
jupyter notebook Final_Unsupervised_Project.ipynb

A standard CPU machine is enough.
---

# 8. Deliverables

Deliverable 1: Jupyter Notebook
Deliverable 2: Video Presentation (MP4 format)
Deliverable 3: GitHub Repository

---

# 9. Final Thoughts

This project shows how unsupervised learning can uncover real customer patterns and how supervised learning can validate those findings.
The segmentation can help businesses with marketing strategies, customer retention, and targeted promotions.

---

