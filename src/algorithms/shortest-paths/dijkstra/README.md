# Dijkstra
A min-priority queue settles smallest tentative non-negative path costs.

## API
`Dijkstra.ShortestPaths(GraphView graph, int source)` returns distances and parents keyed by vertex index.

## Contract
- `graph` is non-null and `source` must be in range; invalid source and any negative edge weight are rejected before a successful result.
- Read indexed neighbors and `long` weights from `GraphView` without graph mutation. Use decrease-key or discard stale priority-queue entries.
- Distances and parents are keyed by vertex index. Unreachable vertices have explicit infinity; parent indexes reconstruct each reachable shortest path.
- Support vertices added before the run, cycles, parallel edges, and self-loops. Path-cost addition must detect integer overflow rather than wrap.

## Complexity
O((V+E) log V) time and O(V) auxiliary space.

## Verification
Exercise a dynamic `GraphView`, weighted index-keyed paths, infinity, stale entries, negative-weight rejection, and invalid-source rejection.
