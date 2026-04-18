---
description: Digest recent Claude Code conversations across all projects.
---

Summarize recent Claude sessions to recover context.

1. List JSONL files under `~/.claude/projects/` modified in the last 7 days (or the window the user specifies).
2. For each file, extract:
   - The project directory (decoded from the parent folder name).
   - The first user message (the session's topic).
   - The last assistant message or any end-of-turn summary (the outcome).
   - Any unresolved TODOs, errors, or "next steps" language.
3. Group by project directory.
4. Output a digest: each project → bulleted list of sessions, one line each:
   `<time> — <topic> → <outcome or status>`
5. Call out sessions that look unfinished or errored.

Be efficient: stat first, skim the head and tail of each file, don't read the whole transcript unless needed.
