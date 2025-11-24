# Customer Segmentation with Unsupervised Learning (Mall Customers Dataset)

This project is my final assignment for the **Unsupervised Algorithms in Machine Learning** course.  
The goal is to use unsupervised methods to discover meaningful customer segments in the classic Mall Customers dataset and then compare those results with simple supervised models.

---

## 1. Dataset

- **Name:** Mall Customers dataset  
- **Size:** 200 customers, 5 columns  
- **Main features:**  
  - `Age`  
  - `Annual Income (k$)`  
  - `Spending Score (1-100)`  
- **Source:** Public teaching dataset (often used on Kaggle and in ML tutorials).

The target variable is not provided in the original data. I treat this as a pure unsupervised segmentation problem and later create a simple binary target for supervised comparison.

---

## 2. Project Structure

- `mall_customers_clustering.ipynb` – main Jupyter notebook with:
  - exploratory data analysis (EDA)
  - K-Means clustering with elbow and silhouette analysis
  - Hierarchical clustering and dendrogram
  - DBSCAN clustering (density-based)
  - cluster interpretation and profiles
  - comparison with supervised models (Logistic Regression, Random Forest)
  - small hyperparameter tuning example with GridSearchCV
- `Mall_Customers.csv` – dataset file (if allowed to include in the repo)
- `README.md` – this file

---

## 3. Methods Used

### Unsupervised

- **K-Means clustering**
  - Features: Age, Annual Income, Spending Score  
  - StandardScaler for feature scaling  
  - Elbow method and Silhouette Score to select the number of clusters  
  - Final model: `k = 4`
- **Hierarchical clustering**
  - Ward linkage with Euclidean distance  
  - Dendrogram to visualize how clusters merge
- **DBSCAN**
  - Density-based clustering to check whether the data forms natural dense regions

### Supervised (for comparison)

- **Logistic Regression**  
- **Random Forest Classifier**  
- Train–test split on the scaled features  
- Simple binary target: high vs low spenders based on Spending Score  
- Small hyperparameter tuning with `GridSearchCV` on the Random Forest

---

## 4. Main Findings

- The EDA suggests that the data naturally separates along income and spending behavior.
- K-Means with **k = 4** produces four intuitive customer groups, such as:
  - younger high spenders  
  - older low spenders  
  - wealthier but low-spending customers  
  - more balanced, average customers
- Hierarchical clustering roughly supports this structure, while DBSCAN struggles because the data is not strongly density-based.
- Supervised models confirm the unsupervised structure: the same high-spending customers identified by K-Means are also separated well by Logistic Regression and Random Forest.
- A small amount of hyperparameter tuning slightly improves the Random Forest performance and demonstrates how tuning can be used in practice.

---
