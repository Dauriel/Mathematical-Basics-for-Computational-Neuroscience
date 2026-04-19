# Temporal Structure: jPCA, dPCA, and TCA

## Learning Objectives

By the end of this section, you should be able to:
- Explain how jPCA captures rotational dynamics in neural populations
- Derive dPCA as a method that separates task variables
- Describe Tensor Component Analysis and when tensor methods outperform matrix methods
- Compare these methods in terms of their assumptions and what they reveal

## Outline

### jPCA: Rotational Dynamics
- Motivation: neural trajectories during movement look rotational
- jPCA fits a skew-symmetric dynamics matrix $M_{\text{skew}}$ to the time derivative of PCA-projected data
- Skew-symmetric $\Rightarrow$ purely imaginary eigenvalues $\Rightarrow$ rotations
- Algorithm:
  1. Apply PCA to reduce dimensionality
  2. Estimate $\dot{X} \approx M X$
  3. Constrain $M$ to be skew-symmetric: $M = M_{\text{skew}}$
  4. Eigendecomposition of $M_{\text{skew}}$ gives rotation planes

### Demixed PCA (dPCA)
- Motivation: PCA components mix together multiple task variables (e.g., stimulus identity, time, decision)
- dPCA finds components that each capture variance associated with a single task variable
- Formulation: decompose the data matrix into marginalizations, then find linear projections that reconstruct each marginalization
- Loss function combines reconstruction of each marginalization

$$
L = \sum_{\phi} \| X_\phi - F_\phi D_\phi X \|^2
$$

where $X_\phi$ is the marginalization for variable $\phi$, $D_\phi$ and $F_\phi$ are the decoder and encoder.

### Tensor Component Analysis (TCA)
- Neural data as a tensor: neurons $\times$ time $\times$ trials
- CP decomposition: $\mathcal{X} \approx \sum_{r=1}^R \mathbf{a}_r \circ \mathbf{b}_r \circ \mathbf{c}_r$
- Each component $r$ gives a neuron factor, a temporal factor, and a trial factor
- Advantage over PCA: does not require matricization (preserving the natural tensor structure)

### When to Use What?
| Method | Finds | Requires | Best for |
|--------|-------|----------|----------|
| jPCA | Rotational dynamics | Time series after PCA | Motor cortex, rhythmic dynamics |
| dPCA | Task-variable-specific components | Task labels | Multi-condition experiments |
| TCA | Low-rank tensor structure | Tensor-shaped data | Separating neuron/time/trial factors |

:::{admonition} Key Papers
:class: seealso
- **dPCA:** Kobak et al. (2016). [Demixed principal component analysis of neural population data](https://arxiv.org/abs/1410.6031). eLife.
- **TCA:** Williams et al. (2018). [Unsupervised discovery of demixed, low-dimensional neural dynamics](https://pubmed.ncbi.nlm.nih.gov/34880499/). Nature Neuroscience.
:::
