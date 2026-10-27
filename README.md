# Algorithms & Data Structures

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Repository](https://img.shields.io/badge/Repository-Learning%20Project-2ea44f)](https://github.com/suvakovan/algorithm)

A hands-on Python repository for learning algorithms, implementing core techniques, and exploring how execution time changes as input size grows. Examples are organized as Jupyter notebooks and include plots for basic performance experiments.

## Contents

- [Overview](#overview)
- [Notebooks](#notebooks)
- [Algorithms at a Glance](#algorithms-at-a-glance)
- [Getting Started](#getting-started)
- [Running the Notebooks](#running-the-notebooks)
- [Notes on Benchmarking](#notes-on-benchmarking)
- [Learning Objectives](#learning-objectives)
- [Contributing](#contributing)
- [Author](#author)

## Overview

This repository is intended as a practical space to:

- Implement searching and sorting algorithms in Python.
- Measure execution time on inputs of different sizes.
- Visualize experimental results with Matplotlib.
- Build familiarity with algorithm analysis and time complexity.

## Notebooks

| Notebook | Focus |
| --- | --- |
| [Untitled1.ipynb](./Untitled1.ipynb) | Linear search and a plot of execution time against list size |
| [Untitled2.ipynb](./Untitled2.ipynb) | Insertion sort and heap-based sorting, with timing comparisons |
| [untitled1.ipynb](./untitled1.ipynb) | Additional linear-search timing experiment |

### Open in Google Colab

- [Linear search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled1.ipynb)
- [Sorting comparison](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled2.ipynb)
- [Additional linear search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/untitled1.ipynb)

## Algorithms at a Glance

| Algorithm | Typical time complexity | Notes |
| --- | --- | --- |
| Linear search | O(n) | Checks elements sequentially; worst-case time grows linearly with input size |
| Insertion sort | O(n²) worst case | Simple in-place sorting algorithm; efficient for small or nearly sorted inputs |
| Heap-based sorting | O(n log n) | The notebook uses Python's heapq module to repeatedly retrieve the smallest element |

Complexities describe typical algorithmic behavior, not guaranteed wall-clock timings for a particular run.

## Getting Started

### Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Matplotlib

### 1. Clone the repository

\`\`\`bash
git clone https://github.com/suvakovan/algorithm.git
cd algorithm
\`\`\`

### 2. Create a virtual environment (recommended)

\`\`\`bash
python -m venv .venv
\`\`\`

Activate it on Windows:

\`\`\`powershell
.venv\\Scripts\\Activate.ps1
\`\`\`

Or on macOS/Linux:

\`\`\`bash
source .venv/bin/activate
\`\`\`

### 3. Install dependencies

\`\`\`bash
python -m pip install notebook matplotlib
\`\`\`

### 4. Launch Jupyter

\`\`\`bash
jupyter notebook
\`\`\`

Open a notebook and run its cells in order. You can also open the notebooks directly in Google Colab using the links above.

## Notes on Benchmarking

The notebooks use small timing experiments and Matplotlib charts to illustrate how runtime changes with input size. Results can vary with hardware, system load, random input, and measurement precision. For reliable comparisons, repeat each experiment several times, use the same input data when comparing algorithms, and compare averages rather than relying on a single run.

## Learning Objectives

- Strengthen problem-solving skills through implementation.
- Relate code behavior to time complexity.
- Practice collecting and visualizing experimental data.
- Improve code clarity and test edge cases.

## Contributing

This is a personal learning project, and the notebooks may evolve over time. Suggestions and constructive feedback are welcome. Open an issue to discuss a correction or improvement.

## Author

**Suvakovan** — [GitHub profile](https://github.com/suvakovan)

---

*Learn by implementing. Improve by measuring. Understand by analyzing.*