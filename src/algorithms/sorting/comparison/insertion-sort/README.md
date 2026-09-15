# Insertion Sort
Shift each item left through a sorted prefix to its position.

## API
`InsertionSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract
- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place. Shift only items strictly greater than the inserted value, preserving equal-item order.
- Nearly sorted input takes the best-case path. Null input fails cleanly; an empty array is a valid no-op.
- Backward index movement must stop before underflow.

## Complexity
Best O(n), average/worst O(n^2), O(1) space.

## Verification
Exercise stable equal values and nearly sorted input.
