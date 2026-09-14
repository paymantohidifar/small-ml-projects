# small-ml-projects

Consolidated repo hosting various short ML/AI projects.

## Background

This repo is a collection of small, self-contained machine learning and deep learning
projects built for learning and reference purposes. Each project lives as a standalone
Jupyter notebook under `notebooks/`, covering a specific model or technique end-to-end —
from data loading through training and evaluation — with explanations alongside the code.

## Tooling Installation

This project uses [`uv`](https://docs.astral.sh/uv/) for dependency management, with
[Pixi](https://pixi.sh/) supported as an alternative. Python `3.11` is required.

### Option A: uv

1. Install `uv` (see [installation guide](https://docs.astral.sh/uv/getting-started/installation/)):

   ```bash
   curl -LsSf https://astral.sh/uv/install.sh | sh
   ```

2. Install the project and its dependencies. Choose the extra that matches your hardware
   (`cpu` or `gpu`), plus `dev` for linting/testing tools:

   ```bash
   uv pip install -e .[cpu,dev]
   # or, on a machine with a CUDA-capable GPU:
   uv pip install -e .[gpu,dev]
   ```

3. Launch JupyterLab:

   ```bash
   uv run jupyter lab
   ```

### Option B: Pixi

1. Install [Pixi](https://pixi.sh/latest/#installation).
2. Install the environment (defaults to the CPU + dev environment):

   ```bash
   pixi install
   # or, for the GPU environment:
   pixi install -e gpu-env
   ```

3. Launch JupyterLab:

   ```bash
   pixi run jupyter lab
   ```


## Notebooks

1. [`random-forest-classifier-with-feature-importance.ipynb`](notebooks/random-forest-classifier-with-feature-importance.ipynb) —
   A complete guide to data preparation, processing, and building and training a random
   forest classifier, with feature importance analysis.
2. [`autoencoders.ipynb`](notebooks/autoencoders.ipynb) —
   Autoencoders implementation in PyTorch, covering linear and convolutional architectures
   on FashionMNIST and CIFAR-10, plus denoising and sparse autoencoder variants.
3. [`vae.ipynb`](notebooks/vae.ipynb) —
   Variational autoencoders (linear and convolutional) implemented in PyTorch.
