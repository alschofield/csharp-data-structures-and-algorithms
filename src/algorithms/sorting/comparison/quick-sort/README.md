# Quick Sort
## How It Works
Partition around a defended pivot and recurse on both sides.
## Required API
`QuickSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending in place; not stable; use median-of-three or randomized pivots; handle all-equal input without unbounded recursion; null nonempty input fails cleanly.
## Complexity Targets
Best/average O(n log n), worst O(n^2), expected O(log n) recursion space.
