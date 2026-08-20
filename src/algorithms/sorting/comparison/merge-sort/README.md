# Merge Sort
## How It Works
Sort halves recursively and merge them through an auxiliary buffer.
## Required API
`MergeSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending and stable by choosing left on ties; allocate O(n) buffer; allocation failure preserves input; null nonempty input fails cleanly.
## Complexity Targets
All cases O(n log n); O(n) plus O(log n) recursion space.
