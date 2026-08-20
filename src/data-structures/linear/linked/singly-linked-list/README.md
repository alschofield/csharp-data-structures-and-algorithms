# Singly Linked List
## How It Works
Nodes carry one forward link and the list retains only its head.
## Required API
`SinglyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.
## Contract
Null values are valid; indexes are `[0,Count)` and insert accepts Count; failures preserve state; final removal restores empty state.
## Complexity Targets
Front operations/metadata O(1); other operations O(n); O(n) node space.
