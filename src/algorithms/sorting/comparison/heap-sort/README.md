# Heap Sort
Bottom-up max-heapify and root extraction sort an implicit array heap.

## API
`HeapSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place with no stability guarantee.
- Build the implicit max heap bottom-up in O(n); do not allocate heap nodes.
- Null input fails cleanly; an empty array is a valid no-op. Child-index arithmetic must not overflow.

## Complexity
All cases O(n log n), O(1) iterative space.

## Verification
Exercise bottom-up heapify and unstable equal values.
