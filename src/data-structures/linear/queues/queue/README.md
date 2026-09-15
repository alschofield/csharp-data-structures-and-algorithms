# Queue
An array-backed circular buffer keeps wrapped head and tail indexes.

## API
`Queue<T>`: constructor; `Enqueue(T)`, `Dequeue()`, `Peek()`, `Count`, `IsEmpty`.

## Contract
- `T` is unconstrained: reference-type, value-type, and nullable reference values are valid entries.
- `Dequeue` returns and removes the oldest item; `Peek` returns it without mutation.
- Empty `Dequeue` and `Peek` fail without changing queue state.
- Head and tail wrap correctly through the circular buffer; `Dequeue` never shifts remaining entries.

## Complexity
Enqueue amortized O(1); remaining operations O(1); O(n) contiguous space.

## Verification
Exercise FIFO order, empty access, null entries, wraparound, and growth.
