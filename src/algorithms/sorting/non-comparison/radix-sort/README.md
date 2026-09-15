# Radix Sort
Stable least-significant-digit counting passes sort fixed-width unsigned keys.

## API
`RadixSort.Sort(uint[] items)`.

## Contract
- Input values are unsigned value types, so sorting needs no negative-key policy.
- Process least-significant to most-significant digits with stable fixed-radix counting passes.
- Preserve equal-value order and reuse auxiliary storage across passes.
- A failed allocation leaves the input unchanged. Digit extraction, counts, and indexes must not overflow.

## Complexity
All cases O(d(n+k)), O(n+k) auxiliary space.

## Verification
Exercise stable LSD passes and equal values.
