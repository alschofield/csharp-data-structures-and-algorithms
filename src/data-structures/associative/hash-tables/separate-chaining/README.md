# Separate-Chaining Hash Table
## How It Works
A bucket array resolves collisions through linked chains. The table can use either a fixed-capacity or resizing set policy.
## Required API
`HashTable<TKey,TValue>`: constructors accepting a nonzero `initialCapacity` and hash/equality delegates for the fixed-capacity and resizing policies; `Set`, `TryGetValue`, `Remove`, `ContainsKey`, `Count`, `Capacity`, `IsEmpty`.
## Contract
Keys are non-null and values may be null; `Set` inserts or replaces and returns the previous value; equal replacement preserves the first key object; collisions remain correct. The fixed-capacity policy never resizes. The resizing policy doubles capacity and rehashes all entries before a new insertion would make load exceed 0.75; replacement does not resize, and the table never shrinks automatically.
## Complexity Targets
Expected O(1) with short chains, O(n/capacity) as chains grow, O(n) worst; resizing `Set` is amortized O(1), rehash is O(n), metadata is O(1); O(capacity + entries) space.
