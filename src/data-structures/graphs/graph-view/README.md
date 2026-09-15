# Graph View
An abstraction exposes a dynamically growing graph's indexed vertices and outgoing weighted neighbors without exposing its storage.

## API
`GraphView`: `int VertexCount { get; }` and `Neighbors(int vertex, Action<int,long> consumer)`; each callback receives `(neighborIndex, weight)`.

## Contract
- `VertexCount` exposes stable dense indexes in `[0, VertexCount)`. An invalid vertex index fails before callbacks begin.
- `Neighbors` invokes the non-null consumer once per outgoing edge with the stored `long` weight and destination index. It does not mutate the graph.
- Adapters over adjacency-list, adjacency-matrix, and imported graph formats remain live after adapter creation and do not copy storage.
- Caller-facing node handles stay outside this API; an adapter maps them to indexes. Neighbor order is deterministic when the backing representation provides one.

## Complexity
`VertexCount` is O(1); neighbor iteration is proportional to the backing representation's outgoing-neighbor scan.

## Verification
Exercise dynamic vertex counts, invalid-index rejection, weighted neighbor indexes, and live adapters.
