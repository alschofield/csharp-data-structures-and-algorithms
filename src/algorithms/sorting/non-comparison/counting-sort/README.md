# Counting Sort
Counts and prefix sums place bounded integer keys without comparisons.

## API
`CountingSort.Sort(uint[] items, uint keyLimit)`.

## Contract
- Values and `keyLimit` are unsigned value types; keys must be in `[0, keyLimit)`.
- Use a `keyLimit`-sized count array and stable output placement without comparisons.
- An invalid key or failed allocation leaves the input unchanged.
- Validate conversions and prefix sums before array allocation or indexing so unsigned-to-signed conversion and cumulative counts cannot overflow.

## Complexity
All cases O(n+k), O(n+k) auxiliary space.

## Verification
Exercise bounded keys, stable equal values, and invalid-key preservation.
