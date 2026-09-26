# Adjacency List

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Each dynamically added caller-valued node has an outgoing weighted-edge list, favoring sparse graphs.

The representation records directed or undirected weighted relationships and exposes neighbors by dense vertex index.

## Required API

`AdjacencyList<T>`: `Create(bool directed)`; `AddNode(T value)` returns `Node<T>`; `NodeAt(int index)` and `NodeForValue(T value)` look up handles; `AddEdge(Node<T>,Node<T>,long)`, `HasEdge(Node<T>,Node<T>)`, `Neighbors(Node<T>,Action<Node<T>,long>)`, `NodeCount`, and `EdgeCount`; exposes a dynamic index-based `GraphView` adapter.

## Contract

- `T` is unconstrained. Caller-supplied values are unique under the graph's value equality, for both reference and value types.
- `Create` starts empty. `AddNode` returns a stable handle with immutable dense index; only handles owned by this graph are valid edge endpoints. Invalid/foreign handles fail without mutation.
- Each edge retains its `long` weight. Undirected insertion writes the same weighted connection both ways; self-loops are allowed. The implementation documents and consistently applies its duplicate-edge policy.
- `Neighbors` visits each outgoing edge once in deterministic order. The `GraphView` adapter is live and maps handles to indexes.

## Complexity Targets

`AddNode` amortized O(1); test/iterate O(deg(u)); full traversal O(V+E); O(V+E) space.

Target: O(V + E) storage, O(1) amortized vertex addition, and neighbor iteration proportional to degree.

## Verification

Exercise empty directed/undirected creation, unique dynamic values with dense indexes, foreign-handle rejection, weighted edges, deterministic neighbors, live `GraphView`, and amortized node addition.
