# Algorithms & Data Structures

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Focus](https://img.shields.io/badge/Focus-Algorithms%20%26%20Analysis-2ea44f)](https://github.com/suvakovan/algorithm)

A hands-on Python repository for learning fundamental algorithms through implementation and experimentation. Explore searching and sorting techniques, measure execution time, and visualize how performance changes as input size grows.

## Table of Contents

- [Project Overview](#project-overview)
- [Repository Structure](#repository-structure)
- [Notebook Guide](#notebook-guide)
- [Complexity Reference](#complexity-reference)
- [Choosing an Algorithm](#choosing-an-algorithm)
- [Setup](#setup)
- [Run with Google Colab](#run-with-google-colab)
- [How to Experiment](#how-to-experiment)
- [Correctness Checklist](#correctness-checklist)
- [Benchmarking Notes](#benchmarking-notes)
- [Next Steps](#next-steps)
- [Contributing](#contributing)
- [Author](#author)

## Project Overview

This project is a practical workspace for connecting algorithm concepts with Python code. The notebooks demonstrate searching and sorting, collect execution-time measurements, and use Matplotlib to visualize performance trends.

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
| Heap-based sorting with `heapq` | O(n log n) | O(n log n) | O(n log n) | O(n) |

These are standard asymptotic estimates. The heap-based method builds/uses a heap and retrieves the elements in priority order; the notebook's approach requires additional storage proportional to the input. Actual timings depend on data, implementation, hardware, and system load.

## Choosing an Algorithm

| Task or situation | Suitable starting point | Reason |
| --- | --- | --- |
| Search a small or unsorted list | Linear search | Simple and does not require sorted input |
| Sort a small or nearly sorted list | Insertion sort | Low overhead and efficient for nearly sorted data |
| Repeatedly retrieve the smallest item | Heap-based approach | A heap supports efficient minimum-element retrieval |

The best choice depends on input size, input properties, memory constraints, and the operations your application needs.

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

Open a notebook in your browser and run its cells in order.

## Run with Google Colab

Try the notebooks online without a local Python setup:

- [Linear search notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled1.ipynb)
- [Sorting comparison notebook](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/Untitled2.ipynb)
- [Additional linear-search experiment](https://colab.research.google.com/github/suvakovan/algorithm/blob/main/untitled1.ipynb)

## How to Experiment

1. Read the implementation and summarize its steps.
2. Run it with a small input and verify the result.
3. Increase the input size gradually and record execution time.
4. Repeat measurements and compare the results.
5. Plot the measurements and compare the trend with theoretical complexity.
6. Change one variable at a time so the effect is easier to understand.

## Correctness Checklist

When trying an implementation, consider testing:

- An empty input, if the algorithm accepts one.
- A single-element input.
- Already sorted and reverse-sorted input for sorting algorithms.
- Duplicate values.
- A search target at the beginning, at the end, and absent from the input.
- Whether the original input is modified or preserved.

## Benchmarking Notes

- Compare algorithms with equivalent input sizes and comparable data.
- Repeat each measurement; use an average or median rather than one run.
- Keep execution conditions as consistent as possible.
- Measure the algorithm separately from plotting and display operations.
- Do not infer complexity from one timing result; use theory and repeated experiments together.

## Next Steps

Possible extensions include binary search, merge sort, quicksort, automated correctness tests, and a reusable benchmark utility for consistent comparisons.

## Contributing

Suggestions and corrections are welcome. Open an issue to discuss an improvement or submit a pull request with a clear description of the change and how it was tested.

## Author

**Suvakovan** · [GitHub profile](https://github.com/suvakovan)

---

*Implement with clarity. Measure with care. Learn through analysis.*
