# CEBRA

## Learning Objectives

By the end of this section, you should be able to:
- Explain CEBRA's contrastive learning approach to neural embeddings
- Distinguish supervised, self-supervised, and hybrid CEBRA modes
- Understand what makes CEBRA embeddings "consistent" across subjects and sessions
- Evaluate when CEBRA is preferable to PCA or UMAP

## Outline

### Motivation
- We want embeddings that reflect behaviorally relevant structure
- CEBRA: **C**onsistent **E**m**B**eddings of high-dimensional **R**ecordings using **A**uxiliary variables
- Key idea: use contrastive learning to learn embeddings where nearby time points (or similar behavioral states) are close together

### Contrastive Learning Framework
- Positive pairs: samples that should be close (e.g., temporally adjacent, same behavior)
- Negative pairs: samples that should be far (e.g., random time points)
- Loss function encourages positive pairs to be closer than negative pairs in the embedding

### Modes of Operation
| Mode | Positive pairs defined by | Use case |
|------|--------------------------|----------|
| Self-supervised | Temporal adjacency | No behavioral labels |
| Supervised | Behavioral labels | Known task variables |
| Hybrid | Both | Best of both worlds |

### Consistency Across Subjects
- CEBRA can learn embeddings that are aligned across different animals or sessions
- Enables cross-subject decoding and comparison

### Architecture
- Neural network encoder maps high-D neural data to low-D embedding
- Trained with InfoNCE loss
- Temperature parameter controls the sharpness of the similarity distribution

### Practical Considerations
- Requires choosing: embedding dimension, time window, positive pair definition
- Can decode behavior from the embedding to evaluate quality
- Comparison with UMAP: CEBRA embeddings are more quantitatively meaningful

:::{admonition} Key Paper
:class: seealso
Schneider, Lee & Bhagavatula (2023). [Learnable latent embeddings for joint behavioural and neural analysis](https://www.nature.com/articles/s41586-023-06031-6). Nature.
:::
