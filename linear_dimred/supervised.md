# Supervised and Contrastive Methods: LDA and cPCA

## Learning Objectives

By the end of this section, you should be able to:
- Explain how LDA differs from PCA in its objective
- Derive the LDA optimization problem (maximize between-class variance / within-class variance)
- Describe contrastive PCA and when it is useful
- Compare supervised vs. unsupervised dimensionality reduction

## Outline

### Linear Discriminant Analysis (LDA)

**Objective:** Find projections that maximize class separation.

$$
\mathbf{w}^* = \argmax_{\mathbf{w}} \frac{\mathbf{w}^T S_B \mathbf{w}}{\mathbf{w}^T S_W \mathbf{w}}
$$

where $S_B$ is the between-class scatter matrix and $S_W$ is the within-class scatter matrix.

- Solution: generalized eigenvalue problem $S_B \mathbf{w} = \lambda S_W \mathbf{w}$
- At most $C-1$ discriminant directions (for $C$ classes)
- Connection to Fisher's discriminant

### PCA vs. LDA
- PCA: directions of maximum variance (unsupervised)
- LDA: directions of maximum discriminability (supervised)
- When they agree and when they disagree

### Contrastive PCA (cPCA)
- Goal: find structure present in a target dataset but absent in a background dataset
- Objective: maximize $\mathbf{w}^T (C_{\text{target}} - \alpha C_{\text{background}}) \mathbf{w}$
- The contrast parameter $\alpha$ controls the trade-off
- Choosing $\alpha$ in practice

:::{admonition} Neuroscience Connection
:class: tip
Shenoy et al. (Nature 2018) used LDA to decode movement intentions from neural population activity, finding that population-level patterns carry more information than individual neurons. cPCA can reveal condition-specific neural patterns by contrasting active vs. baseline conditions.
:::
