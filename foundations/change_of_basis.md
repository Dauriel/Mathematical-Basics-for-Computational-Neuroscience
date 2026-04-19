# Change of Basis

## Learning Objectives

By the end of this section, you should be able to:
- Explain what a basis is and why different bases are useful
- Compute the change-of-basis matrix between two bases
- Apply similarity transformations to express a matrix in a new basis
- Connect change of basis to diagonalization and dimensionality reduction

## Outline

### Basis and Coordinates
- A basis $\{v_1, \ldots, v_n\}$ for $\mathbb{R}^n$
- Coordinates of a vector $\mathbf{x}$ with respect to a basis
- The standard basis vs. other bases

### The Change-of-Basis Matrix
- If $P$ is the matrix whose columns are the new basis vectors:

$$
[\mathbf{x}]_{\text{new}} = P^{-1} \mathbf{x}
$$

- For an orthonormal basis: $P^{-1} = P^T$

### Similarity Transformations
- A linear map $A$ in the new basis: $A' = P^{-1} A P$
- Similar matrices represent the same transformation in different coordinates
- Diagonalization as a change of basis: $A = P \Lambda P^{-1}$

### Why Change Basis?
- To simplify computations (diagonalization)
- To reveal structure (principal components)
- To align with meaningful directions in the data

:::{admonition} Neuroscience Connection
:class: tip
PCA is fundamentally a change of basis: from the original neuron-by-neuron coordinates to a coordinate system aligned with the directions of maximum variance. The principal components *are* the new basis vectors.
:::

:::{admonition} Intuition
:class: note
Changing basis is like choosing a different coordinate system on a map. The territory does not change --- only how you describe it. Some coordinate systems make the landscape much easier to read.
:::
