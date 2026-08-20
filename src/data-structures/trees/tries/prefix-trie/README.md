# Prefix Trie
## How It Works
Character paths share prefixes and end flags distinguish stored keys.
## Required API
`PrefixTrie`: `Insert(string)`, `Contains(string)`, `StartsWith(string)`, `Remove(string)`, `Count`.
## Contract
Duplicate insertion is idempotent; empty string is a valid prefix; removal prunes only dead paths and absent removal changes nothing.
## Complexity Targets
All operations O(m), independent of key count; O(total stored characters) worst-case space.
