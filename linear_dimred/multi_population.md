# Multi-Population Methods: CCA, ICA, Factor Analysis, MDS

## Learning Objectives

By the end of this section, you should be able to:
- Explain and derive Canonical Correlation Analysis (CCA)
- Distinguish ICA from PCA in terms of objective and assumptions
- Describe Factor Analysis and its generative model
- Apply Multidimensional Scaling (MDS) to distance data

## Outline

### Canonical Correlation Analysis (CCA)
- Goal: find linear combinations of two sets of variables that are maximally correlated
- Two datasets $X \in \mathbb{R}^{n \times p}$ and $Y \in \mathbb{R}^{n \times q}$
- Find $\mathbf{a}$, $\mathbf{b}$ to maximize:

$$
\rho = \frac{\mathbf{a}^T C_{XY} \mathbf{b}}{\sqrt{\mathbf{a}^T C_{XX} \mathbf{a}} \sqrt{\mathbf{b}^T C_{YY} \mathbf{b}}}
$$

- Solution via generalized eigenvalue problem
- Variants: regularized CCA, deep CCA

### Independent Component Analysis (ICA)
- PCA finds uncorrelated components; ICA finds statistically independent components
- Assumption: observed data is a linear mixture of independent sources: $X = AS$
- Non-Gaussianity as the key: the Central Limit Theorem in reverse
- FastICA algorithm (brief overview)
- Applications: blind source separation, artifact removal in EEG

### Factor Analysis
- Generative model: $\mathbf{x} = W\mathbf{z} + \boldsymbol{\mu} + \boldsymbol{\epsilon}$
  - $\mathbf{z}$: latent factors (low-dimensional)
  - $\boldsymbol{\epsilon}$: noise (diagonal covariance --- each variable has its own noise)
- Difference from PCA: Factor Analysis models observation noise explicitly
- Estimation via EM algorithm

### Multidimensional Scaling (MDS)
- Input: a distance or dissimilarity matrix $D$
- Output: coordinates in low dimensions that preserve pairwise distances
- Classical MDS: connected to PCA via double centering
- Stress function and non-metric MDS

### Comparison

| Method | Input | Objective | Key Assumption |
|--------|-------|-----------|----------------|
| CCA | Two datasets | Max correlation between sets | Linear relationship |
| ICA | One dataset | Statistical independence | Non-Gaussian sources |
| FA | One dataset | Latent variable model | Gaussian factors + noise |
| MDS | Distance matrix | Preserve distances | Meaningful distances |

:::{admonition} Neuroscience Connection
:class: tip
CCA is increasingly used to relate neural activity across brain areas or between neural activity and behavior. Semedo et al. (Neuron, 2019) used CCA to study how visual cortex areas communicate through shared low-dimensional subspaces.
:::
