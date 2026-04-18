# Automations Hub

Central hub for managing work: capture inputs, produce outputs, run agents.

## Purpose
- Capture raw inputs in `inbox/`; produce durable outputs in `notes/`, Linear, or Confluence.
- Route work to the right system: Linear (tasks), Confluence (reference docs), GitHub (code), `notes/` (personal).
- Reuse context across sessions by reading prior Claude conversations in `~/.claude/projects/`.

## Integrations (via MCP)
- **Linear** — issues, projects, cycles, documents, comments.
- **Atlassian** — Jira issues, Confluence pages/comments.
- **GitHub** — PRs, issues, code search. Repo scope: `ryan365apps/automations`.
- **Microsoft Learn** — docs search (not M365 productivity; that MCP is TBD).
- Other MCPs appear in sessions (PostHog, Gamma, Vercel, HubSpot, Google Drive, tldraw) — use when relevant.

## Layout
- `inbox/` — drop raw thoughts, pasted text, emails. Processed by `/inbox`.
- `inbox/.processed/` — filed items are moved here with a date prefix.
- `notes/` — durable notes, briefs, meeting summaries.
- `.claude/commands/` — slash-commands for recurring workflows.

## Conventions
- **Confirm before writing to external systems.** Creating Linear issues, Confluence pages, or GitHub comments always requires explicit confirmation.
- **Read prior sessions first.** Before asking the user for context, check `~/.claude/projects/` for relevant past conversations.
- **File, don't pile.** Every `inbox/` item should land somewhere definite; nothing stays in the inbox.
- **Cite sources.** When producing briefs or summaries, link the Linear/Confluence/GitHub items you drew from.

## Commands
- `/triage` — open Linear work: what needs attention today.
- `/inbox` — process and file everything in `inbox/`.
- `/brief <topic>` — build a context pack from Linear + Confluence + GitHub.
- `/sessions` — digest recent Claude conversations across projects.
