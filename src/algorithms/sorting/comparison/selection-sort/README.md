# Selection Sort
Repeatedly select the smallest remainder item into the sorted prefix.

## API
`SelectionSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place using at most n - 1 swaps.
- Equal values have no stability guarantee. Null input fails cleanly; an empty array is a valid no-op.
- Index bounds and pass limits must not overflow.

## Complexity
All cases O(n^2), O(1) space.

## Verification
Exercise sorted output and the at-most-n-minus-one-swap bound.
