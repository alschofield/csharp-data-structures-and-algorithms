# Generated xUnit Test Specifications

Create test source only under `tests/`; expected initial compile failures are correct because production APIs are intentionally absent.

| Topic | Required test behavior |
| --- | --- |
| dynamic-array | bounds, null values, replacement/removal, geometric growth |
| stack | LIFO, empty access, null values, growth |
| queue | FIFO, wraparound, empty access, growth |
| singly-linked-list | end cases, indexes, final-node removal |
| doubly-linked-list | reciprocal links, both ends, nearer-end indexes |
| separate-chaining | collisions, replacement, fixed ten buckets |
| resizable-separate-chaining | collisions, 0.75 resize, rehash, no shrink |
| binary-search-tree | duplicates, every removal shape, in-order |
| binary-heap | heap ordering, empty access, equal priorities |
| prefix-trie | duplicate keys, prefixes, pruning removal |
| adjacency-list | directedness, invalid vertices, deterministic neighbors |
| adjacency-matrix | symmetric updates, no-op edge changes, row scan |
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
| breadth-first-search | levels, cycles, disconnected vertices, invalid source |
| depth-first-search | branch order, cycles, disconnected vertices, invalid source |
| dijkstra | shortest paths, infinity, stale entries, negative rejection |
| a-star | admissible path, zero heuristic equivalence, no path, tie order |
