# Bubble Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Adjacent swaps carry the largest unsorted value to the tail per pass.

Repeated adjacent comparisons move larger values toward the end until a pass makes no swap.

## Required API

`BubbleSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract

- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place. Do not swap comparer-equal items, preserving their input order.
- A pass with no swaps stops processing. Null input fails cleanly; an empty array is a valid no-op.
- Index bounds and pass limits must not overflow.

## Complexity Targets

Best O(n), average/worst O(n^2), O(1) space.

Target: O(n^2) worst-case time and O(1) auxiliary space; insertion and bubble sort are stable, selection sort is not.

## Verification

Exercise stable equal values and the zero-swap early exit.
