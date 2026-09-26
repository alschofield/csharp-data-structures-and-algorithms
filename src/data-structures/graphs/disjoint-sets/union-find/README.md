# Union-Find

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

A parent forest uses path compression and union by rank or size.

Parent links represent disjoint components; path compression and rank or size metadata keep finds shallow.

## Required API

`UnionFind`: constructor `(int)`; `Find`, `Union`, `Connected`, `SetCount`.

## Contract

- The constructor creates singleton elements at indexes `[0, n)`; negative capacity and out-of-range element indexes fail without state mutation.
- `Find` may mutate parent links through path compression but does not change partition membership or `SetCount`.
- `Union` uses rank or size and decrements `SetCount` only when it joins distinct sets; redundant union changes neither rank/size nor count.
- Representatives are opaque equality tokens, not stable numeric ordering values.

## Complexity Targets

Find/union/connected amortized O(alpha(n)); construction O(n); O(n) space.

Target: amortized O(alpha(n)) find/union and O(n) storage.

## Verification

Exercise path compression, union rank/size, redundant union, and set count.
