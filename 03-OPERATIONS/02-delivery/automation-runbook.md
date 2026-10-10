---
title: Automation runbook
type: runbook
updated: 2026-10-10
---

# Workflow automation runbook

For jobs like chasing quotes, moving details between systems, invoice/receipt handling, follow-ups.

## 1. Map it (before any build)

Write the job as it happens today, step by step: **trigger → steps → who → which tool → output.** Mark the step where it usually breaks.

Then the automated version: what triggers it, what it does, where a person approves, what happens when it fails.

## 2. Pick the simplest tool that works

Use the order: the client's existing tools' built-in features → no-code automation (e.g. n8n, Zapier, Make) → custom code. Only go further down the list when the step above can't do the job.

## 3. Build

- Build one path end to end before adding branches.
- Every automation has: a failure alert (to the client owner and us), a log of what it did, and a manual override.
- Use the client's own accounts where possible, so they own it.

## 4. Test (all must pass)

- [ ] Normal case
- [ ] Bad / missing data (empty field, wrong format)
- [ ] Same item twice (no duplicates created)
- [ ] Connected tool is down (it alerts, doesn't silently drop)
- [ ] Client runs it themselves once and approves

## 5. Go-live

Run alongside the old way for one week, then switch. Move to [[handover-and-adoption]].
