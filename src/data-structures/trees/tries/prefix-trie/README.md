# Prefix Trie

## Implementation Status

Target scaffold. Production behavior is not claimed until the learner-owned implementation and its verification are complete.

## How It Works

Character paths share prefixes and end flags distinguish stored keys.

Each edge represents part of a key, so shared prefixes share storage and prefix lookup follows a path.

## Required API

`PrefixTrie`: `Insert(string)`, `Contains(string)`, `StartsWith(string)`, `Remove(string)`, `Count`.

## Contract

- Keys are strings; null-key behavior is not an alternate API and must fail rather than be treated as a key.
- Duplicate insertion is idempotent and does not increment `Count`.
- The empty string is a valid prefix.
- Removing an existing key mutates only the nodes no longer needed by another key or prefix. Removing an absent key changes nothing.

## Complexity Targets

All operations O(m), independent of key count; O(total stored characters) worst-case space.

Target: O(m) lookup/update by key length m and O(total stored key characters) storage.

## Verification

Exercise duplicate keys, prefixes, and removal pruning.
