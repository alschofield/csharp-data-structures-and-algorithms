# Binary Search Tree

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

An unbalanced tree puts smaller values left and larger values right.

Ordered comparisons select the left or right subtree and in-order traversal visits values in sorted order.

## Required API

`BinarySearchTree<T>`: comparer constructor; `Insert`, `TryFind`, `Contains`, `Remove`, `InOrder`, `Count`, `IsEmpty`.

## Contract

- `T` is unconstrained, so the supplied comparer defines ordering for both reference and value types. Stored values are non-null.
- Equal insertion does not replace the first stored object.
- `Remove` preserves ordering for leaf, one-child, two-child, and root removal.
- `InOrder` is strictly increasing under the comparer and supports early stop without further traversal mutation.
- No integer arithmetic is used to derive ordering or indexes.

## Complexity Targets

Balanced lookup/insert/remove O(log n), worst O(n); traversal O(n); O(n) nodes plus O(height) work space.

Target: O(log n) time and O(1) auxiliary space.

## Verification

Exercise duplicates, each removal shape, and in-order traversal.
