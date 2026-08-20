# Adjacency List
## How It Works
Each vertex has an outgoing-edge list, favoring sparse graphs.
## Required API
`AdjacencyList`: constructor `(int,bool)`; `AddEdge`, `HasEdge`, `Neighbors`, `VertexCount`, `EdgeCount`.
## Contract
Vertices are `[0,V)`; reject invalid values; undirected adds both directions; duplicate policy is explicit; deterministic iteration visits each out-edge once; self-loops allowed.
## Complexity Targets
Add amortized O(1); test/iterate O(deg(u)); full traversal O(V+E); O(V+E) space.
