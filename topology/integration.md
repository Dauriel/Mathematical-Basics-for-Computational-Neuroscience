# Integration and Future Directions

## Learning Objectives

By the end of this section, you should be able to:
- Connect the methods covered in this seminar into a coherent framework
- Identify open questions and active research directions
- Discuss the relationship between dimensionality reduction and neural computation

## Outline

### The Big Picture
- Linear algebra provides the foundation for nearly all neural data analysis methods
- The progression: raw data $\to$ matrix/tensor $\to$ decomposition $\to$ interpretation
- Each method makes different assumptions and reveals different structure

### Connections Between Methods
- PCA $\leftrightarrow$ SVD $\leftrightarrow$ Eigendecomposition: the fundamental equivalence
- LDA as "supervised PCA": changing the objective from variance to discriminability
- dPCA as "structured PCA": decomposing by task variable
- jPCA as "dynamical PCA": fitting dynamics to PCA-projected data
- UMAP as "non-linear PCA": preserving manifold structure instead of variance
- CEBRA as "learned embedding": using neural networks to find task-relevant structure

### Open Questions
- **How many dimensions does neural computation really use?** (dimensionality vs. rank)
- **Linear vs. non-linear manifolds:** when does non-linearity matter?
- **Dynamics on manifolds:** combining topology with dynamical systems
- **Scaling to modern datasets:** millions of neurons, many brain areas
- **Interpretability:** what do the components *mean* biologically?

### Future Directions
- Foundation models for neural data
- Cross-species and cross-area alignment methods
- Real-time dimensionality reduction for brain-computer interfaces
- Integration of neural and behavioral manifolds

### Discussion Questions
*For the seminar session:*
1. Which method did you find most surprising or counterintuitive? Why?
2. For your own research question, which analysis pipeline would you use?
3. What are the biggest limitations of the linear algebra framework for understanding the brain?
