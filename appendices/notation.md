# Notation Reference

This page collects the mathematical notation used throughout the course.

## Scalars, Vectors, and Matrices

| Symbol | Meaning |
|--------|---------|
| $a, b, \lambda$ | Scalars (lowercase, italic) |
| $\mathbf{x}, \mathbf{v}, \mathbf{w}$ | Vectors (bold lowercase) |
| $A, B, C$ | Matrices (uppercase, italic) |
| $\mathcal{X}, \mathcal{T}$ | Tensors (calligraphic uppercase) |
| $I$ or $I_n$ | Identity matrix ($n \times n$) |
| $\mathbf{0}$ | Zero vector or zero matrix |
| $\mathbf{e}_i$ | $i$-th standard basis vector |

## Matrix Operations

| Symbol | Meaning |
|--------|---------|
| $A^T$ | Transpose of $A$ |
| $A^{-1}$ | Inverse of $A$ |
| $A^*$ | Conjugate transpose (Hermitian transpose) |
| $A^{\dagger}$ | Moore-Penrose pseudoinverse |
| $\det(A)$ | Determinant of $A$ |
| $\tr(A)$ | Trace of $A$: $\sum_i A_{ii}$ |
| $\rank(A)$ | Rank of $A$ |
| $\|A\|_F$ | Frobenius norm: $\sqrt{\sum_{ij} A_{ij}^2}$ |
| $\|A\|_2$ | Spectral norm: largest singular value |

## Vector Operations

| Symbol | Meaning |
|--------|---------|
| $\mathbf{x}^T \mathbf{y}$ or $\langle \mathbf{x}, \mathbf{y} \rangle$ | Inner product (dot product) |
| $\mathbf{x} \otimes \mathbf{y}$ or $\mathbf{x} \mathbf{y}^T$ | Outer product |
| $\|\mathbf{x}\|$ or $\|\mathbf{x}\|_2$ | Euclidean norm: $\sqrt{\sum_i x_i^2}$ |

## Subspaces

| Symbol | Meaning |
|--------|---------|
| $\mathcal{C}(A)$ | Column space of $A$ |
| $\mathcal{N}(A)$ | Null space of $A$ |
| $\text{span}(\mathbf{v}_1, \ldots, \mathbf{v}_k)$ | Span of vectors |
| $\dim(V)$ | Dimension of subspace $V$ |

## Decompositions

| Symbol | Meaning |
|--------|---------|
| $\lambda_i$ | $i$-th eigenvalue |
| $\mathbf{v}_i$ | $i$-th eigenvector |
| $\sigma_i$ | $i$-th singular value |
| $\mathbf{u}_i$ | $i$-th left singular vector |
| $\Lambda$ | Diagonal matrix of eigenvalues |
| $\Sigma$ | Diagonal matrix of singular values |
| $A = P\Lambda P^{-1}$ | Eigendecomposition |
| $A = U\Sigma V^T$ | Singular value decomposition |

## Statistics and Data

| Symbol | Meaning |
|--------|---------|
| $X \in \mathbb{R}^{n \times p}$ | Data matrix: $n$ observations, $p$ features |
| $\bar{\mathbf{x}}$ | Sample mean |
| $C$ or $\Sigma_X$ | Covariance matrix |
| $\Var(\cdot)$ | Variance |
| $\Cov(\cdot, \cdot)$ | Covariance |

## Sets and Spaces

| Symbol | Meaning |
|--------|---------|
| $\mathbb{R}$ | Real numbers |
| $\mathbb{R}^n$ | $n$-dimensional real vector space |
| $\mathbb{R}^{m \times n}$ | Space of $m \times n$ real matrices |
| $\mathbb{C}$ | Complex numbers |
| $S^n$ | $n$-sphere |
| $T^n$ | $n$-torus |
