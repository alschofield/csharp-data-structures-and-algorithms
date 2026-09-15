# A-Star
A min-priority frontier orders candidates by `g + h` toward a goal.

## API
`AStar.FindPath(GraphView graph, int source, int goal, Func<int,ulong> heuristic)` returns an optional index path.

## Contract
- `graph` and `heuristic` are non-null; `source` and `goal` must be valid graph indexes. Invalid endpoints and negative edge weights are rejected.
- Read indexed neighbors and weights from `GraphView` without mutation. A non-negative `ulong` heuristic is evaluated by vertex index.
- With an admissible heuristic, return an optimal index path. A zero heuristic has Dijkstra-equivalent results.
- Frontier ties are deterministic; an unreachable goal explicitly returns no path. `g + h` and path-cost arithmetic must detect overflow rather than wrap.

## Complexity
Worst O((V+E) log V), O(V) auxiliary space.

## Verification
Exercise a dynamic `GraphView`, admissible weighted index paths, zero-heuristic equivalence, no path, deterministic ties, and invalid-endpoint rejection.
