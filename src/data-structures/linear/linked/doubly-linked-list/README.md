# Doubly Linked List
## How It Works
Previous and next links plus retained endpoints make both ends constant time.
## Required API
`DoublyLinkedList<T>`: `PushFront`, `PushBack`, `PopFront`, `PopBack`, `Get`, `Insert`, `Remove`, `Count`, `IsEmpty`.
## Contract
Maintain reciprocal links and synchronized endpoints; indexes are `[0,Count)` and insert accepts Count; walks begin nearer the target; final removal clears both ends.
## Complexity Targets
End operations/metadata O(1); indexed operations O(n), at most n/2 steps; O(n) space.
