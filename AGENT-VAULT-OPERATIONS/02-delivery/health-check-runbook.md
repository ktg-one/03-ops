---
title: Digital Health Check runbook
type: runbook
updated: 2026-10-10
source: Good-AI-Business-Plan.docx (Tier 0, Lead Gen Engine, GTM Phase 1)
---

# Digital Health Check runbook

**The offer (business plan, Tier 0):** an AI-powered audit of a business's website and online presence. It's the lead-gen engine: the client sees what's wrong, then picks which of our services to deploy from the report.
**Price:** $149 (business plan, confirmed 2026-10-10). The plan's free promo has **not started**: don't offer it free until Kev launches it. GST treatment not confirmed, so don't quote "incl." or "excl. GST" yet.

## What the client gets (plan)

Packaged as a one-page interactive website:
- An enriched report with clear next actions
- An infographic of the priority areas
- An audio overview
- A video walkthrough

## Two ways it runs

| Mode | Who | Price | Purpose |
|---|---|---|---|
| **Outbound** | Businesses with the weakest web scores, picked by us | Free once the promo starts (not yet) | Opens the conversation (marketing-qualified → sales-qualified lead) |
| **Inbound** | Someone who asks for one | $149 | Paid diagnostic, credited against a build |

## Steps

| # | Step | Output |
|---|---|---|
| 1 | Pick the business (outbound: lowest web scores; inbound: they asked or paid) | Todoist task, label `health-check` |
| 2 | Run the web analyzer on their site and public footprint | Raw findings |
| 3 | Turn the findings into report, infographic, audio and video (NotebookLM or equivalent) | Asset bundle |
| 4 | Check every finding against a source. Cut anything you can't show | Checked report |
| 5 | Package as the one-page site and send the private link | Link sent |
| 6 | Follow up in 2 business days: "Which of these would you like fixed first?" Map their answer to a service tier | Next step agreed |

## Rules

- Outbound reports go to the business only, privately. Never publish a report about a business that didn't ask for it.
- No claim without evidence; nothing invented to make the report scarier.
- Stay inside what the plan sells: map every recommendation to a tier (website bot, knowledge bot, automation, voice) or to "you can do this yourself".

## Done when

- [ ] Link sent
- [ ] Follow-up made
- [ ] Their answer recorded in Todoist (next step, or not now)
