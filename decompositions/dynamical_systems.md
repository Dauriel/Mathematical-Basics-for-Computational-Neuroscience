# Eigenvalues for Dynamical Systems

## Learning Objectives

By the end of this section, you should be able to:
- Analyze the stability of linear dynamical systems using eigenvalues
- Classify fixed points (stable/unstable nodes, spirals, saddles, centers)
- Interpret complex eigenvalues as oscillatory dynamics
- Connect this framework to neural dynamics and jPCA

## Outline

### Linear Dynamical Systems
- The system $\dot{\mathbf{x}} = A\mathbf{x}$, with solution $\mathbf{x}(t) = e^{At}\mathbf{x}_0$
- Discrete-time: $\mathbf{x}_{t+1} = A\mathbf{x}_t$, with solution $\mathbf{x}_t = A^t \mathbf{x}_0$

### Stability from Eigenvalues
- Continuous-time: stability determined by $\text{Re}(\lambda_i)$
  - $\text{Re}(\lambda_i) < 0$ for all $i$: **stable** (trajectories decay)
  - $\text{Re}(\lambda_i) > 0$ for some $i$: **unstable** (trajectories grow)
  - $\text{Re}(\lambda_i) = 0$: **marginal** (oscillatory, centers)
- Discrete-time: stability determined by $|\lambda_i|$
  - $|\lambda_i| < 1$: stable
  - $|\lambda_i| > 1$: unstable

### Classification of Fixed Points (2D)

| Eigenvalues | Type | Behavior |
|-------------|------|----------|
| $\lambda_1, \lambda_2 > 0$ | Unstable node | Trajectories diverge |
| $\lambda_1, \lambda_2 < 0$ | Stable node | Trajectories converge |
| $\lambda_1 > 0 > \lambda_2$ | Saddle point | Converge on one axis, diverge on another |
| $\alpha \pm i\beta$, $\alpha < 0$ | Stable spiral | Oscillating decay |
| $\alpha \pm i\beta$, $\alpha > 0$ | Unstable spiral | Oscillating growth |
| $\pm i\beta$ (purely imaginary) | Center | Persistent oscillation |

### Phase Portraits
- Visualizing trajectories in state space
- How eigenvectors determine the geometry of flow

### The Matrix Exponential
- $e^{At} = P e^{\Lambda t} P^{-1}$
- Each eigenvalue contributes a mode: $e^{\lambda_i t}$
- Complex eigenvalues: $e^{(\alpha + i\beta)t} = e^{\alpha t}(\cos\beta t + i\sin\beta t)$

:::{admonition} Neuroscience Connection
:class: tip
Neural population dynamics during movement are often well-described by rotational dynamics --- trajectories that spiral in state space. This corresponds to complex eigenvalues of the dynamics matrix, and is exactly what jPCA is designed to find. See the [jPCA/dPCA section](../linear_dimred/temporal.md).
:::

:::{admonition} Intuition
:class: note
Real eigenvalues correspond to exponential growth or decay along straight lines. Complex eigenvalues add rotation. The real part controls whether the system spirals inward (stable) or outward (unstable); the imaginary part controls the frequency of oscillation.
:::
