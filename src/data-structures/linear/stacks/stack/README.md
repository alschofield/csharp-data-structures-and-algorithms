# Stack
## How It Works
An array-backed LIFO keeps its top at the last used index.
## Required API
`Stack<T>`: constructor; `Push(T)`, `Pop()`, `Peek()`, `Count`, `IsEmpty`.
## Contract
Null values are valid; pop removes and peek preserves the latest item; empty access fails without mutation; storage grows geometrically.
## Complexity Targets
Push amortized O(1); remaining operations O(1); O(n) contiguous space.
