# Binary Search Tree
## How It Works
An unbalanced tree puts smaller values left and larger values right.
## Required API
`BinarySearchTree<T>`: comparer constructor; `Insert`, `TryFind`, `Contains`, `Remove`, `InOrder`, `Count`, `IsEmpty`.
## Contract
Values are non-null; duplicates preserve the first object; remove handles leaf, one-child, two-child, and root cases; in-order is strictly increasing and supports early stop.
## Complexity Targets
Balanced lookup/insert/remove O(log n), worst O(n); traversal O(n); O(n) nodes plus O(height) work space.
