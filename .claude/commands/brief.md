---
description: Assemble a context brief on a topic from Linear, Confluence, and GitHub.
argument-hint: <topic>
---

Build a context brief on: **$ARGUMENTS**

Run these searches in parallel:
1. Linear — issues, projects, and documents matching the topic.
2. Confluence — pages matching the topic (CQL search).
3. GitHub — PRs and issues in `ryan365apps/automations` matching the topic.
4. Prior Claude sessions — skim `~/.claude/projects/` for related conversations.

Produce a markdown brief with:
- **Summary** — 3–5 bullets of what the topic is and current state.
- **Open threads** — what's unresolved, what's blocked, what's in flight.
- **Sources** — linked list of every Linear/Confluence/GitHub item referenced.
- **Unknowns** — questions the brief can't answer.

Save to `notes/briefs/<kebab-case-topic>.md` and print the path.
