# Source

Vendored copy of [humanize-ru](https://github.com/v0lka/skills/tree/main/writing/humanize-ru)
from [v0lka/skills](https://github.com/v0lka/skills).

| Field | Value |
| ----- | ----- |
| Upstream path | `writing/humanize-ru/` |
| Upstream repo HEAD at vendor time | `3c001ff6c9d4ebae4b927b11fb0e80db13fefee9` (2026-07-04) |
| License | MIT — see `LICENSE` (Copyright (c) 2026 Vladimir Kochetkov) |
| Vendor date | 2026-08-06 |

## Role in Thinking Lab

This skill removes AI-generation markers from Russian text while preserving
register. It is the **AI-marker pass** in the Thinking Lab draft pipeline:

```text
RUSSIAN_ANTI_PATTERNS → humanize-ru → HUMANIZER_CORE → HUMANIZER_RULES
```

It does not replace `skills/russian-humanizer` (modes / voice adapters) or
Thinking Lab research orchestration (`skills/thinking-lab-content`).

## Local source of truth

For agents working in this repository, the files under `skills/humanize-ru/`
are the source of truth.

`references/` match upstream catalogs and should stay syncable.

`SKILL.md` may include a short Thinking Lab routing block on top of upstream
procedure. When re-syncing from upstream, preserve that routing block and
refresh the reference files from upstream.
