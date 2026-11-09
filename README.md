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
- [Understanding Big-O](#understanding-big-o)
- [Troubleshooting](#troubleshooting)
- [Choosing an Algorithm](#choosing-an-algorithm)
- [Setup](#setup)
- [Run with Google Colab](#run-with-google-colab)
- [How to Experiment](#how-to-experiment)
- [Practice Challenges](#practice-challenges)
- [Algorithm Design Checklist](#algorithm-design-checklist)
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
| [untitled1.ipynb](./untitled1.ipynb) | Linear-search timing and recursive binary-search timing |

## Complexity Reference

| Algorithm | Best time | Average time | Worst time | Auxiliary space |
| --- | --- | --- | --- | --- |
| Linear search | O(1) | O(n) | O(n) | O(1) |
| Recursive binary search on a sorted list | O(1) | O(log n) | O(log n) | O(log n) |
| Insertion sort | O(n) | O(n²) | O(n²) | O(1) |
| Heap-based sorting with `heapq` | O(n log n) | O(n log n) | O(n log n) | O(n) |

These are standard asymptotic estimates. Recursive binary search requires sorted input and uses O(log n) auxiliary call-stack space in the worst case. The heap-based method builds/uses a heap and retrieves the elements in priority order; the notebook's approach requires additional storage proportional to the input. Actual timings depend on data, implementation, hardware, and system load.

## Understanding Big-O

Big-O notation describes how an algorithm's resource usage grows as the input size, usually written as `n`, increases. It is about growth rate rather than an exact execution time.

| Complexity | Common name | Practical intuition |
| --- | --- | --- |
| O(1) | Constant | The work stays roughly the same as input grows |
| O(log n) | Logarithmic | The problem size is reduced by a constant factor at each step |
| O(n) | Linear | Work grows in proportion to the number of items |
| O(n log n) | Linearithmic | Common in efficient general-purpose sorting |
| O(n²) | Quadratic | Nested passes over the input can make work grow quickly |

For example, linear search may inspect every element in an unsorted list, so its worst-case time is O(n). Insertion sort may shift many earlier elements for each new element, so its worst-case time is O(n²).

When comparing algorithms, consider both time complexity and auxiliary space. Also remember that Big-O describes growth for large inputs; small inputs and implementation details can affect real-world performance.

## Troubleshooting

| Issue | What to try |
| --- | --- |
| `jupyter` command is not found | Activate the virtual environment and run `python -m pip install notebook` |
| Matplotlib import fails | Run `python -m pip install matplotlib` in the same environment used by Jupyter |
| Notebook cells use the wrong Python environment | In Jupyter, select the kernel associated with your project environment |
| A plot does not appear | Re-run the plotting cell and check that the measurement lists contain data |
| Timings vary between runs | Close unnecessary background tasks and repeat the benchmark several times |

If an issue persists, note the command you ran, the full error message, and your Python version before investigating further.

## Choosing an Algorithm

| Task or situation | Suitable starting point | Reason |
| --- | --- | --- |
| Search a small or unsorted list | Linear search | Simple and does not require sorted input |
| Search a sorted list repeatedly | Binary search | Halves the remaining search interval at each step; the list must stay sorted |
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
- In the notebooks, input generation is outside the timed region. In `untitled1.ipynb`, sorting is also completed before the binary-search timer starts, so that plot measures search time rather than the total cost of sorting and searching.
- The current experiments take a single timing sample for each input size. For more reliable comparisons, repeat each case many times, use `time.perf_counter()`, and compare a median.



## Practice Challenges

Use these exercises to check your understanding and extend the notebook experiments.

### Linear search

1. Implement a function that returns the index of the first matching value.
2. Return `-1` when the target is not present.
3. Test the function with an empty list, duplicate values, and a target at different positions.

### Insertion sort

1. Trace the algorithm by hand for `[5, 2, 4, 1]`.
2. Modify the implementation to sort in descending order.
3. Compare the number of shifts for an already sorted list and a reverse-sorted list.

### Heap-based sorting

1. Use Python's `heapq` module to retrieve values in ascending order.
2. Try a list containing duplicate and negative values.
3. Explain why building a separate heap requires additional memory.

### Analysis questions

- Which input makes linear search perform the most comparisons?
- Why is insertion sort often effective on nearly sorted data?
- What is the difference between an algorithm's time complexity and its measured runtime?
- Why should benchmark runs use the same input data when comparing implementations?



## Algorithm Design Checklist

Before implementing a new algorithm, work through these steps:

1. **Define the problem:** State the expected input, output, and constraints.
2. **Work through examples:** Include normal cases, boundary cases, and invalid inputs where relevant.
3. **Choose an approach:** Consider a straightforward solution first, then compare alternatives.
4. **Write the logic:** Use short pseudocode or a step-by-step explanation before coding.
5. **Implement clearly:** Prefer meaningful names and small functions.
6. **Verify correctness:** Test edge cases and compare results with a simple reference solution when possible.
7. **Analyze efficiency:** Estimate time and auxiliary space complexity.
8. **Measure performance:** Benchmark only after correctness is established.

### Example: Linear search pseudocode

```text
LINEAR-SEARCH(items, target)
    for each index i in items
        if items[i] equals target
            return i
    return -1
```

The loop may inspect every element, so the worst-case time complexity is O(n). It uses O(1) auxiliary space when it does not create another collection.


## Next Steps

Possible extensions include binary search, merge sort, quicksort, automated correctness tests, and a reusable benchmark utility for consistent comparisons.

## Contributing

Suggestions and corrections are welcome. Open an issue to discuss an improvement or submit a pull request with a clear description of the change and how it was tested.

## Author

**Suvakovan** · [GitHub profile](https://github.com/suvakovan)

---

*Implement with clarity. Measure with care. Learn through analysis.*
