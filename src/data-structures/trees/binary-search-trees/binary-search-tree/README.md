# Binary Search Tree
An unbalanced tree puts smaller values left and larger values right.

## API
`BinarySearchTree<T>`: comparer constructor; `Insert`, `TryFind`, `Contains`, `Remove`, `InOrder`, `Count`, `IsEmpty`.

## Contract
- `T` is unconstrained, so the supplied comparer defines ordering for both reference and value types. Stored values are non-null.
- Equal insertion does not replace the first stored object.
- `Remove` preserves ordering for leaf, one-child, two-child, and root removal.
- `InOrder` is strictly increasing under the comparer and supports early stop without further traversal mutation.
- No integer arithmetic is used to derive ordering or indexes.

## Complexity
Balanced lookup/insert/remove O(log n), worst O(n); traversal O(n); O(n) nodes plus O(height) work space.

## Verification
Exercise duplicates, each removal shape, and in-order traversal.
