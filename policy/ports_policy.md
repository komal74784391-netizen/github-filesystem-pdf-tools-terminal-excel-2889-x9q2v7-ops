# Port tree policy (platform-owned, v3)

The `ports/` tree holds starter stubs for every approved item of the sprint backlog.
Platform owns this file; application teams do not edit it.

## Layout

- One directory per implementation language, using the language display name exactly:
  `Go`, `Rust`, `Python`.
- One stub per approved backlog item, inside its language directory.
- Stub file name: `<slug>.<ext>`, where `<slug>` is the backlog `slug` copied verbatim
  (lower-case kebab-case) and `<ext>` comes from the language table below.

## Language table

| Language | Extension |
|----------|-----------|
| Go       | .go       |
| Rust     | .rs       |
| Python   | .py       |

The extension is a short code, not the language name. Do not add, rename or re-case
directories.

## Stub body

The first line of every stub must be:

    port stub: <slug>

Example: `ports/Rust/ring-cache-core.rs` starts with `port stub: ring-cache-core`.

## Scope

Only backlog items whose `status` is `approved` get a stub. Items with any other status
(`deferred`, `on-hold`, ...) must not appear in the tree and must not appear in the
published manifest.
