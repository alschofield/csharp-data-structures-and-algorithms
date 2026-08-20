# Insertion Sort
## How It Works
Shift each item left through a sorted prefix to its position.
## Required API
`InsertionSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending in place; shift only strictly greater values for stability; adapt to nearly sorted input; null nonempty input fails cleanly.
## Complexity Targets
Best O(n), average/worst O(n^2), O(1) space.
