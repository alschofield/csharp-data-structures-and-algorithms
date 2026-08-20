# Breadth-First Search
## How It Works
A FIFO frontier completes each distance layer before the next.
## Required API
`BreadthFirstSearch.Traverse(AdjacencyList graph, int source)` returns visit order.
## Contract
Mark on enqueue; visit each reachable vertex once; reject invalid source; support cycles, self-loops, and disconnected graphs without graph mutation; distances are minimum hops.
## Complexity Targets
O(V+E) time and O(V) space with an adjacency list.
