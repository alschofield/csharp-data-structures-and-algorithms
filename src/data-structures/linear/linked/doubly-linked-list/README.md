# Doubly Linked List

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Previous and next links plus retained endpoints make both ends constant time.

Nodes carry links between neighboring values so endpoint updates do not require shifting a contiguous array.

## Required API

`DoublyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.

## Contract

- `T` is unconstrained; values may be reference or value types.
- `Get` and `Remove` accept indexes in `[0, Count)`; `Insert` also accepts `Count`.
- Every adjacent pair has reciprocal `Previous`/`Next` links, and endpoints remain synchronized.
- Indexed walks start from the nearer endpoint. Removing the last item clears both endpoints.
- Invalid indexed operations fail without mutation.

## Complexity Targets

End operations/metadata O(1); indexed operations O(n), at most n/2 steps; O(n) space.

Target: O(1) endpoint-link operations, O(n) indexed traversal, and O(n) storage.

## Verification

Exercise reciprocal links, both ends, index boundaries, nearer-end traversal, and final-node removal.
