# Separate-Chaining Hash Table
A bucket array resolves collisions through linked chains. The table can use either a fixed-capacity or resizing set policy.

## API
`HashTable<TKey,TValue>`: constructors accepting a nonzero `initialCapacity` and hash/equality delegates for the fixed-capacity and resizing policies; `Set`, `TryGetValue`, `Remove`, `ContainsKey`, `Count`, `Capacity`, `IsEmpty`.

## Contract
- `TKey` and `TValue` are unconstrained. Keys are non-null; values, including null reference values, are valid.
- `Set` inserts or replaces and returns the previous value. Equal-key replacement preserves the first key object and leaves `Count` unchanged.
- Colliding keys remain independently retrievable and removable. Hash normalization, bucket selection, and capacity doubling must not overflow.
- The fixed-capacity policy never resizes. The resizing policy doubles and rehashes before a new insertion would exceed load 0.75; replacement does not resize, and neither policy shrinks automatically.

## Complexity
Expected O(1) with short chains, O(n/capacity) as chains grow, O(n) worst; resizing `Set` is amortized O(1), rehash is O(n), metadata is O(1); O(capacity + entries) space.

## Verification
Exercise collisions, replacement, explicit nonzero capacity, both policies, capacity reporting, resize-and-rehash at 0.75, and no automatic shrink.
