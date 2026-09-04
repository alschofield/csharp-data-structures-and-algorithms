# Data Structures and Algorithms in C#

The `src/` taxonomy mirrors the canonical C curriculum's 26 applicable leaves. Each carries a contract README; `TEST-SPECS.md` provides generated xUnit targets for every leaf. No production C# source is supplied.

`List<T>` is the native dynamic-sequence baseline and is not a separate curriculum exercise. It may be used where a topic needs contiguous backing storage.

## Verification

`dotnet test` becomes meaningful after test files and user-owned production APIs are introduced. Implement each learning target directly: do not substitute BCL collections, search helpers, or sorting helpers except for `List<T>` as the allowed native dynamic-sequence baseline.
