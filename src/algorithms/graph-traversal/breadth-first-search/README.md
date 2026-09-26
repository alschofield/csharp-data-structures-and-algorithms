# Breadth-First Search

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

A FIFO frontier completes each distance layer before the next.

A FIFO frontier visits each discovered vertex layer by layer while a visited set prevents repeated work.

## Required API

`BreadthFirstSearch.Traverse(GraphView graph, int source)` returns index visit order.

## Contract

- `graph` is a non-null `GraphView`; `source` must be in its indexed range or traversal fails before mutation.
- Mark vertices on enqueue and visit each reachable index once. Edge weights are read only as graph data and do not affect traversal order.
- The result order is index-based, including vertices added before traversal. Cycles, self-loops, and disconnected vertices are handled without graph mutation.
- The traversal level of each reached vertex is its minimum hop distance. Queue indexes and level counters must not overflow.

## Complexity Targets

O(V+E) time and O(V) space for a `GraphView` whose weighted-neighbor iteration totals O(E).

Target: O(V + E) time and O(V) auxiliary space.

## Verification

Exercise a dynamic `GraphView`, index source, levels, ignored weights, cycles, disconnected vertices, and invalid-source rejection.
