---
title: Website bot and knowledge bot runbook
type: runbook
updated: 2026-10-10
source: Good-AI-Business-Plan.docx (Tier 1, Tier 2)
---

# Website bot (Tier 1) and knowledge bot (Tier 2) runbook

| | Tier 1: Website bot | Tier 2: Company knowledge bot |
|---|---|---|
| What (plan) | Local semantic chatbot for the website, trained on the client's own content | Custom-trained internal bot on company knowledge |
| Price (plan, Kev to confirm) | $299 setup + $49/month | $799+ setup + $149-299/month (plan also gives $1,000-3,000 setup by size) |
| Hosting (plan) | Small local model (~2GB RAM), website only | Local model for small companies; partner inference for larger ones |
| Who it's for | SMEs wanting a smart FAQ/enquiry bot that keeps data local | 20-50+ staff companies wanting answers from their own documents |

## 1. Scope

- What it must answer, and what it must hand to a person
- Source content: website pages, FAQs, policies, internal docs (client supplies; we don't invent facts)
- Where enquiries go (email, CRM, form)
- Data rules: what can and can't be loaded, where it's hosted

## 2. Build

1. Collect and clean the source content. Remove anything sensitive the client didn't approve.
2. Load it into the model / knowledge base.
3. Write the bot's instructions: tone (plain, friendly, Australian), what it won't do, when it hands over.
4. Tier 1: embed on a test page first. Tier 2: connect to the client's workspace with their own accounts.

## 3. Test (all must pass)

- [ ] Top 10 real questions answered correctly from the source
- [ ] Question not in the source: says it doesn't know and offers a person, doesn't invent
- [ ] Asked for prices, dates or promises it wasn't given: refuses politely
- [ ] Sensitive data request: refuses
- [ ] Client asks 5 questions themselves and approves

## 4. Go-live

Embed on the live site (Tier 1) or roll out to staff (Tier 2). Review the transcripts weekly for the first month. Then move to [[handover-and-adoption]].
