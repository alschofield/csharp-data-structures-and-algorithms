# A-Star
## How It Works
A min-priority frontier orders candidates by `g + h` toward a goal.
## Required API
`AStar.FindPath(GraphView graph, int source, int goal, Func<int,ulong> heuristic)` returns an optional index path.
## Contract
Read edge weights and neighbor indexes from `GraphView`; require non-negative weights and source and goal indexes inside the view; admissible heuristics yield optimal paths; zero heuristic exactly degenerates to Dijkstra; ties are deterministic; unreachable goals explicitly report no path.
## Complexity Targets
Worst O((V+E) log V), O(V) auxiliary space.
