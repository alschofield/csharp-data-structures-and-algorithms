# Heap Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Bottom-up max-heapify and root extraction sort an implicit array heap.

A complete tree stored in an array maintains its heap invariant by sifting values up or down.

## Required API

`HeapSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract

- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place with no stability guarantee.
- Build the implicit max heap bottom-up in O(n); do not allocate heap nodes.
- Null input fails cleanly; an empty array is a valid no-op. Child-index arithmetic must not overflow.

## Complexity Targets

All cases O(n log n), O(1) iterative space.

Target: O(n log n) time, O(1) auxiliary space, and unstable ordering.

## Verification

Exercise bottom-up heapify and unstable equal values.
