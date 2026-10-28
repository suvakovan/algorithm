# Algorithms & Data Structures

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![GitHub](https://img.shields.io/badge/Project-Open%20Source-2ea44f)](https://github.com/suvakovan/algorithm)

A practical Python learning repository for implementing core algorithms, measuring their runtime, and visualizing how performance changes as input size grows. The examples are provided as Jupyter notebooks, making it easy to experiment with the code and learn by doing.

## Table of Contents

- [Project Overview](#project-overview)
- [Notebook Guide](#notebook-guide)
- [Algorithms and Complexity](#algorithms-and-complexity)
- [Quick Start](#quick-start)
- [Run in Google Colab](#run-in-google-colab)
- [Benchmarking Tips](#benchmarking-tips)
- [What You'll Learn](#what-youll-learn)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)

## Project Overview

This repository explores searching and sorting through small, understandable Python implementations and runtime experiments. It is suitable for students practicing algorithms, Python, and basic empirical performance analysis.

## Notebook Guide

| Notebook | Topics |
| --- | --- |
| [Untitled1.ipynb](./Untitled1.ipynb) | Linear search and execution-time visualization as list size changes |
| [Untitled2.ipynb](./Untitled2.ipynb) | Insertion sort and heap-based sorting with timing comparisons |
| [untitled1.ipynb](./untitled1.ipynb) | Additional linear-search timing experiment |

## Algorithms and Complexity

| Algorithm | Best case | Average case | Worst case |
| --- | --- | --- | --- |
| Linear search | O(1) | O(n) | O(n) |
| Insertion sort | O(n) | O(n²) | O(n²) |
| Heap-based sorting | O(n log n) | O(n log n) | O(n log n) |

These are standard time-complexity estimates. Actual execution times depend on input data, implementation details, hardware, and system load.

## Quick Start

### Requirements

- Python 3
- Jupyter Notebook
- Matplotlib

### 1. Clone the repository

```bash
git clone https://github.com/suvakovan/algorithm.git
cd algorithm
```

### 2. Create and activate a virtual environment (recommended)

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

macOS / Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies and start Jupyter

```bash
python -m pip install notebook matplotlib
jupyter notebook
```

Open a notebook in the browser and run its cells from top to bottom.

## Run in Google Colab

No local setup is needed to try the notebooks in Colab:

- [Open linear search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled1.ipynb)
- [Open sorting comparison](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled2.ipynb)
- [Open additional linear search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/untitled1.ipynb)

## Benchmarking Tips

- Use the same input data when comparing algorithms.
- Repeat measurements and compare averages instead of a single run.
- Test multiple input sizes to identify growth trends.
- Keep in mind that background processes and hardware can affect results.
- Use plots as a learning aid; timing experiments do not replace complexity analysis.

## What You'll Learn

- Implement fundamental searching and sorting techniques.
- Interpret best-, average-, and worst-case time complexity.
- Measure runtime with Python.
- Visualize experimental results with Matplotlib.
- Think critically about edge cases and fair comparisons.

## Future Improvements

Possible extensions for this learning project include adding binary search, merge sort and quicksort; writing automated correctness tests; and standardizing benchmarks across algorithms and input sizes.

## Contributing

Suggestions and corrections are welcome. Open an issue to discuss an improvement, or submit a pull request with a clear explanation of the change.

## Author

**Suvakovan** · [GitHub profile](https://github.com/suvakovan)

---

*Implement. Measure. Analyze. Repeat.*
