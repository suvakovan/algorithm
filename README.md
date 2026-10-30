# Algorithms & Data Structures

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Repository](https://img.shields.io/badge/Focus-Algorithms%20%26%20Analysis-2ea44f)](https://github.com/suvakovan/algorithm)

A hands-on Python repository for learning fundamental algorithms through implementation and experimentation. Explore searching and sorting techniques, measure execution time, and use visualizations to understand how performance changes as input size grows.

## Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Notebook Guide](#notebook-guide)
- [Complexity Reference](#complexity-reference)
- [Setup](#setup)
- [Run with Google Colab](#run-with-google-colab)
- [How to Experiment](#how-to-experiment)
- [Benchmarking Notes](#benchmarking-notes)
- [Next Steps](#next-steps)
- [Contributing](#contributing)
- [Author](#author)

## Project Overview

The notebooks focus on practical algorithm learning: implement a technique, run it with different inputs, measure its execution time, and compare the observed behavior with its theoretical complexity. Matplotlib is used for performance visualization.

## Repository Structure

```text
algorithm/
├── README.md
├── Untitled1.ipynb
├── Untitled2.ipynb
└── untitled1.ipynb
```

## Notebook Guide

| Notebook | Main topic |
| --- | --- |
| [Untitled1.ipynb](./Untitled1.ipynb) | Linear search and execution-time visualization |
| [Untitled2.ipynb](./Untitled2.ipynb) | Insertion sort and heap-based sorting comparisons |
| [untitled1.ipynb](./untitled1.ipynb) | Additional linear-search timing experiment |

## Complexity Reference

| Algorithm | Best time | Average time | Worst time | Auxiliary space |
| --- | --- | --- | --- | --- |
| Linear search | O(1) | O(n) | O(n) | O(1) |
| Insertion sort | O(n) | O(n²) | O(n²) | O(1) |
| Heap-based sorting (heapq) | O(n log n) | O(n log n) | O(n log n) | O(n) |

Complexities are standard estimates. The heap-based notebook approach uses a heap to retrieve elements in sorted order; its auxiliary storage is linear in the number of elements. Actual runtime depends on input data, implementation, hardware, and system load.

## Setup

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

Open a notebook in the browser and execute its cells in order.

## Run with Google Colab

Try the notebooks online without setting up a local Python environment:

- [Linear search notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled1.ipynb)
- [Sorting comparison notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled2.ipynb)
- [Additional linear-search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/untitled1.ipynb)

## How to Experiment

1. Start with a small input and verify the algorithm's output.
2. Try edge cases, including empty inputs, single-element inputs, and unsuccessful searches where applicable.
3. Increase the input size gradually and record the execution time.
4. Repeat measurements to reduce the effect of random system variation.
5. Plot the results and compare the trend with the expected complexity.
6. Explain any difference between theoretical growth and observed timings.

## Benchmarking Notes

- Use equivalent input sizes and comparable data when evaluating algorithms.
- Repeat each measurement and compare averages or medians.
- Keep the machine and execution conditions as consistent as possible.
- Remember that plotting and notebook overhead can affect measurements.
- Do not infer an algorithm's complexity from a single timing result.

## Next Steps

Potential extensions include binary search, merge sort, quicksort, automated correctness tests, and a shared benchmark utility to compare multiple algorithms using consistent inputs.

## Contributing

Suggestions and corrections are welcome. Open an issue to discuss an improvement or submit a pull request with a clear description of the change and how it was tested.

## Author

**Suvakovan** · [GitHub profile](https://github.com/suvakovan)

---

*Implement with clarity. Measure with care. Learn through analysis.*
