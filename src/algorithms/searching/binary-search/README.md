# Binary Search

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Midpoint comparisons halve a sorted candidate range.

Repeatedly compare the target with the middle of a sorted range and discard one half.

## Required API

`BinarySearch.IndexOf<T>(T[] items, T key, IComparer<T>)` returning `int?`.

## Contract

- `T` is unconstrained; the supplied comparer defines ascending order for reference and value types.
- The caller supplies ascending input. The method neither sorts nor validates that precondition.
- Midpoint calculation cannot overflow. Any index holding an equal duplicate is valid.
- Empty or null input has no match; the array is never mutated.

## Complexity Targets

Best O(1), average/worst O(log n), O(1) iterative space.

Target: O(log n) time and O(1) auxiliary space.

## Verification

Exercise both boundaries, duplicates, and absent or empty sorted input.
