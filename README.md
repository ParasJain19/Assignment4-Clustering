# 📊 Comparative Clustering Analysis on UCI Iris Dataset

This project performs a **comparative performance study of clustering algorithms** using different **pre-processing techniques**, evaluated on multiple metrics like **Silhouette Score**, **Calinski-Harabasz Index**, and **Davies-Bouldin Score**.

---

## 📌 Objective

To analyze how different clustering algorithms (**KMeans, Hierarchical, MeanShift**) behave on varying pre-processing techniques and how they perform across different numbers of clusters (where applicable).

---

## 📁 Dataset

- **Source**: UCI Machine Learning Repository  
- **Dataset Used**: [Iris Dataset](https://archive.ics.uci.edu/ml/datasets/iris)
- **Attributes**: 4 features, 150 samples

---

## 🧪 Preprocessing Techniques Applied

| Preprocessing Code | Description                               |
|--------------------|-------------------------------------------|
| No Processing      | Raw input features                        |
| Normalization      | Min-Max scaling between [0,1]             |
| Transform          | Square root transformation                |
| PCA                | Dimensionality reduction (2 components)   |
| T+N                | Square root → Normalization               |
| T+N+PCA            | T+N → PCA (2 components)                  |

---

## 🧠 Clustering Algorithms Used

| Algorithm      | Notes                                   |
|----------------|------------------------------------------|
| **KMeans**     | Tested for k = 3, 4, 5                   |
| **Hierarchical** (Agglomerative) | Tested for k = 3, 4, 5 |
| **MeanShift**  | Auto-detects number of clusters          |

---

## 📈 Evaluation Metrics

1. **Silhouette Score** – Measures cohesion & separation
2. **Calinski-Harabasz Index** – Ratio of between-cluster to within-cluster dispersion
3. **Davies-Bouldin Score** – Measures intra/inter-cluster similarity (lower is better)

---

## 🧾 Files Included

| File Name                  | Description                                   |
|---------------------------|-----------------------------------------------|
| `clustering_full_results.csv` | Full list of clustering results for all methods |
| `clustering_summary.csv`      | Aggregated average metric scores             |
| `Clustering_Analysis.ipynb`   | Complete Colab-compatible notebook          |
| `README.md`                    | This documentation                         |

---

## 🔍 Observations

- **KMeans** performed best with `T+N` and `Normalization` in terms of **Silhouette** and **Calinski-Harabasz**.
- **MeanShift** detected a dynamic number of clusters but underperformed on Davies-Bouldin in some pre-processing modes.
- **Hierarchical** was more stable under `T+N+PCA`, but generally sensitive to input scaling.

---

## 📊 Visualizations

Three heatmaps were generated to visualize the average clustering performance:

- Average **Silhouette Score** per method & algorithm  
- Average **Calinski-Harabasz Index**  
- Average **Davies-Bouldin Score**

---

## ✅ Conclusion

Preprocessing plays a **critical role** in the performance of clustering algorithms. In general:

- **Transform + Normalize** (`T+N`) improves performance across most algorithms.
- **Dimensionality reduction via PCA** can help or hurt depending on algorithm sensitivity.
- It's important to try multiple combinations for real-world data for best results.

---


