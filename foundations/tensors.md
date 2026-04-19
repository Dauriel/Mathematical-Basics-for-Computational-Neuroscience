# Tensors

## Learning Objectives

By the end of this section, you should be able to:
- Understand tensors as generalizations of matrices to higher dimensions
- Read and write tensor notation (index notation)
- Describe common tensor operations (outer product, contraction, reshaping)
- Motivate why neural data naturally lives in tensor form

## Outline

### From Scalars to Tensors
- Scalar (order 0), vector (order 1), matrix (order 2), tensor (order $\geq 3$)
- A tensor as a multi-dimensional array $\mathcal{X} \in \mathbb{R}^{I_1 \times I_2 \times \cdots \times I_N}$

### Tensor Operations
- Outer product
- Tensor contraction and trace
- Matricization (unfolding): converting a tensor into a matrix along a mode
- Kronecker and Khatri-Rao products

### Tensor Decompositions (Preview)
- CP decomposition (CANDECOMP/PARAFAC)
- Tucker decomposition
- Connection to matrix SVD

:::{admonition} Neuroscience Connection
:class: tip
Neural data is naturally tensorial: neurons $\times$ time $\times$ trials $\times$ conditions. Tensor Component Analysis (TCA) exploits this structure rather than flattening data into a matrix. See the [TCA section](../linear_dimred/temporal.md) for the full treatment.
:::

:::{admonition} Intuition
:class: note
Think of a matrix as a spreadsheet (2D). A tensor is a stack of spreadsheets (3D), or a stack of stacks (4D), and so on. Each "mode" of the tensor represents a different axis of variation in your data.
:::
