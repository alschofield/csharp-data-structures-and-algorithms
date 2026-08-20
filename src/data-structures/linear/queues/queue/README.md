# Queue
## How It Works
An array-backed circular buffer keeps wrapped head and tail indexes.
## Required API
`Queue<T>`: constructor; `Enqueue(T)`, `Dequeue()`, `Peek()`, `Count`, `IsEmpty`.
## Contract
Null values are valid; dequeue/peek expose the oldest item; empty access fails cleanly; dequeue never shifts elements.
## Complexity Targets
Enqueue amortized O(1); remaining operations O(1); O(n) contiguous space.
