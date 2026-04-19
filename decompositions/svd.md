# Singular Value Decomposition (SVD)

## Learning Objectives

By the end of this section, you should be able to:
- State and derive the SVD
- Interpret the SVD geometrically (rotation-stretch-rotation)
- Use the SVD for low-rank approximation (Eckart-Young theorem)
- Connect SVD to eigendecomposition and PCA

## Outline

### The SVD

:::{prf:theorem} Singular Value Decomposition
Every matrix $A \in \mathbb{R}^{m \times n}$ can be factored as

$$
A = U \Sigma V^T
$$

where:
- $U \in \mathbb{R}^{m \times m}$ is orthogonal (left singular vectors)
- $\Sigma \in \mathbb{R}^{m \times n}$ is diagonal with $\sigma_1 \geq \sigma_2 \geq \cdots \geq 0$ (singular values)
- $V \in \mathbb{R}^{n \times n}$ is orthogonal (right singular vectors)
:::

### Geometric Interpretation
- Any linear transformation = rotation ($V^T$) then stretch ($\Sigma$) then rotation ($U$)
- The singular values are the semi-axes of the image of the unit sphere

### Derivation
- Connection to eigendecomposition: $A^T A = V \Sigma^2 V^T$, $A A^T = U \Sigma^2 U^T$
- Singular values = square roots of eigenvalues of $A^T A$

### Low-Rank Approximation

:::{prf:theorem} Eckart-Young Theorem
The best rank-$k$ approximation to $A$ (in Frobenius or spectral norm) is

$$
A_k = \sum_{i=1}^k \sigma_i \mathbf{u}_i \mathbf{v}_i^T
$$

obtained by keeping only the $k$ largest singular values.
:::

### Compact and Truncated SVD
- Full vs. economy vs. truncated SVD
- Computational considerations for large matrices

### SVD and PCA
- PCA on centered data $X$: the right singular vectors of $X$ are the principal components
- Singular values of $X$ relate to eigenvalues of the covariance matrix: $\lambda_i = \sigma_i^2 / (n-1)$

:::{admonition} Neuroscience Connection
:class: tip
The SVD is the computational backbone of PCA. When you run PCA on neural population data, you are computing the SVD of the (centered) data matrix. The singular values tell you how much variance each component captures.
:::
