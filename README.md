# Customer Segmentation Analysis via Unsupervised Learning

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/avinash-chauhan-oss/Customer-Segmentation-Analysis/blob/main/notebooks/customer_segmentation.ipynb)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/Library-Scikit--learn-F7931E.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

An end-to-end unsupervised machine learning pipeline that identifies distinct high-value consumer segments from retail transactional data, enabling actionable targeting strategies.

---

## Overview

Understanding customer behavior is a core challenge in data-driven business strategy. This project applies **Principal Component Analysis (PCA)** and **K-Means Clustering** to mall customer data to discover natural groupings based on income and spending patterns — without any labeled training data.

**Business goal:** Identify actionable customer personas to optimize marketing spend and maximize ROI.

---

## Methodology

### 1. Data Preprocessing
- Standardized all numeric features (Annual Income, Spending Score, Age) using `StandardScaler` to ensure uniform distance metrics across dimensions.

### 2. Dimensionality Reduction (PCA)
- Applied PCA to reduce the 3D feature space to 2D principal components.
- **77%+ of total variance** is preserved, enabling clean 2D visualization of cluster separation.

### 3. Optimal Cluster Selection
- Applied the **Elbow Method** on Within-Cluster Sum of Squares (WCSS) to determine the optimal number of clusters: **k = 5**.

### 4. K-Means Clustering
- Trained K-Means (k=5) with `k-means++` initialization for stable convergence.
- Assigned each customer to their nearest centroid.

---

## Discovered Consumer Personas

| Segment | Income | Spending | Profile |
|---------|--------|----------|---------|
| **1 — Careful Savers** | High | Low | Financially conservative; needs trust-building |
| **2 — Priority Targets** | High | High | Ideal customers; high-value loyalists |
| **3 — Careless Spenders** | Low | High | Impulsive buyers; respond to promotions |
| **4 — Sensible Shoppers** | Average | Average | Mainstream segment; needs value proposition |
| **5 — Constrained** | Low | Low | Price-sensitive; limited discretionary spend |

---

## Key Results

- **Silhouette Score ≈ 0.55** — indicates well-separated, cohesive clusters
- Clear visual separation of all 5 clusters in 2D PCA space
- Segment 2 ("Priority Targets") represents the highest-value cohort for targeted campaigns

---

## Tech Stack

`Python` · `Scikit-learn` · `NumPy` · `Pandas` · `Matplotlib` · `Seaborn`

---

## Repository Structure

```
Customer-Segmentation-Analysis/
├── notebooks/
│   └── customer_segmentation.ipynb   # Full pipeline notebook
├── data/                             # Dataset (Mall Customers CSV)
└── README.md
```

---

## Author

**Avinash Chauhan** — BS-MS Mathematics, IISER Thiruvananthapuram  
🌐 [Portfolio](https://avinash-chauhan-oss.github.io)
