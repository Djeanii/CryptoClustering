# Cryptocurrency Clustering Analysis

## Overview
This project uses **unsupervised learning** techniques to analyze cryptocurrency market data and identify potential clusters of cryptocurrencies based on their 24-hour and 7-day price changes. The analysis is conducted using **K-Means clustering** and **Principal Component Analysis (PCA)** to evaluate the impact of dimensionality reduction.

---

## Objectives
1. Analyze cryptocurrency data using **K-Means clustering**.
2. Use the **Elbow Method** to determine the optimal number of clusters.
3. Apply **PCA** to reduce features and compare clustering results.
4. Visualize and contrast clusters from the original data and PCA-reduced data.

---

## Project Files
- **`crypto_market_data.csv`**: Dataset containing cryptocurrency price changes and other metrics.
- **`Crypto_Clustering.ipynb`**: Jupyter Notebook with the analysis and clustering workflow.
- **`README.md`**: Documentation for the project.

---

## Technologies Used
- **Python**: Programming language for analysis and visualization.
- **Libraries**:
  - `pandas`: For data manipulation.
  - `scikit-learn`: For K-Means clustering and PCA.
  - `hvPlot`: For interactive visualizations.
  - `matplotlib`: For plotting Elbow Curves.

---

## Methodology

### 1. Data Preprocessing
- **Normalization**: Used `StandardScaler` from `scikit-learn` to normalize the data for fair clustering.
- **Feature Selection**: Focused on `price_change_percentage_24h` and `price_change_percentage_7d` for clustering.

### 2. Clustering with K-Means
- Determined the optimal number of clusters using the **Elbow Method**.
- Visualized clusters in the original scaled feature space.

### 3. Dimensionality Reduction with PCA
- Applied PCA to reduce the data to two principal components (`PC1` and `PC2`).
- Recomputed clusters on the PCA-reduced data.

### 4. Visualizations
- Created scatter plots to visualize clusters from both the original and PCA data.
- Compared Elbow Curves for original and PCA data to evaluate the impact of dimensionality reduction.

---

## Key Results

### Elbow Method
- **Optimal Number of Clusters (k)**: The Elbow Curve indicates the best \(k\) value is **4** for both original and PCA data.

### Cluster Analysis
- Clusters are similar in both original and PCA-reduced data, with PCA simplifying the feature space.

---

## Visualizations
### 1. Clustering Results
- Scatter plots showing cryptocurrency clusters based on both **original scaled data** and **PCA-reduced data**.

![Clusters Combined Data](Screenshot.png)

### 2. Elbow Curve
- A comparison of Elbow Curves for the **original scaled data** and **PCA-reduced data**.

![Elbow Curve Comparison](ElbowCurve.png)

---

## Conclusions
- **Dimensionality Reduction with PCA**:
  - Simplifies clustering and visualization while retaining most of the original data's variance.
  - Reduces computational complexity without significantly affecting clustering quality.
- **K-Means Clustering**:
  - Effectively groups cryptocurrencies based on similar price change behaviors.
  - Identifies meaningful clusters in both the original and reduced feature spaces.

---

## How to Run the Analysis
1. Clone the repository and navigate to the project folder.
2. Install the required Python libraries:
   ```bash
   pip install pandas scikit-learn hvplot matplotlib
