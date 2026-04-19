# Neural Manifolds and Topology

## Learning Objectives

By the end of this section, you should be able to:
- Explain the neural manifold hypothesis
- Describe what topology is and why it matters for neural data
- Understand basic concepts of topological data analysis (TDA)
- Interpret persistent homology and Betti numbers

## Outline

### The Neural Manifold Hypothesis
- Neural population activity is high-dimensional (one dimension per neuron)
- But the activity is constrained to a low-dimensional manifold
- The geometry of this manifold reflects the structure of the computation

### What Is a Manifold?
- Informally: a smooth, curved surface that locally looks like $\mathbb{R}^d$
- Examples: a circle ($S^1$), a sphere ($S^2$), a torus ($T^2$)
- Intrinsic dimension vs. embedding dimension
- The manifold may have non-trivial topology (holes, twists)

### Topology: Beyond Geometry
- Topology studies properties preserved under continuous deformation
- A coffee mug and a donut are topologically equivalent (genus 1)
- Key question: what is the topology of the neural manifold?

### Topological Data Analysis (TDA)
- **Simplicial complexes:** building a combinatorial approximation of the manifold from data points
- **Vietoris-Rips complex:** connect points within distance $\varepsilon$, form simplices from cliques
- **Persistent homology:** track topological features (connected components, loops, voids) as $\varepsilon$ varies
- **Betti numbers:** $\beta_0$ = connected components, $\beta_1$ = loops, $\beta_2$ = voids
- **Persistence diagrams and barcodes:** visualizing which features persist across scales

### Interpreting Neural Topology
- A ring in neural state space may indicate a circular variable (e.g., head direction)
- A torus may indicate two independent circular variables
- Topology constrains the possible computations the network can implement

:::{admonition} Neuroscience Connection
:class: tip
Gardner et al. showed that head direction cells in the fly form a ring manifold, matching the topology of the represented variable. The Laplace Neural Manifold framework extends this to working memory representations.
:::

:::{admonition} Key Resources
:class: seealso
- Colah's blog: [Neural Networks, Manifolds, and Topology](https://colah.github.io/posts/2014-03-NN-Manifolds-Topology/)
- Chaudhuri et al. (eLife, reviewed preprint): ["What" x "When" working memory representations using Laplace Neural Manifolds](https://elifesciences.org/reviewed-preprints/108804)
:::
