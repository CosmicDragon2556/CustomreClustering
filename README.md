
# Customer Segmentation Using Clustering Techniques

## Overview

This project applies various clustering techniques to segment customers based on their purchasing behavior using the Online Retail Dataset. The dataset undergoes preprocessing, feature engineering, and clustering to analyze customer purchasing patterns.

## Dataset


- Source: Online Retail dataset [Github](https://github.com/CosmicDragon2556/CustomrsClustering/blob/main/Online%20Retail.xlsx)
- [Website Link](https://archive.ics.uci.edu/ml/datasets/Online+Retail)

## Preprocessing Steps:
- Removed duplicates
- Handled missing values (Dropped Description column due to 0.27% missing values)
- Removed negative values in Quantity and UnitPrice
- Created new features: TotalAmount, DayOfWeek, Month, InterPurchaseInterval, and ProductDiversity

## Exploratory Data Analysis(EDA):
- __Histograms__: Displaying distributions of Recency, Frequency, and Monetary values.
- __Correlation Heatmap__: Understanding relationships between RFM variables.
- __Scatter Plot__: Visualizing Recency vs. Monetary values, colored by Frequency.

## Clustering Techniques

1. __K-Means Clustering__:
- Standardized the data using StandardScaler
- Applied PCA for visualization
- Chose 4 clusters

2. __Gaussian Mixture Models(GMM)__:

- Applied Gaussian Mixture clustering with 4 components
- Visualized clusters using PCA

3. __Hierarchical Clustering__:
- Used Ward’s method for linkage
- Plotted a dendrogram for visualization

4. __t-SNE Visualization__:
- Applied t-SNE for dimensionality reduction
- Visualized clusters in a 2D space

5. __DBSCAN Clustering__:
- Applied DBSCAN for density-based clustering
- Identified noise points

## Evaluation Metrics
1. Inertia (K-Means)
Measures within-cluster variance (lower is better)

2. Number of Clusters and Outliers (DBSCAN)
Counts identified clusters and noise points

3. Silhouette Score

Measures cluster separation (-1 to 1, higher is better)

4. Davies-Bouldin Index

Measures cluster compactness and separation (lower is better)

5. Calinski-Harabasz Index

Measures between-cluster dispersion (higher is better)



## Summary_Of_metrics

![Summary Of Metrices](https://github.com/CosmicDragon2556/CustomreClustering/blob/main/Summary_of_metrics.png)



## Results & Insights

- K-Means and GMM provided clear segmentations

- DBSCAN detected noise points effectively

- Hierarchical clustering helped understand relationships

- Silhouette and Davies-Bouldin scores helped in model selection


## Installation & Usage
1. Install Dependencies:

```python
pip install numpy pandas matplotlib seaborn scikit-learn scipy
```

2. Load the dataset and preprocess it.

3. Run the clustering models and visualize results.

4. Evaluate clustering performance using metrics.

## Conclusion:

Customer segmentation using clustering helps businesses better understand customer behavior, optimize marketing strategies, and improve customer retention. Future work can include advanced deep learning-based clustering techniques.
