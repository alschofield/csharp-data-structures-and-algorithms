# Binary Heap
## How It Works
An implicit contiguous complete tree uses sift-up and sift-down.
## Required API
`BinaryHeap<T>`: comparer constructor; `Push`, `Pop`, `Peek`, `Count`, `IsEmpty`.
## Contract
Use children `2i+1` and `2i+2`, no nodes; empty access fails cleanly; equal priorities have no stable order; growth failure preserves state.
## Complexity Targets
Push/pop O(log n), peek/metadata O(1), bottom-up build O(n), O(n) space.
