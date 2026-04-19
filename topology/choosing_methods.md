# Choosing Your Method

## Learning Objectives

By the end of this section, you should be able to:
- Select an appropriate dimensionality reduction or analysis method for a given dataset and question
- Articulate the assumptions and trade-offs of each method
- Design an analysis pipeline that combines multiple methods
- Avoid common pitfalls in dimensionality reduction

## Outline

### Decision Framework

**Start with your question:**
1. **Exploration / visualization?** $\to$ PCA first, then UMAP if non-linear structure suspected
2. **Separate task variables?** $\to$ dPCA (labeled conditions), TCA (tensor structure)
3. **Find dynamics?** $\to$ jPCA (rotational), eigenvalue analysis (stability)
4. **Relate two populations/modalities?** $\to$ CCA
5. **Classify or decode?** $\to$ LDA
6. **Find independent sources?** $\to$ ICA
7. **Learn behaviorally aligned embeddings?** $\to$ CEBRA
8. **Understand topology?** $\to$ TDA, persistent homology

### Key Questions to Ask
- Is my data linear or non-linear?
- Do I have labels/conditions or is this unsupervised?
- Is temporal structure important?
- Do I have multiple data modalities?
- What do I want to preserve: variance, distances, cluster structure, dynamics?

### Common Pipelines
- PCA $\to$ UMAP (reduce noise before non-linear embedding)
- PCA $\to$ jPCA (find rotational dynamics in top PCs)
- PCA $\to$ K-Means (cluster in reduced space)
- CEBRA (end-to-end if behavioral labels available)

### Pitfalls
- **Applying PCA to already-low-dimensional data:** wasteful, may add noise
- **Over-interpreting UMAP clusters:** cluster size and distance are not meaningful
- **Confusing variance with importance:** PCA's top components capture variance, not necessarily the signal you care about
- **Ignoring trial-to-trial variability:** single-trial methods vs. trial-averaged
- **Not cross-validating:** always assess generalization

### Method Comparison Table

See the [Method Comparison](../appendices/method_comparison.md) appendix for a comprehensive side-by-side table.
