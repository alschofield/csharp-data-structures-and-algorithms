# Adjacency Matrix
## How It Works
A dynamically resized N by N grid stores weighted edge cells and makes edge tests one indexed read.
## Required API
`AdjacencyMatrix<T>`: `Create(bool directed)`; `AddNode(T value)` returns `Node<T>`; `NodeAt(int index)` and `NodeForValue(T value)` look up handles; `AddEdge(Node<T>,Node<T>,long)`, `RemoveEdge(Node<T>,Node<T>)`, `HasEdge(Node<T>,Node<T>)`, `Neighbors(Node<T>,Action<Node<T>,long>)`, `NodeCount`, and `EdgeCount`; exposes a dynamic index-based `GraphView` adapter.
## Contract
Create an empty directed or undirected graph, then add uniquely valued nodes with caller-supplied values. Each returned node handle is stable, owns an immutable graph-assigned dense index, and only handles owned by this graph are valid edge endpoints. New rows and columns contain no edges; every present cell stores its edge weight; undirected updates are symmetric with the same weight; duplicate adds and absent removals are documented no-ops; weighted neighbors scan the full row. Its `GraphView` adapter remains current as nodes and edges are added and maps handles to their indexes.
## Complexity Targets
`AddNode` O(N^2); add/remove/test O(1); neighbor iteration O(N); full traversal O(N^2); O(N^2) space.
