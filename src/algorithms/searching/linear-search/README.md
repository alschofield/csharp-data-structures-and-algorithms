# Linear Search
## How It Works
Scan in order until the first match or exhaustion.
## Required API
`LinearSearch.IndexOf<T>(T[] items, T key, IComparer<T>)` returning `int?`.
## Contract
Works unsorted; returns first duplicate; empty/null input is not found; input is never modified.
## Complexity Targets
Best O(1), average/worst O(n), O(1) space.
