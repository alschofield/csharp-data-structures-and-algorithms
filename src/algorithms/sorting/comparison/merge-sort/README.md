# Merge Sort
Sort halves recursively and merge them through an auxiliary buffer.

## API
`MergeSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending and choose the left run on comparer ties, preserving equal-item order.
- Use O(n) auxiliary buffer space. A failed allocation leaves the input unchanged.
- Null input fails cleanly; an empty array is a valid no-op. Split and merge bounds must not overflow.

## Complexity
All cases O(n log n); O(n) plus O(log n) recursion space.

## Verification
Exercise stable merging and uneven runs.
