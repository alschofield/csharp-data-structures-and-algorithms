# Dijkstra
## How It Works
A min-priority queue settles smallest tentative non-negative path costs.
## Required API
`Dijkstra.ShortestPaths(GraphView graph, int source)` returns distances and parents keyed by vertex index.
## Contract
Read edge weights and neighbor indexes from `GraphView`; reject negative weights and a source index outside the view; use decrease-key or skip stale entries; unreachable vertices have explicit infinity; parent indexes reconstruct shortest paths; support vertices added before traversal, cycles, parallel edges, and loops.
## Complexity Targets
O((V+E) log V) time and O(V) auxiliary space.
