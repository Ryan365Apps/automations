---
description: Process items in inbox/ and file each one to the right destination.
---

Process everything in `inbox/`, but skip `inbox/.processed/`, `inbox/.gitkeep`, and any other dotfiles in `inbox/`.

For each remaining file:
1. Read it and classify:
   - **actionable** → Linear issue (propose team, title, description, priority).
   - **reference** → Confluence page or `notes/`. Propose the destination.
   - **context for an existing item** → Linear comment, Confluence comment, or GitHub comment on an existing PR/issue.
   - **noise** → ask whether to delete.
2. Present the classification and proposed action. **Wait for confirmation** before creating or writing anywhere.
3. After filing, move the source file to `inbox/.processed/YYYY-MM-DD-<original-name>`.
4. At the end, print a one-line summary per item: `<filename> → <destination>`.

Rules:
- Never auto-create tickets, pages, or comments.
- Never delete a file without confirmation.
- If an item is ambiguous, ask rather than guess.
