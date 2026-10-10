---
title: Voice agent runbook
type: runbook
updated: 2026-10-10
---

# Voice agent (phone answering) runbook

**Offer (business plan):** Voice agent integration on Trillet: an emotive voice agent that answers your phone, WhatsApp and website with a custom personality. **$1,000 setup + $149/month** (plan price, Kev to confirm). The plan's main add-on to sell across all tiers.
**Our own demo:** the business line on goodai.au, (08) 7741 4191.

## 1. Scope (before build)

- Hours it answers (after-hours only, overflow, or all calls)
- What it must capture: name, number, reason, urgency, address/job details
- What it must never do: quote prices, book without checking, give advice outside the script
- Where details go: email, SMS, CRM, calendar
- When it hands to a human, and how (transfer number, callback promise)
- Call recording: check the actual setting on the Trillet agent and record it. Don't guess a default

## 2. Build

1. Create the agent on the voice platform. Name, voice and greeting agreed with the client.
2. Write the knowledge doc: business hours, services, service area, FAQs. Client signs off the facts.
3. Set the capture fields and where they're sent.
4. Set the handover rule and fallback ("I'll get someone to call you back by [time]").
5. Connect a test number first, not their real line.

## 3. Consent gate (all green before deploy)

| Gate | Green when |
|---|---|
| Disclosure | Greeting says it's an AI assistant and the call may be recorded: *"This call is being answered by [Client]'s AI assistant and may be recorded."* |
| Recording setting | Observed on the agent and written down |
| Privacy | Voice-caller section of the client's privacy policy reviewed by a lawyer before the first client go-live |
| Escalation number | Client-supplied, reachable |
| Knowledge base | Client-supplied facts only |

## 4. Test (all must pass before go-live; 10+ calls)

- [ ] Normal enquiry: details captured and delivered correctly
- [ ] Caller asks something not in the knowledge doc: agent says it'll pass it on, doesn't invent
- [ ] Caller asks for a human: handover works
- [ ] Caller hangs up mid-call: partial details still delivered
- [ ] Poor line / background noise: agent recovers or hands over
- [ ] Perth suburb names pronounced right (Joondalup, Innaloo, etc.)
- [ ] Response gaps under ~2 seconds
- [ ] Kev sign-off call
- [ ] Client makes 3 test calls themselves and approves

## 5. Go-live

1. Forward their real number (client usually does this with their phone provider; we send them the steps).
2. Watch every call for the first 3 days. Fix anything wrong the same day.
3. Weekly call-log review after that: missed calls, failed intents, anything made up.
4. Move to [[handover-and-adoption]].
