# Mathematical Basics for Computational Neuroscience

A seminar course on the mathematical foundations for computational neuroscience.

## Building the site locally

```bash
# Install dependencies
pip install -r requirements.txt

# Build the book
jupyter-book build .

# Open in browser
open _build/html/index.html
```

## Structure

```
foundations/       - Module 1: Matrix theory, properties, tensors, change of basis
decompositions/    - Module 2: Eigentheory, dynamical systems, SVD, spectral analysis
linear_dimred/     - Module 3: PCA, LDA, dPCA, jPCA, TCA, CCA, ICA, FA, MDS
nonlinear/         - Module 4: UMAP, CEBRA, K-Means, DBSCAN
topology/          - Module 5: Neural manifolds, topology, method selection
appendices/        - Notation, method comparison, setup guide
```

## Deployment

The site auto-deploys to GitHub Pages via GitHub Actions on every push to `main`. See `.github/workflows/deploy.yml`.

## Adding content

1. Edit or create `.md` files (MyST Markdown) or `.ipynb` notebooks
2. Update `_toc.yml` if adding new pages
3. Add paper citations to `references.bib`
4. Push to `main` --- the site rebuilds automatically
