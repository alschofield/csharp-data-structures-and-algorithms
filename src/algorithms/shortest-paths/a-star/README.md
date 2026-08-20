# A-Star
## How It Works
A min-priority frontier orders candidates by `g + h` toward a goal.
## Required API
`AStar.FindPath(WeightedGraph graph, int source, int goal, Func<int,ulong> heuristic)` returns an optional vertex path.
## Contract
Require non-negative weights; admissible heuristics yield optimal paths; zero heuristic exactly degenerates to Dijkstra; ties are deterministic; unreachable goals explicitly report no path.
## Complexity Targets
Worst O((V+E) log V), O(V) auxiliary space.
