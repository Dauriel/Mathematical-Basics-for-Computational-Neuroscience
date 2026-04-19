# What Is a Matrix?

## Learning Objectives

By the end of this section, you should be able to:
- Define a matrix as a linear transformation between vector spaces
- Explain column space, row space, null space, and rank
- Interpret matrix-vector multiplication geometrically
- Distinguish between different ways to think about a matrix (data table, transformation, system of equations)

## Outline

### Vectors and Vector Spaces
- Vectors as elements of $\mathbb{R}^n$
- Vector spaces: closure, span, linear independence
- Basis and dimension

### What Is a Matrix?
- A matrix as a rectangular array of numbers $A \in \mathbb{R}^{m \times n}$
- As a linear map: $A: \mathbb{R}^n \to \mathbb{R}^m$
- As a collection of column vectors
- As a system of linear equations $A\mathbf{x} = \mathbf{b}$

### The Four Fundamental Subspaces
- Column space $\mathcal{C}(A)$
- Row space $\mathcal{C}(A^T)$
- Null space $\mathcal{N}(A)$
- Left null space $\mathcal{N}(A^T)$
- Rank-nullity theorem

### Matrix-Vector Multiplication as Transformation
- Geometric interpretation: what happens to the unit square?
- Composition of transformations = matrix multiplication

:::{admonition} Neuroscience Connection
:class: tip
In neural data analysis, a matrix often represents neural population activity: rows are neurons (or trials), columns are time points (or conditions). The column space captures the accessible patterns of population activity.
:::

## Interactive Demo

See the [Matrix Transformations Demo](demos/matrix_transformations.ipynb) for a visual, interactive exploration of how matrices transform space.
