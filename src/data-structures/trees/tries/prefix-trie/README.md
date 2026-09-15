# Prefix Trie
Character paths share prefixes and end flags distinguish stored keys.

## API
`PrefixTrie`: `Insert(string)`, `Contains(string)`, `StartsWith(string)`, `Remove(string)`, `Count`.

## Contract
- Keys are strings; null-key behavior is not an alternate API and must fail rather than be treated as a key.
- Duplicate insertion is idempotent and does not increment `Count`.
- The empty string is a valid prefix.
- Removing an existing key mutates only the nodes no longer needed by another key or prefix. Removing an absent key changes nothing.

## Complexity
All operations O(m), independent of key count; O(total stored characters) worst-case space.

## Verification
Exercise duplicate keys, prefixes, and removal pruning.
