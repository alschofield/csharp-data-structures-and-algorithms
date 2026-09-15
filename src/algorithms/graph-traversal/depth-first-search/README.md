# Depth-First Search
A stack or recursion follows a branch fully before backtracking.

## API
`DepthFirstSearch.Traverse(GraphView graph, int source)` returns index visit order.

## Contract
- `graph` is a non-null `GraphView`; `source` must be in its indexed range or traversal fails before mutation.
- Maintain visited state and visit each reachable index once. Edge weights do not affect traversal order.
- The result is index-based, including vertices added before traversal. Cycles, self-loops, and disconnected vertices are handled without graph mutation.
- Either recursion or an explicit stack is valid; indexes and stack bounds must not overflow.

## Complexity
O(V+E) time and O(V) space for a `GraphView` whose weighted-neighbor iteration totals O(E).

## Verification
Exercise a dynamic `GraphView`, index source, branch order, ignored weights, cycles, disconnected vertices, and invalid-source rejection.
