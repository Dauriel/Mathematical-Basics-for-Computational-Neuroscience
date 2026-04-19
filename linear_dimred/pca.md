# Principal Component Analysis (PCA)

## Learning Objectives

By the end of this section, you should be able to:
- Derive PCA from both the variance-maximization and minimum-reconstruction-error perspectives
- Connect PCA to eigendecomposition of the covariance matrix and to the SVD
- Interpret scree plots and explained variance
- Apply PCA to neural population data and interpret the results

## Outline

### Motivation
- High-dimensional data, low-dimensional structure
- The curse of dimensionality
- Why reduce dimensions? Visualization, denoising, compression, discovery

### PCA: Two Derivations

**Variance maximization:**

$$
\mathbf{w}_1 = \argmax_{\|\mathbf{w}\|=1} \Var(\mathbf{w}^T X) = \argmax_{\|\mathbf{w}\|=1} \mathbf{w}^T C \mathbf{w}
$$

where $C = \frac{1}{n-1} X^T X$ is the covariance matrix. Solution: $\mathbf{w}_1$ is the eigenvector of $C$ with the largest eigenvalue.

**Minimum reconstruction error:**

$$
\min_{W} \| X - X W W^T \|_F^2
$$

Same solution via the Eckart-Young theorem (SVD).

### The PCA Algorithm
1. Center the data: $X \leftarrow X - \bar{X}$
2. Compute covariance matrix $C$ or perform SVD of $X$
3. Select top $k$ components
4. Project: $Z = X W_k$

### Diagnostics
- Scree plot: eigenvalues vs. component number
- Explained variance ratio: $\frac{\lambda_i}{\sum_j \lambda_j}$
- Cumulative explained variance
- How to choose $k$?

### Limitations of PCA
- Linear: can only find linear subspaces
- Unsupervised: ignores labels or conditions
- Variance $\neq$ importance: the highest-variance direction may not be the most scientifically meaningful

:::{admonition} Neuroscience Connection
:class: tip
PCA is the most widely used dimensionality reduction method in systems neuroscience. It reveals the dominant patterns of covariation across neural populations. But its limitations motivate all the methods that follow in this module: supervised methods (LDA), contrastive methods (cPCA), and temporal methods (jPCA, dPCA).
:::
