# Spectral Analysis: Complex Matrices and the FFT

## Learning Objectives

By the end of this section, you should be able to:
- Work with complex vector spaces and Hermitian matrices
- Understand the Discrete Fourier Transform as a change of basis
- Explain the FFT algorithm and its computational advantage
- Apply spectral analysis to time-series data

## Outline

### Complex Vector Spaces
- Complex inner product: $\langle \mathbf{u}, \mathbf{v} \rangle = \mathbf{u}^* \mathbf{v}$ (conjugate transpose)
- Hermitian matrices: $A = A^*$ (generalize symmetric matrices to $\mathbb{C}$)
- Unitary matrices: $U^* U = I$ (generalize orthogonal matrices)

### The Discrete Fourier Transform (DFT)
- The DFT matrix $F_n$ with entries $F_{jk} = \omega^{jk}$, where $\omega = e^{-2\pi i / n}$
- DFT as a change of basis: from time domain to frequency domain
- Each column of $F_n$ is a complex sinusoid at a different frequency

### The Fast Fourier Transform (FFT)
- The $O(n \log n)$ algorithm vs. naive $O(n^2)$
- Divide-and-conquer on even/odd indices (Cooley-Tukey)

### Power Spectral Density
- From DFT coefficients to power spectrum: $P(f) = |X(f)|^2$
- Parseval's theorem: total power is preserved
- Windowing and spectral leakage (brief overview)

### Spectrogram and Time-Frequency Analysis
- Short-time Fourier Transform (STFT)
- Trade-off between time and frequency resolution

:::{admonition} Neuroscience Connection
:class: tip
Spectral analysis is fundamental to understanding neural oscillations --- alpha, beta, gamma rhythms. The FFT converts raw voltage traces (LFP, EEG) into frequency content, revealing oscillatory structure that is invisible in the time domain.
:::
