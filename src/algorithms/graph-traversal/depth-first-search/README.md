# Depth-First Search
## How It Works
A stack or recursion follows a branch fully before backtracking.
## Required API
`DepthFirstSearch.Traverse(AdjacencyList graph, int source)` returns visit order.
## Contract
Use visited state; visit each reachable vertex once; reject invalid source; handle cycles, self-loops, and disconnected graphs without mutation; understand recursive and explicit-stack forms.
## Complexity Targets
O(V+E) time and O(V) space with an adjacency list.
