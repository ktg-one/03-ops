---
title: Voice agent runbook
type: runbook
updated: 2026-10-10
---

# Voice agent (phone answering) runbook

> Open decision: which voice platform is live (Trillet per launch notes, ElevenLabs per the privacy page and studio code). Fill in [[../06-admin/open-decisions]] before the first client build.

## 1. Scope (before build)

- Hours it answers (after-hours only, overflow, or all calls)
- What it must capture: name, number, reason, urgency, address/job details
- What it must never do: quote prices, book without checking, give advice outside the script
- Where details go: email, SMS, CRM, calendar
- When it hands to a human, and how (transfer number, callback promise)
- Call recording: on or off, and how callers are told (confirm what's required with a qualified adviser)

## 2. Build

1. Create the agent on the voice platform. Name, voice and greeting agreed with the client.
2. Write the knowledge doc: business hours, services, service area, FAQs. Client signs off the facts.
3. Set the capture fields and where they're sent.
4. Set the handover rule and fallback ("I'll get someone to call you back by [time]").
5. Connect a test number first, not their real line.

## 3. Test (all must pass before go-live)

- [ ] Normal enquiry: details captured and delivered correctly
- [ ] Caller asks something not in the knowledge doc: agent says it'll pass it on, doesn't invent
- [ ] Caller asks for a human: handover works
- [ ] Caller hangs up mid-call: partial details still delivered
- [ ] Poor line / background noise: agent recovers or hands over
- [ ] Client makes 3 test calls themselves and approves

## 4. Go-live

1. Forward their real number (client usually does this with their phone provider; we send them the steps).
2. Watch every call for the first 3 days. Fix anything wrong the same day.
3. Move to [[handover-and-adoption]].
