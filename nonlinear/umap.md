# UMAP

## Learning Objectives

By the end of this section, you should be able to:
- Explain the intuition behind UMAP (and how it differs from t-SNE)
- Describe the mathematical framework: fuzzy simplicial sets and cross-entropy optimization
- Understand the key hyperparameters and their effects
- Know when UMAP is appropriate and when it can be misleading

## Outline

### Why Non-Linear?
- Linear methods (PCA, etc.) can only find linear subspaces
- Real neural data may live on curved manifolds
- Non-linear methods can capture this structure --- but with trade-offs

### UMAP: Uniform Manifold Approximation and Projection
- **High-level idea:**
  1. Build a graph of nearest neighbors in high dimensions
  2. Optimize a low-dimensional layout that preserves the graph structure
- Based on Riemannian geometry and algebraic topology (fuzzy simplicial sets)

### The Algorithm
1. Construct a weighted $k$-nearest neighbor graph
2. Symmetrize the graph (fuzzy union of directed edges)
3. Initialize low-dimensional embedding (e.g., via spectral embedding)
4. Optimize positions to minimize cross-entropy between high-D and low-D edge weights

### Key Hyperparameters
| Parameter | Effect | Default |
|-----------|--------|---------|
| `n_neighbors` | Local vs. global structure. Larger = more global. | 15 |
| `min_dist` | How tightly points cluster. Smaller = tighter clusters. | 0.1 |
| `n_components` | Embedding dimensionality | 2 |
| `metric` | Distance function in high-D space | euclidean |

### UMAP vs. t-SNE
- Both are neighbor-graph methods
- UMAP: faster, better preserves global structure, has theoretical grounding
- t-SNE: tends to create more uniform-sized clusters
- Neither preserves distances reliably --- interpret with caution

### Pitfalls
- Cluster sizes and distances in UMAP plots are not meaningful
- Results depend heavily on hyperparameters
- Random seed affects the layout
- Do not over-interpret visual separation as statistical significance

:::{admonition} Neuroscience Connection
:class: tip
UMAP is widely used to visualize neural population states, revealing cluster structure and trajectories that are invisible in PCA. But beware: UMAP distorts distances and densities. Always validate findings with quantitative analysis.
:::
