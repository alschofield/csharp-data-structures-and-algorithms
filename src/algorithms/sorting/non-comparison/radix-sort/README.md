# Radix Sort
## How It Works
Stable least-significant-digit counting passes sort fixed-width unsigned keys.
## Required API
`RadixSort.Sort(uint[] items)`.
## Contract
Process LSD to MSD with stable fixed-radix counting passes; preserve equal order; reuse auxiliary storage; allocation failure preserves input.
## Complexity Targets
All cases O(d(n+k)), O(n+k) auxiliary space.
