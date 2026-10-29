# Algorithms & Data Structures

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Repository](https://img.shields.io/badge/Project-Algorithm%20Practice-2ea44f)](https://github.com/suvakovan/algorithm)

A hands-on Python repository for practicing algorithms and understanding how their performance changes as input size grows. The project uses Jupyter notebooks to explore searching, sorting, runtime measurement, and visual comparison.

## Contents

- [Project Goals](#project-goals)
- [Notebook Guide](#notebook-guide)
- [Complexity Reference](#complexity-reference)
- [Getting Started](#getting-started)
- [Run in Google Colab](#run-in-google-colab)
- [Suggested Learning Workflow](#suggested-learning-workflow)
- [Benchmarking Guidelines](#benchmarking-guidelines)
- [Ideas for Future Work](#ideas-for-future-work)
- [Contributing](#contributing)

## Project Goals

- Practice implementing fundamental algorithms in Python.
- Connect algorithm design with time-complexity analysis.
- Measure execution time across different input sizes.
- Use Matplotlib to visualize performance trends.

## Notebook Guide

| Notebook | What it covers |
| --- | --- |
| [Untitled1.ipynb](./Untitled1.ipynb) | Linear search and runtime visualization as list size changes |
| [Untitled2.ipynb](./Untitled2.ipynb) | Insertion sort and heap-based sorting with timing comparisons |
| [untitled1.ipynb](./untitled1.ipynb) | Additional linear-search timing experiment |

## Complexity Reference

| Algorithm | Best case | Average case | Worst case |
| --- | --- | --- | --- |
| Linear search | O(1) | O(n) | O(n) |
| Insertion sort | O(n) | O(n²) | O(n²) |
| Heap-based sorting | O(n log n) | O(n log n) | O(n log n) |

These are standard asymptotic estimates. The measured runtime may differ depending on input order, implementation, hardware, and system load.

## Getting Started

### Requirements

- Python 3
- Jupyter Notebook
- Matplotlib

### 1. Clone the repository

```bash
git clone https://github.com/suvakovan/algorithm.git
cd algorithm
```

### 2. Create and activate a virtual environment

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

### 3. Install dependencies and launch Jupyter

```bash
python -m pip install notebook matplotlib
jupyter notebook
```

Choose a notebook and run its cells in order.

## Run in Google Colab

You can experiment without installing Python locally:

- [Open the linear-search notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled1.ipynb)
- [Open the sorting-comparison notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled2.ipynb)
- [Open the additional linear-search notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/untitled1.ipynb)

## Suggested Learning Workflow

1. Read the algorithm and describe its steps in your own words.
2. Run the notebook with a small input and check the output.
3. Try edge cases, such as an empty list, one element, or a missing search target where applicable.
4. Increase the input size and observe the runtime plot.
5. Compare the observed trend with the expected time complexity.
6. Change one part of the experiment at a time and record what changes.

## Benchmarking Guidelines

- Compare algorithms using equivalent input data.
- Run each experiment multiple times and compare average measurements.
- Test several input sizes rather than drawing conclusions from one data point.
- Avoid running heavy background tasks during timing experiments when possible.
- Treat plots as experimental evidence, not as a substitute for complexity analysis.

## Ideas for Future Work

- Add binary search and compare it with linear search on sorted data.
- Add merge sort and quicksort to expand the sorting comparison.
- Write tests for correctness and edge cases.
- Separate algorithm implementations from benchmark and plotting code.
- Record repeated timings and summarize them in a comparison chart.

## Contributing

Feedback and improvements are welcome. Open an issue to discuss an idea, or submit a pull request with a concise description of the change and the tests or experiments you ran.

## Author

**Suvakovan** · [GitHub profile](https://github.com/suvakovan)

---

*Understand the algorithm. Measure its behavior. Learn from the results.*
