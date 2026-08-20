# Separate-Chaining Hash Table
## How It Works
A fixed ten-bucket array resolves collisions through linked chains.
## Required API
`HashTable<TKey,TValue>`: constructor accepting hash/equality delegates; `Set`, `TryGetValue`, `Remove`, `ContainsKey`, `Count`, `IsEmpty`.
## Contract
Keys are non-null and values may be null; replacement returns the old value and retains the original key; collisions work; fixed capacity never rehashes.
## Complexity Targets
Expected O(1), O(n/buckets) as chains grow, O(n) worst; metadata O(1); O(entries + 10) space.
