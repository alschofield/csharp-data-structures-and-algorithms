# Selection Sort
## How It Works
Repeatedly select the smallest remainder item into the sorted prefix.
## Required API
`SelectionSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending in place; make at most n-1 swaps; classic form is not stable; null nonempty input fails cleanly.
## Complexity Targets
All cases O(n^2), O(1) space.
