# Union-Find
## How It Works
A parent forest uses path compression and union by rank or size.
## Required API
`UnionFind`: constructor `(int)`; `Find`, `Union`, `Connected`, `SetCount`.
## Contract
Elements are `[0,n)` and begin singleton; invalid values fail cleanly; redundant union changes neither ranks nor count; representatives are equality-only.
## Complexity Targets
Find/union/connected amortized O(alpha(n)); construction O(n); O(n) space.
