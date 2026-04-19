# Resources: Linear Dimensionality Reduction

## Key Papers

### PCA in Neuroscience
- Cunningham & Yu (2014). [Dimensionality reduction for large-scale neural recordings](https://www.nature.com/articles/nn.3776). Nature Neuroscience. --- Landmark review of dimensionality reduction in neuroscience.
- Fusi et al. (2016). [Why neurons mix: high dimensionality for higher cognition](https://www.sciencedirect.com/science/article/abs/pii/S0959438816000118). Current Opinion in Neurobiology. --- Why neural representations are high-dimensional and what that means.

### dPCA
- Kobak et al. (2016). [Demixed principal component analysis of neural population data](https://arxiv.org/abs/1410.6031). eLife. --- Introduces dPCA for separating task-variable contributions.

### TCA
- Williams et al. (2018). [Unsupervised discovery of demixed, low-dimensional neural dynamics across multiple timescales](https://pubmed.ncbi.nlm.nih.gov/34880499/). Nature Neuroscience. --- Tensor Component Analysis applied to neural data.

### LDA
- Pandarinath et al. (2018). [Inferring single-trial neural population dynamics using sequential auto-encoders](https://www.nature.com/articles/s41586-018-0459-6). Nature. --- Uses population-level decoding approaches including LDA.

### CCA
- Semedo et al. (2019). [Cortical areas interact through a communication subspace](https://www.cell.com/neuron/fulltext/S0896-6273(19)30053-4). Neuron. --- CCA applied to inter-area communication.

## Review Articles and Overviews

- Williamson et al. (2019). [Bridging large-scale neuronal recordings and large-scale network models using dimensionality reduction](https://arxiv.org/abs/2502.11036). --- Overview of methods and their connections.
- Musacchio (2024). [Dimensionality Reduction in Neuroscience](https://www.fabriziomusacchio.com/blog/2024-10-24-dimensionality_reduction_in_neuroscience/). --- Accessible blog post covering multiple methods.
- Musacchio (2026). [Neural Dynamics](https://www.fabriziomusacchio.com/blog/2026-02-04-neural_dynamics/). --- Blog post on neural dynamics and analysis methods.

## Software and Tutorials

- [scikit-learn: Decomposition](https://scikit-learn.org/stable/modules/decomposition.html) --- PCA, ICA, Factor Analysis, NMF implementations
- [dPCA Python package](https://github.com/machenslab/dPCA) --- Official dPCA implementation
- [TCA (TensorTools)](https://github.com/neurostatslab/tensortools) --- Python package for tensor decompositions on neural data
- [pyriemann](https://pyriemann.readthedocs.io/) --- Riemannian geometry tools for covariance matrices
