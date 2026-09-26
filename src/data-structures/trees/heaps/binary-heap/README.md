# Binary Heap

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

An implicit contiguous complete tree uses sift-up and sift-down.

A complete tree stored in an array maintains its heap invariant by sifting values up or down.

## Required API

`BinaryHeap<T>`: comparer constructor; `Push`, `Pop`, `Peek`, `Count`, `IsEmpty`.

## Contract

- `T` is unconstrained; the supplied comparer defines priority for reference and value types.
- Array child calculations are `2i + 1` and `2i + 2`; index arithmetic must not overflow.
- `Pop` removes the highest-priority item and `Peek` does not mutate. Empty access fails without mutation.
- Equal priorities have no promised stable order. Failed growth preserves heap state.

## Complexity Targets

Push/pop O(log n), peek/metadata O(1), bottom-up build O(n), O(n) space.

## Verification

Exercise heap ordering, empty access, and equal priorities.
