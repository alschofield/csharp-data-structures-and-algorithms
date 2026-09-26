# Merge Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Sort halves recursively and merge them through an auxiliary buffer.

Recursively sort runs, then merge them while preserving encounter order for equal keys.

## Required API

`MergeSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract

- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending and choose the left run on comparer ties, preserving equal-item order.
- Use O(n) auxiliary buffer space. A failed allocation leaves the input unchanged.
- Null input fails cleanly; an empty array is a valid no-op. Split and merge bounds must not overflow.

## Complexity Targets

All cases O(n log n); O(n) plus O(log n) recursion space.

Target: O(n log n) time and O(n) auxiliary space; stable.

## Verification

Exercise stable merging and uneven runs.
