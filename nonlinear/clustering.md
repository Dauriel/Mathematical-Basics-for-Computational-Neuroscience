# Clustering: K-Means and DBSCAN

## Learning Objectives

By the end of this section, you should be able to:
- Explain and implement the K-Means algorithm
- Understand DBSCAN and density-based clustering
- Choose between clustering methods based on data properties
- Evaluate clustering quality

## Outline

### What Is Clustering?
- Unsupervised grouping of data points by similarity
- No labels --- the algorithm discovers structure
- Applications: identifying neural states, cell types, behavioral categories

### K-Means
- **Algorithm:**
  1. Initialize $k$ centroids (randomly or via k-means++)
  2. Assign each point to nearest centroid
  3. Recompute centroids as cluster means
  4. Repeat until convergence
- **Objective:** minimize within-cluster sum of squares

$$
\min_{C_1, \ldots, C_k} \sum_{j=1}^k \sum_{\mathbf{x} \in C_j} \|\mathbf{x} - \boldsymbol{\mu}_j\|^2
$$

- **Choosing $k$:** elbow method, silhouette score, gap statistic
- **Limitations:** assumes spherical clusters of similar size, sensitive to initialization

### DBSCAN (Density-Based Spatial Clustering)
- **Key idea:** clusters are dense regions separated by sparse regions
- **Parameters:**
  - $\varepsilon$: neighborhood radius
  - `min_samples`: minimum points to form a dense region
- **Algorithm:**
  1. A point is a *core point* if it has $\geq$ `min_samples` neighbors within $\varepsilon$
  2. Core points that are neighbors form a cluster
  3. Non-core points near a cluster are *border points*
  4. Remaining points are *noise*
- **Advantages:** finds clusters of arbitrary shape, identifies outliers, no need to specify $k$
- **Limitations:** sensitive to $\varepsilon$ and `min_samples`, struggles with varying-density clusters

### Comparison

| Property | K-Means | DBSCAN |
|----------|---------|--------|
| Cluster shape | Spherical | Arbitrary |
| Number of clusters | Must specify $k$ | Automatic |
| Handles noise | No | Yes (labels outliers) |
| Scalability | Fast ($O(nk)$) | $O(n \log n)$ with spatial index |

:::{admonition} Neuroscience Connection
:class: tip
Clustering is used to identify discrete neural states (e.g., UP/DOWN states, attractor states) from continuous recordings. Applying K-Means or DBSCAN to dimensionality-reduced neural data (e.g., after PCA or UMAP) can reveal state transitions.
:::
