---
description: Morning briefing — Linear pulse + my triage + unfinished Claude sessions.
---

Assemble today's briefing.

Today's date: read from the environment (current system date in YYYY-MM-DD).

1. Do the `/pulse` work: Linear activity across all projects in the last 24 hours.
2. Do the `/triage` work: my open, assigned issues and what needs attention today.
3. Do the `/sessions` work: unfinished threads from Claude conversations in the last 3 days (skip if `~/.claude/projects/` is unavailable — e.g. in CI).
4. Assemble a single markdown document with sections:
   - `## What moved` — from pulse.
   - `## What's on me` — from triage.
   - `## Unfinished from yesterday` — from sessions (omit the section entirely if unavailable).
   - `## Recommended focus` — 3 bullets, the things I should actually do today.
5. Write the document to `notes/daily/<YYYY-MM-DD>.md`, overwriting if it exists.
6. Print the path at the end. Do not post to Linear, Confluence, or GitHub — this briefing stays local/in-repo.

If running non-interactively (e.g. GitHub Actions), do not prompt for confirmation; just produce the file.
