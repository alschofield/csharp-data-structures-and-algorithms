# Quick Sort
Partition around a defended pivot and recurse on both sides.

## API
`QuickSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place with no stability guarantee.
- Use a median-of-three or randomized pivot. Equal-heavy input must still make partition progress and avoid unbounded recursion.
- Null input fails cleanly; an empty array is a valid no-op. Partition and midpoint arithmetic must not overflow.

## Complexity
Best/average O(n log n), worst O(n^2), expected O(log n) recursion space.

## Verification
Exercise sorted, reverse-sorted, equal-heavy input, and pivot defense.
