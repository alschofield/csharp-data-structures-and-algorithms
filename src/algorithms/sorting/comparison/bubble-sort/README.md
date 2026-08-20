# Bubble Sort
## How It Works
Adjacent swaps carry the largest unsorted value to the tail per pass.
## Required API
`BubbleSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending in place; stable by never swapping equals; exit after a zero-swap pass; null nonempty input fails cleanly.
## Complexity Targets
Best O(n), average/worst O(n^2), O(1) space.
