# 🚗 Unsupervised Vehicle Clustering

## 📌 Project Overview

This project applies unsupervised machine learning to cluster vehicles based on technical and performance features.  

An automobile manufacturer has developed prototypes for a new vehicle. Before launching the model, they want to understand which existing vehicles are most similar to the prototype to identify competitors and optimize market positioning.

The objective is to use clustering methods to find the most distinctive vehicle groups, summarizing existing market patterns and providing actionable insights for product development and strategy.

---

## 📂 Dataset

- **Source:** `Cars.csv`  
- **Observations:** 156  
- **Features used for clustering:**  
  - `engine_s` – Engine Size  
  - `horsepow` – Horsepower  
  - `wheelbas` – Wheelbase  
  - `width` – Vehicle Width  
  - `length` – Vehicle Length  
  - `curb_wgt` – Curb Weight  
  - `fuel_cap` – Fuel Capacity  
  - `mpg` – Miles per Gallon  

---

## ⚙️ Methods & Workflow

- **Data Preprocessing:** Feature selection, missing value check, MinMax scaling  
- **Hierarchical Clustering:** Agglomerative clustering with Ward, Complete, and Average linkage  
- **K-Means Clustering:** Elbow method and silhouette score for optimal clusters  
- **Evaluation:** Silhouette score to assess cluster cohesion and separation  
- **Comparison:** Determined best clustering approach based on silhouette score  

---

## 🏆 Key Results & Insights

### Hierarchical Clustering

- **Average linkage achieved the highest silhouette score:** 0.515  
- Ward: 0.366 | Complete: 0.364  
- **Insight:** Clusters have varying shapes/sizes; Average linkage captures these better.

### K-Means Clustering

| Method                 | Silhouette Score |
|------------------------|-----------------|
| Hierarchical (Average) | 0.515           |
| K-Means                | 0.367           |

- Hierarchical clustering outperformed K-Means, indicating better-separated and more cohesive clusters.
- **Impact:** Identifies competitive vehicle groups more accurately, supporting strategic decisions.

---

## 🛠️ Tools & Libraries

- Python  
- scikit-learn  
- Pandas, NumPy  
- Matplotlib, Seaborn  

---

## ✅ Summary

Hierarchical clustering with Average linkage provides the most meaningful segmentation of vehicles, offering a practical framework for competitive analysis and market positioning.

---

## 🚀 How to Run

1. Clone the repository  
2. Install dependencies:  
```bash
pip install -r requirements.txt
jupyter notebook Unsupervised_Clustering_Vehicle.ipynb

