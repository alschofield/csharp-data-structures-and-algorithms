# Adjacency Matrix
A dynamically resized N by N grid stores weighted edge cells and makes edge tests one indexed read.

## API
`AdjacencyMatrix<T>`: `Create(bool directed)`; `AddNode(T value)` returns `Node<T>`; `NodeAt(int index)` and `NodeForValue(T value)` look up handles; `AddEdge(Node<T>,Node<T>,long)`, `RemoveEdge(Node<T>,Node<T>)`, `HasEdge(Node<T>,Node<T>)`, `Neighbors(Node<T>,Action<Node<T>,long>)`, `NodeCount`, and `EdgeCount`; exposes a dynamic index-based `GraphView` adapter.

## Contract
- `T` is unconstrained. Caller-supplied values are unique under the graph's value equality, for both reference and value types.
- `Create` starts empty. `AddNode` returns a stable handle with immutable dense index; only handles owned by this graph are valid edge endpoints. Invalid/foreign handles fail without mutation.
- New rows and columns contain no edges. Present cells retain their `long` weights; undirected changes are symmetric with the same weight.
- Duplicate adds and absent removals are no-ops. `Neighbors` scans the full row. Matrix dimensions and index calculations must fail before integer overflow.
- The `GraphView` adapter is live and maps handles to indexes.

## Complexity
`AddNode` O(N^2); add/remove/test O(1); neighbor iteration O(N); full traversal O(N^2); O(N^2) space.

## Verification
Exercise empty directed/undirected creation, unique dynamic values with dense indexes, foreign-handle rejection, symmetric weighted edges, no-op edge changes, row scans, live `GraphView`, and O(N^2) node addition.
