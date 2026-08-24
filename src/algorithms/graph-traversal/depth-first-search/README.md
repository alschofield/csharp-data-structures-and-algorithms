# Depth-First Search
## How It Works
A stack or recursion follows a branch fully before backtracking.
## Required API
`DepthFirstSearch.Traverse(GraphView graph, int source)` returns index visit order.
## Contract
Use visited state; visit each reachable vertex once; ignore edge weights; reject a source index outside the view; handle vertices added before traversal, cycles, self-loops, and disconnected graphs without mutation; understand recursive and explicit-stack forms.
## Complexity Targets
O(V+E) time and O(V) space for a `GraphView` whose weighted-neighbor iteration totals O(E).
