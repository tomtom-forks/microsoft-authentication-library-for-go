# CLAUDE.md — microsoft-authentication-library-for-go (TomTom fork)

Go module: `github.com/AzureAD/microsoft-authentication-library-for-go`

## Project layout

```
apps/
  public/          # PublicClientApplication (interactive / device-code / auth-code flows)
  confidential/    # ConfidentialClientApplication (client-credentials, OBO, user_fic)
  managedidentity/ # Managed Identity credential support
  internal/
    base/          # Shared Client used by both public and confidential
    oauth/         # Token-endpoint I/O and authority resolution
    base/storage/  # In-memory token cache (Manager + PartitionedManager)
    cache/         # cache.ExportReplace interface consumed by callers
```

## ReminAIscence

This project has an active ReminAIscence codebase map and memory store.

### Codebase map

Built from commit `11b8221` (Go, scip-go):

| Metric | Value |
|--------|-------|
| Nodes | 8 193 |
| Edges | 3 471 |
| Files indexed | 99 |
| Functions embedded | 838 / 838 (100 %) |

Refresh after significant refactors:

```
/reminaiscence:codebase-map rebuild
```

### Useful queries

```
# Find everything that depends on a module (up to 5 hops)
/reminaiscence:codebase-map blast-radius <module-name>

# Find direct callers of a function
/reminaiscence:codebase-map callers <function-name>

# Semantic search — find functions related to a concept, then their blast radius
/reminaiscence:codebase-map impact <natural-language description>

# Check map freshness
/reminaiscence:codebase-map status
```

### Memory

```
# Search stored memories for this project
/reminaiscence:memory search <query>

# Trigger manual memory consolidation after a heavy session
/reminaiscence:dream
```
