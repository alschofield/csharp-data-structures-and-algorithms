# Singly Linked List
Nodes carry one forward link and the list retains only its head.

## API
`SinglyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.

## Contract
- `T` is unconstrained; null reference values are valid list values.
- `Get` and `Remove` accept indexes in `[0, Count)`; `Insert` also accepts `Count`.
- Invalid access or mutation fails without changing the list.
- The final removal restores a valid empty state; no operation depends on a tail reference.

## Complexity
Front operations/metadata O(1); other operations O(n); O(n) node space.

## Verification
Exercise both ends, index boundaries, and removing the final node.
