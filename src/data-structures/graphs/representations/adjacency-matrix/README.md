# Adjacency Matrix
## How It Works
A V by V grid makes edge tests one indexed read.
## Required API
`AdjacencyMatrix`: constructor `(int,bool)`; `AddEdge`, `RemoveEdge`, `HasEdge`, `Neighbors`, `VertexCount`, `EdgeCount`.
## Contract
Vertices are `[0,V)`; fresh cells clear; undirected changes are symmetric; duplicate adds and absent removals are documented no-ops; neighbors scan a full row.
## Complexity Targets
Add/remove/test O(1); neighbor iteration O(V); full traversal O(V^2); O(V^2) space.
