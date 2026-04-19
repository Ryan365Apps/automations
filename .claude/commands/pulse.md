---
description: Surface Linear activity across all projects in a recent time window.
argument-hint: [hours] (default 24)
---

Summarize recent Linear activity across the entire workspace — **all teams, all projects**.

Window: last **$ARGUMENTS** hours. If no argument, use **24**.

1. Query Linear for issues with `updatedAt` within the window.
2. Group by project (fall back to team for issues with no project).
3. For each issue show a single line: `<identifier> <title> — <status>, P<priority>, updated by <user>, <what changed>`.
   - "what changed" = status transition, new comments, assignee change, or "created"/"closed" when applicable.
4. Add three short callout sections at the top:
   - **New** — issues created in the window.
   - **Closed** — issues moved to Done/Cancelled in the window.
   - **Blocked** — issues newly marked blocked or with blocker labels.
5. Keep it dense. One line per issue. No narrative.

**Fallback:** if the Linear MCP is unavailable (e.g. CI without auth wired), do not fail. Emit a single line `Linear MCP unavailable — no pulse data this run.` and return. `/daily` relies on this so the briefing still renders in non-interactive runs.
