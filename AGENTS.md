# Learning Repo Source Ownership

The user writes all production C# by hand.

- Production `.cs` files are user-owned. Do not create, delete, or modify them unless the user explicitly requests that exact source edit.
- This includes blank scaffolds, declarations, stubs, and completed implementations.
- Tests under `tests/`, documentation, and build tooling are agent-editable.
- Review production source read-only; report findings and verify after the user changes it.
