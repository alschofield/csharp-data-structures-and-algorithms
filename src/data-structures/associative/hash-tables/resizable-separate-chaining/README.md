# Resizable Separate-Chaining Hash Table
## How It Works
Linked collision chains are rehashed into doubled capacity before load exceeds 0.75.
## Required API
`ResizableHashTable<TKey,TValue>`: hash/equality constructor; `Set`, `TryGetValue`, `Remove`, `ContainsKey`, `Count`, `Capacity`, `IsEmpty`.
## Contract
Start at ten buckets; retain original equal key; rehash before insertion exceeds 0.75; failed resize preserves state; never shrink automatically.
## Complexity Targets
Operations expected amortized O(1), O(n) worst; rehash O(n) amortized; O(capacity + entries) space.
