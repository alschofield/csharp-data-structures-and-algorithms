# Graph View
## How It Works
An abstraction exposes a dynamically growing graph's indexed vertices and outgoing weighted neighbors without exposing its storage.
## Required API
`GraphView`: `int VertexCount { get; }` and `Neighbors(int vertex, Action<int,long> consumer)`; each callback receives `(neighborIndex, weight)`.
## Contract
Vertices are stable dense indexes in `[0,VertexCount)`; reject an index outside that range before iteration. Invoke the consumer once for every outgoing edge with its stored weight and destination index, and document deterministic order when available. Adapters over adjacency-list, adjacency-matrix, and imported graph formats reflect nodes added after adapter creation without copying storage. A concrete graph may expose caller-facing node handles, but its adapter maps those handles to indexes rather than exposing them here.
## Complexity Targets
`VertexCount` is O(1); neighbor iteration is proportional to the backing representation's outgoing-neighbor scan.
