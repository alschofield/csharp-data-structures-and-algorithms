# Binary Search
## How It Works
Midpoint comparisons halve a sorted candidate range.
## Required API
`BinarySearch.IndexOf<T>(T[] items, T key, IComparer<T>)` returning `int?`.
## Contract
Requires ascending input without validating or sorting; midpoint cannot overflow; any duplicate match is valid; empty/null is not found; no mutation.
## Complexity Targets
Best O(1), average/worst O(log n), O(1) iterative space.
