# Doubly Linked List
Previous and next links plus retained endpoints make both ends constant time.

## API
`DoublyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.

## Contract
- `T` is unconstrained; values may be reference or value types.
- `Get` and `Remove` accept indexes in `[0, Count)`; `Insert` also accepts `Count`.
- Every adjacent pair has reciprocal `Previous`/`Next` links, and endpoints remain synchronized.
- Indexed walks start from the nearer endpoint. Removing the last item clears both endpoints.
- Invalid indexed operations fail without mutation.

## Complexity
End operations/metadata O(1); indexed operations O(n), at most n/2 steps; O(n) space.

## Verification
Exercise reciprocal links, both ends, index boundaries, nearer-end traversal, and final-node removal.
