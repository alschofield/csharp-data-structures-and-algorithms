# Breadth-First Search
A FIFO frontier completes each distance layer before the next.

## API
`BreadthFirstSearch.Traverse(GraphView graph, int source)` returns index visit order.

## Contract
- `graph` is a non-null `GraphView`; `source` must be in its indexed range or traversal fails before mutation.
- Mark vertices on enqueue and visit each reachable index once. Edge weights are read only as graph data and do not affect traversal order.
- The result order is index-based, including vertices added before traversal. Cycles, self-loops, and disconnected vertices are handled without graph mutation.
- The traversal level of each reached vertex is its minimum hop distance. Queue indexes and level counters must not overflow.

## Complexity
O(V+E) time and O(V) space for a `GraphView` whose weighted-neighbor iteration totals O(E).

## Verification
Exercise a dynamic `GraphView`, index source, levels, ignored weights, cycles, disconnected vertices, and invalid-source rejection.
