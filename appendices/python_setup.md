# Python Setup

This page explains how to set up a Python environment to run the interactive notebooks locally.

## Option 1: Google Colab (No Installation)

The easiest way to run the notebooks is via Google Colab. Each notebook page has a "Launch on Colab" button at the top. Click it, and you can run the code directly in your browser.

## Option 2: Local Installation

### 1. Install Python

We recommend Python 3.10 or later. Download from [python.org](https://www.python.org/downloads/) or use a package manager:

```bash
# macOS (Homebrew)
brew install python@3.11

# Ubuntu/Debian
sudo apt install python3.11
```

### 2. Create a Virtual Environment

```bash
# Navigate to the course directory
cd Caro_Course

# Create a virtual environment
python3 -m venv .venv

# Activate it
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate      # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter

```bash
jupyter notebook
```

Then navigate to the `demos/` folders within each module to find the interactive notebooks.

## Key Packages

| Package | What it does |
|---------|-------------|
| `numpy` | Array operations, linear algebra |
| `scipy` | Scientific computing, sparse matrices, optimization |
| `matplotlib` | Static plots and figures |
| `plotly` | Interactive plots (the main visualization tool in our demos) |
| `scikit-learn` | PCA, K-Means, DBSCAN, and many other methods |
| `pandas` | Data manipulation |
| `ipywidgets` | Interactive widgets in notebooks |

## Building the Book Locally

If you want to build the full website locally:

```bash
pip install -r requirements.txt
jupyter-book build .
```

The output will be in `_build/html/`. Open `_build/html/index.html` in your browser.
