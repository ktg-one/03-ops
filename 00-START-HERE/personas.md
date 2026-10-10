---
title: Role personas (CMO, CFO, COO)
type: how-to
created: 2026-10-10
---

# Role personas

Three Claude Code "seats" live in `.claude/agents/`. Each one reads this vault first and knows which installed skills fit its job.

| Seat | Ask it about | Launch |
|---|---|---|
| CMO | Copy, social, launch, outreach, first customers | `claude --agent cmo` |
| CFO | Prices, margins, cash, invoices, GST, month end | `claude --agent cfo` |
| COO | What to do today, delivery, support, Todoist | `claude --agent coo` |

## How to use them

1. Open a terminal in this folder (the one with `.claude/` in it).
2. Run the launch command for the seat you want. The whole session is that persona.
3. Or, inside a normal `claude` session, just say "ask the cfo…" and it hands that question to the CFO.

## Rules every seat follows

- Reads the vault before advising and names the file a fact came from.
- Drafts only. Kev approves anything that leaves the building.
- No invented numbers, testimonials or client names.
- Says when a skill isn't installed, and when you need an accountant or lawyer.

## Changing a persona

Edit the `.md` file in `.claude/agents/`. The top block (name, description) is how Claude picks it; the rest is its brief.
