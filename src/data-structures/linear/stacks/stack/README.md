# Stack
An array-backed LIFO keeps its top at the last used index.

## API
`Stack<T>`: constructor; `Push(T)`, `Pop()`, `Peek()`, `Count`, `IsEmpty`.

## Contract
- `T` is unconstrained: reference-type, value-type, and nullable reference values are valid entries.
- `Push` adds the newest item; `Pop` returns and removes it; `Peek` returns it without mutation.
- `Pop` and `Peek` on an empty stack fail without changing `Count` or storage state.
- Backing storage grows geometrically. A failed growth allocation preserves the stack.

## Complexity
Push amortized O(1); remaining operations O(1); O(n) contiguous space.

## Verification
Exercise LIFO order, empty `Pop`/`Peek`, null entries, and growth.
