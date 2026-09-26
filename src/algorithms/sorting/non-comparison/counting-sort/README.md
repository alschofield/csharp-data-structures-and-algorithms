# Counting Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Counts and prefix sums place bounded integer keys without comparisons.

Count occurrences in a bounded integer-key range, then place values using cumulative counts.

## Required API

`CountingSort.Sort(uint[] items, uint keyLimit)`.

## Contract

- Values and `keyLimit` are unsigned value types; keys must be in `[0, keyLimit)`.
- Use a `keyLimit`-sized count array and stable output placement without comparisons.
- An invalid key or failed allocation leaves the input unchanged.
- Validate conversions and prefix sums before array allocation or indexing so unsigned-to-signed conversion and cumulative counts cannot overflow.

## Complexity Targets

All cases O(n+k), O(n+k) auxiliary space.

Target: O(n + k) time and O(n + k) space for key range k; stable.

## Verification

Exercise bounded keys, stable equal values, and invalid-key preservation.
