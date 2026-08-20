# Dynamic Array
## How It Works
Contiguous generic storage separates used count from geometrically grown capacity.
## Required API
`DynamicArray<T>`: constructor; `Get(int)`, `Set(int,T)`, `Insert(int,T)`, `Remove(int)`, `Count`, `Capacity`, `IsEmpty`.
## Contract
Indexes are `[0,Count)` and insert accepts Count; null elements are valid; invalid operations preserve state; the structure owns storage only.
## Complexity Targets
Access/metadata O(1), append amortized O(1), indexed insert/remove O(n), O(n) contiguous space.
