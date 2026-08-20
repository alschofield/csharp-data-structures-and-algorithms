# Counting Sort
## How It Works
Counts and prefix sums place bounded integer keys without comparisons.
## Required API
`CountingSort.Sort(uint[] items, uint keyLimit)`.
## Contract
Keys are `[0,keyLimit)`; use a size-k counts array and stable output placement; no comparisons; invalid keys or allocation failure preserve input.
## Complexity Targets
All cases O(n+k), O(n+k) auxiliary space.
