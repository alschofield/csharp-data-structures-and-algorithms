# Bubble Sort
Adjacent swaps carry the largest unsorted value to the tail per pass.

## API
`BubbleSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place. Do not swap comparer-equal items, preserving their input order.
- A pass with no swaps stops processing. Null input fails cleanly; an empty array is a valid no-op.
- Index bounds and pass limits must not overflow.

## Complexity
Best O(n), average/worst O(n^2), O(1) space.

## Verification
Exercise stable equal values and the zero-swap early exit.
