# Insertion Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Shift each item left through a sorted prefix to its position.

Each next value is inserted into the already sorted prefix by shifting larger values right.

## Required API

`InsertionSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract

- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place. Shift only items strictly greater than the inserted value, preserving equal-item order.
- Nearly sorted input takes the best-case path. Null input fails cleanly; an empty array is a valid no-op.
- Backward index movement must stop before underflow.

## Complexity Targets

Best O(n), average/worst O(n^2), O(1) space.

Target: O(n^2) worst-case time and O(1) auxiliary space; insertion and bubble sort are stable, selection sort is not.

## Verification

Exercise stable equal values and nearly sorted input.
