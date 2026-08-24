# Breadth-First Search
## How It Works
A FIFO frontier completes each distance layer before the next.
## Required API
`BreadthFirstSearch.Traverse(GraphView graph, int source)` returns index visit order.
## Contract
Mark on enqueue; visit each reachable vertex once; ignore edge weights; reject a source index outside the view; support vertices added before traversal, cycles, self-loops, and disconnected graphs without graph mutation; distances are minimum hops.
## Complexity Targets
O(V+E) time and O(V) space for a `GraphView` whose weighted-neighbor iteration totals O(E).
