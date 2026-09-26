# Singly Linked List

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Nodes carry one forward link and the list retains only its head.

Nodes carry links between neighboring values so endpoint updates do not require shifting a contiguous array.

## Required API

`SinglyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.

## Contract

- `T` is unconstrained; null reference values are valid list values.
- `Get` and `Remove` accept indexes in `[0, Count)`; `Insert` also accepts `Count`.
- Invalid access or mutation fails without changing the list.
- The final removal restores a valid empty state; no operation depends on a tail reference.

## Complexity Targets

Front operations/metadata O(1); other operations O(n); O(n) node space.

Target: O(1) endpoint-link operations, O(n) indexed traversal, and O(n) storage.

## Verification

Exercise both ends, index boundaries, and removing the final node.
