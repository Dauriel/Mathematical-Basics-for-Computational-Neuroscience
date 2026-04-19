# Matrix Properties and Special Matrices

## Learning Objectives

By the end of this section, you should be able to:
- Identify and characterize symmetric, orthogonal, and rotational matrices
- Compute determinants and inverses and interpret them geometrically
- Understand matrix norms and condition numbers
- Recognize positive definite matrices and their significance

## Outline

### Transpose, Symmetry, and Skew-Symmetry
- Transpose: $A^T$, $(AB)^T = B^T A^T$
- Symmetric matrices: $A = A^T$
- Skew-symmetric matrices: $A = -A^T$

### Orthogonal Matrices
- Definition: $Q^T Q = I$, equivalently $Q^{-1} = Q^T$
- Columns form an orthonormal basis
- Preserve lengths and angles: $\|Q\mathbf{x}\| = \|\mathbf{x}\|$

### Rotation Matrices
- 2D rotation by angle $\theta$:

$$
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}
$$

- Properties: $\det(R) = 1$, $R^T = R^{-1}$
- 3D rotations and Euler angles (brief overview)

### Determinants
- Geometric interpretation: signed volume scaling factor
- $\det(AB) = \det(A)\det(B)$
- Invertibility: $A$ is invertible $\iff$ $\det(A) \neq 0$

### Inverse Matrices
- Definition and computation
- When does the inverse exist?
- Numerical stability and condition number

### Positive Definite Matrices
- Definition: $\mathbf{x}^T A \mathbf{x} > 0$ for all $\mathbf{x} \neq 0$
- All eigenvalues positive
- Connection to covariance matrices

:::{admonition} Neuroscience Connection
:class: tip
The covariance matrix of neural activity is always symmetric and positive semi-definite. Its properties directly determine the behavior of PCA and related methods.
:::
