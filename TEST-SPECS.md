# Generated xUnit Test Specifications

Create test source only under `tests/`; expected initial compile failures are correct because production APIs are intentionally absent.

| Topic | Required test behavior |
| --- | --- |
| dynamic-array | bounds, null values, replacement/removal, geometric growth |
| stack | LIFO, empty access, null values, growth |
| queue | FIFO, wraparound, empty access, growth |
| singly-linked-list | end cases, indexes, final-node removal |
| doubly-linked-list | reciprocal links, both ends, nearer-end indexes |
| separate-chaining | collisions, replacement, explicit nonzero initial capacity, fixed-capacity and resizing set policies, capacity getter, 0.75 resize and rehash, no automatic shrink |
| binary-search-tree | duplicates, every removal shape, in-order |
| binary-heap | heap ordering, empty access, equal priorities |
| prefix-trie | duplicate keys, prefixes, pruning removal |
| graph-view | dynamic vertex count, invalid index rejection, weighted neighbor-index delivery, live adjacency-list/matrix/imported-graph adapters |
| adjacency-list | empty directed/undirected creation, unique dynamic caller-valued nodes with stable dense indexes, handle-based weighted edges, foreign-handle rejection, deterministic neighbors, live index-based GraphView adapter, amortized O(1) node addition |
| adjacency-matrix | empty directed/undirected creation, unique dynamic caller-valued nodes with stable dense indexes, handle-based symmetric weighted edges, foreign-handle rejection, no-op edge changes, weighted row scan, live index-based GraphView adapter, O(N^2) node addition |
| union-find | compression, rank, redundant union, set count |
| linear-search | unsorted input, first duplicate, absent/empty input |
| binary-search | boundaries, duplicates, absent/empty sorted input |
| bubble-sort | stable order and early exit |
| selection-sort | sorted result and at-most-n-minus-one swaps |
| insertion-sort | stable order and nearly sorted input |
| merge-sort | stable merge and uneven runs |
| quick-sort | sorted/reverse/equal-heavy inputs and pivot defense |
| heap-sort | bottom-up heapify and unstable equal values |
| counting-sort | bounded keys, stability, invalid key preservation |
| radix-sort | stable LSD passes and equal values |
| breadth-first-search | dynamic GraphView and index source, levels, ignored weights, cycles, disconnected vertices, invalid source rejection |
| depth-first-search | dynamic GraphView and index source, branch order, ignored weights, cycles, disconnected vertices, invalid source rejection |
| dijkstra | dynamic GraphView and index source, weighted shortest paths keyed by index, infinity, stale entries, negative rejection, invalid source rejection |
| a-star | dynamic GraphView and index endpoints, weighted admissible index path, zero heuristic equivalence, no path, tie order, invalid endpoint rejection |
