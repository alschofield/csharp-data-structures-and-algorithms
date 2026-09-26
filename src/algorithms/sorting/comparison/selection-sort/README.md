# Selection Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Repeatedly select the smallest remainder item into the sorted prefix.

Each pass selects the smallest remaining value and places it at the next output position.

## Required API

`SelectionSort.Sort<T>(T[] items, IComparer<T>)`.

## Contract

- `T` is unconstrained; the comparer orders both reference and value types.
- Sort ascending in place using at most n - 1 swaps.
- Equal values have no stability guarantee. Null input fails cleanly; an empty array is a valid no-op.
- Index bounds and pass limits must not overflow.

## Complexity Targets

All cases O(n^2), O(1) space.

Target: O(n^2) worst-case time and O(1) auxiliary space; insertion and bubble sort are stable, selection sort is not.

## Verification

Exercise sorted output and the at-most-n-minus-one-swap bound.
