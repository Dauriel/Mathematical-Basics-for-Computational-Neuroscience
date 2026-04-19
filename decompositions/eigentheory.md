# Eigenvalues and Eigenvectors

## Learning Objectives

By the end of this section, you should be able to:
- Define eigenvalues and eigenvectors and compute them for small matrices
- Interpret eigenvalues/eigenvectors geometrically
- Perform eigendecomposition and understand when it exists
- Connect the spectral theorem to symmetric matrices

## Outline

### Definition

:::{prf:definition} Eigenvalue and Eigenvector
Let $A \in \mathbb{R}^{n \times n}$. A scalar $\lambda$ is an **eigenvalue** of $A$ if there exists a nonzero vector $\mathbf{v} \in \mathbb{R}^n$ such that

$$
A\mathbf{v} = \lambda \mathbf{v}
$$

The vector $\mathbf{v}$ is called an **eigenvector** corresponding to $\lambda$.
:::

### Computing Eigenvalues
- Characteristic polynomial: $\det(A - \lambda I) = 0$
- Algebraic vs. geometric multiplicity
- Examples: 2x2 and 3x3 matrices

### Geometric Interpretation
- Eigenvectors are directions that the matrix only stretches (or flips), never rotates
- Eigenvalues are the stretch factors
- Complex eigenvalues imply rotation

### Eigendecomposition
- $A = P \Lambda P^{-1}$ where $\Lambda = \diag(\lambda_1, \ldots, \lambda_n)$
- Exists when $A$ has $n$ linearly independent eigenvectors
- For symmetric matrices: $A = Q \Lambda Q^T$ (orthogonal diagonalization)

### The Spectral Theorem

:::{prf:theorem} Spectral Theorem (Real Symmetric Case)
If $A \in \mathbb{R}^{n \times n}$ is symmetric ($A = A^T$), then:
1. All eigenvalues of $A$ are real
2. Eigenvectors corresponding to distinct eigenvalues are orthogonal
3. $A$ can be orthogonally diagonalized: $A = Q \Lambda Q^T$
:::

### Matrix Powers and the Eigendecomposition
- $A^k = P \Lambda^k P^{-1}$
- Matrix exponential: $e^{At}$ (preview for dynamical systems)

:::{admonition} Neuroscience Connection
:class: tip
The eigenvalues of the covariance matrix of neural activity tell you how much variance lies along each principal direction. The eigenvectors define those directions. This is the mathematical core of PCA.
:::
