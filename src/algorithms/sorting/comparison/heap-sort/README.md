# Heap Sort
## How It Works
Bottom-up max-heapify and root extraction sort an implicit array heap.
## Required API
`HeapSort.Sort<T>(T[] items, IComparer<T>)`.
## Contract
Sort ascending; not stable; use bottom-up O(n) heap construction and no nodes; null nonempty input fails cleanly.
## Complexity Targets
All cases O(n log n), O(1) iterative space.
