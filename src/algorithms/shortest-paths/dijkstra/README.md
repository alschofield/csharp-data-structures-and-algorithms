# Dijkstra
## How It Works
A min-priority queue settles smallest tentative non-negative path costs.
## Required API
`Dijkstra.ShortestPaths(WeightedGraph graph, int source)` returns distances and parents.
## Contract
Reject negative weights and invalid source; use decrease-key or skip stale entries; unreachable vertices have explicit infinity; parents reconstruct shortest paths; support cycles, parallel edges, and loops.
## Complexity Targets
O((V+E) log V) time and O(V) auxiliary space.
