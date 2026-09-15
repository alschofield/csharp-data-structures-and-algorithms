# Linear Search
Scan in order until the first match or exhaustion.

## API
`LinearSearch.IndexOf<T>(T[] items, T key, IComparer<T>)` returning `int?`.

## Contract
- `T` is unconstrained; the supplied comparer defines equality for reference and value types.
- Input may be unsorted. The first equal item is returned.
- Empty or null input has no match. The array and its elements are never mutated.
- The returned index is an existing array index; scanning uses incrementing bounds that do not overflow.

## Complexity
Best O(1), average/worst O(n), O(1) space.

## Verification
Exercise unsorted input, the first duplicate, and absent or empty input.
