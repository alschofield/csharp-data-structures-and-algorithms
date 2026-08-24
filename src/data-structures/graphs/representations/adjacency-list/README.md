# Adjacency List
## How It Works
Each dynamically added caller-valued node has an outgoing weighted-edge list, favoring sparse graphs.
## Required API
`AdjacencyList<T>`: `Create(bool directed)`; `AddNode(T value)` returns `Node<T>`; `NodeAt(int index)` and `NodeForValue(T value)` look up handles; `AddEdge(Node<T>,Node<T>,long)`, `HasEdge(Node<T>,Node<T>)`, `Neighbors(Node<T>,Action<Node<T>,long>)`, `NodeCount`, and `EdgeCount`; exposes a dynamic index-based `GraphView` adapter.
## Contract
Create an empty directed or undirected graph, then add uniquely valued nodes with caller-supplied values. Each returned node handle is stable, owns an immutable graph-assigned dense index, and only handles owned by this graph are valid edge endpoints. Every edge stores its supplied weight; undirected adds the same weighted edge in both directions; make duplicate policy explicit; deterministic weighted-neighbor iteration visits each out-edge once; self-loops are allowed. Its `GraphView` adapter remains current as nodes and edges are added and maps handles to their indexes.
## Complexity Targets
`AddNode` amortized O(1); test/iterate O(deg(u)); full traversal O(V+E); O(V+E) space.
