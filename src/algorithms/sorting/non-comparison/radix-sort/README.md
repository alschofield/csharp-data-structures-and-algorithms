# Radix Sort

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Stable least-significant-digit counting passes sort fixed-width unsigned keys.

Apply stable digit-wise passes from least significant digit to most significant digit.

## Required API

`RadixSort.Sort(uint[] items)`.

## Contract

- Input values are unsigned value types, so sorting needs no negative-key policy.
- Process least-significant to most-significant digits with stable fixed-radix counting passes.
- Preserve equal-value order and reuse auxiliary storage across passes.
- A failed allocation leaves the input unchanged. Digit extraction, counts, and indexes must not overflow.

## Complexity Targets

All cases O(d(n+k)), O(n+k) auxiliary space.

Target: O(d(n + k)) time and O(n + k) auxiliary space for d digits; stable.

## Verification

Exercise stable LSD passes and equal values.
