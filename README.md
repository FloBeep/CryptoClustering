# CryptoClustering

This is a cryptocurrency clustering project with the following steps:

1. **Initial Analysis**
   * Summary statistics and initial visual analysis of the data.
2. **Data Preparation**
   * Normalization of the data and creation of a new scaled DataFrame using `StandardScaler` from `scikit-learn`, setting `coin_id` as the index.
3. **Finding Optimal k for Clustering**
   * Application of the elbow method on the scaled data to determine the best k value. This involved calculating inertia values for k values from 1 to 11 and plotting them to visually identify the optimal k.
4. **K-means Clustering**
   * Initialization and fitting of a K-means model with the optimal k on the scaled data, predicting clusters and adding labels.
   * Creation of a scatter plot using `hvPlot` with `price_change_percentage_24h` and `price_change_percentage_7d` as axes, and included `coin_id` in the hover options for data identification.
5. **Principal Component Analysis (PCA) for Dimensionality Reduction**
   * Utization of PCA on the scaled data, reducing it to three principal components and analyzing the explained variance to understand information retention.
6. **Optimal k for PCA Data**
   * Repeat of the elbow method on the PCA-reduced data to find the best k, comparing results with the original data.
7. **K-means Clustering with PCA Data**
   * Clusterization of PCA-transformed data using the optimal k value. Prediction of clusters and creation of a scatter plot using `hvPlot` with `PC1` and `PC2` as axes, including `coin_id` for identification.
8. **Analysis**
   * Clustering outcomes were compared between the original and reduced datasets, assessing the impact of dimensionality reduction on cluster quality

The following questions have been answered:

**Question:** What is the best value for `k` when using the PCA data?

**Answer:** When using PCA data, the best value of `k` is 4.

**Question:** Does it differ from the best k value found using the original data?

**Answer:** The best value of `k` using the PCA data is the same value found using the original data.

**Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?`<br>`

**Answer:** The impact of using fewer features to cluster the data using K-Means changed the inertia and resulted in more precise clusters.
