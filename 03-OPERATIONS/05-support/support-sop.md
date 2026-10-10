---
title: Support SOP
type: sop
updated: 2026-10-10
---

# Support

## Channels

Email and the business line. One address for clients (decide between info@ and hello@ — see [[../06-admin/open-decisions]]).

## Response targets

| Severity | Example | First response | Fix or workaround |
|---|---|---|---|
| Down | Phone agent not answering, automation stopped | Within 2 business hours | Same day: switch client to manual fallback first, then fix |
| Wrong | Agent gave wrong info, duplicate records | Same business day | Within 2 business days |
| Request | Change wording, add a field | Within 2 business days | Quoted if out of scope |

## When something breaks

1. Switch to the manual fallback in the client's "how it runs" doc. Client keeps working.
2. Find what broke and when. Check the tool's logs.
3. Fix, test with the original failing case, confirm with the client.
4. One line in the client's `log.md`: what broke, why, what changed.
5. If it could happen to other clients, add a test to the relevant runbook.

## Out of scope

Anything not in the proposal: say so kindly, offer a quote. Never do unpaid scope creep quietly.
