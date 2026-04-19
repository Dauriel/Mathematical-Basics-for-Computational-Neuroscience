# Method Comparison

A side-by-side comparison of the dimensionality reduction and analysis methods covered in this seminar.

## Linear Methods

| Method | Input | Objective | Supervised? | Preserves | Key Assumption | Max Components |
|--------|-------|-----------|-------------|-----------|----------------|----------------|
| **PCA** | Data matrix | Max variance | No | Variance | Linear subspace | $\min(n, p)$ |
| **LDA** | Data + labels | Max class separation | Yes | Discriminability | Gaussian classes, shared covariance | $C - 1$ |
| **cPCA** | Target + background | Contrastive variance | Semi | Target-specific variance | Linear, contrast with background | $\min(n, p)$ |
| **jPCA** | Time series (post-PCA) | Rotational dynamics | No | Rotational structure | Skew-symmetric dynamics | Pairs (2D planes) |
| **dPCA** | Data + condition labels | Demixed variance | Yes | Per-variable variance | Linear, additive contributions | $\min(n, p)$ per variable |
| **TCA** | Tensor (neuron x time x trial) | Low-rank tensor | No | Tensor structure | CP decomposition exists | $R$ (rank) |
| **CCA** | Two data matrices | Max correlation | No | Cross-set correlation | Linear relationship | $\min(p, q)$ |
| **ICA** | Data matrix | Statistical independence | No | Independence | Non-Gaussian sources, linear mixing | $p$ |
| **FA** | Data matrix | Latent factors + noise | No | Shared variance | Gaussian factors, diagonal noise | Chosen by user |
| **MDS** | Distance matrix | Preserve distances | No | Pairwise distances | Meaningful distances | Chosen by user |

## Non-Linear Methods

| Method | Input | Objective | Supervised? | Preserves | Key Assumption | Key Hyperparameters |
|--------|-------|-----------|-------------|-----------|----------------|---------------------|
| **UMAP** | Data matrix | Manifold structure | No | Local neighborhoods | Manifold hypothesis | `n_neighbors`, `min_dist` |
| **t-SNE** | Data matrix | Local structure | No | Local neighborhoods | Local similarity meaningful | Perplexity |
| **CEBRA** | Neural data + (optional) behavior | Behaviorally aligned embedding | Optional | Task-relevant structure | Contrastive learning | Embedding dim, time window |

## Clustering Methods

| Method | Input | Finds | Must specify $k$? | Handles noise? | Cluster shape |
|--------|-------|-------|-------------------|----------------|---------------|
| **K-Means** | Data matrix | $k$ spherical clusters | Yes | No | Spherical |
| **DBSCAN** | Data matrix | Density-based clusters | No | Yes | Arbitrary |

## Decision Guide

```
What is your question?
│
├── "What are the main patterns of activity?"
│   └── PCA
│
├── "Can I separate conditions/classes?"
│   └── LDA (few classes) or dPCA (multiple task variables)
│
├── "What is unique to this condition vs. baseline?"
│   └── cPCA
│
├── "Are there rotational dynamics?"
│   └── jPCA
│
├── "How do two brain areas relate?"
│   └── CCA
│
├── "Are there independent sources?"
│   └── ICA
│
├── "What does the data look like in 2D?"
│   ├── Quick look → PCA (first 2 PCs)
│   └── Non-linear structure suspected → UMAP
│
├── "I want behaviorally aligned embeddings"
│   └── CEBRA
│
├── "Are there discrete states?"
│   ├── Known number of states → K-Means
│   └── Unknown, density-based → DBSCAN
│
└── "What is the topology of the neural manifold?"
    └── TDA / Persistent homology
```
