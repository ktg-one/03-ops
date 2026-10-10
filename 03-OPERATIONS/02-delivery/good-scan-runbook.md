---
title: Good Scan runbook
type: runbook
updated: 2026-10-10
source: old 03-OPERATIONS/processes/goodscan-pipeline-sop.md + processes/01-deep=dive/
---

# Good Scan (Deep DIVE audit) runbook

**The offer:** a diagnostic of one business, delivered as an interactive web portal instead of a PDF nobody reads. It's Tier 3 in the 8 Oct launch catalogue: **consult only** (priced per engagement, quoted after discovery).
**Also used as:** a lead magnet. A short scan of a prospect's public footprint opens the conversation for voice or workflow work.

## The D.I.V.E. score (0-100 each)

| Pillar | Looks at |
|---|---|
| **D** Defence | Privacy and compliance exposure, unencrypted forms, data leakage |
| **I** Identity | Positioning, authority signals, brand coherence |
| **V** Visibility | Search, Google Maps / citations, local SEO |
| **E** Experience | Intake and booking friction, response speed, conversion path |

## Steps

| # | Step | Output |
|---|---|---|
| 1 | Discovery call (see [[../01-sales/discovery-call]]); agree scope and price in writing | Accepted proposal |
| 2 | Payment clears → client folder from `03-clients/_client-template` | Folder + Todoist task |
| 3 | Research: website, Google profile, socials, public records → NotebookLM notebook in `leads/<client>/` | Notebook |
| 4 | Generate assets from the notebook: report, audio overview, infographic, deck | Raw bundle |
| 5 | Package: `pipeline.py --zip <bundle> --client <slug> --out <dir>` (in old `processes/01-deep=dive/`) | Portal folder |
| 6 | Review every claim in the report against a source. Cut anything unsourced | Checked report |
| 7 | Publish the portal (GitHub Pages: `ktg-one.github.io/<client>-audit/`) and send the link | Live portal |
| 8 | 20-min debrief call. Offer the fix (voice or workflow sprint) as the next step | Next step agreed |

## Required in every portal

`report.md`, `assets/audio.m4a`, `assets/info.png`, `assets/deck.pdf`, `assets/dossier.zip`. Video, data table and mind map are optional.

## Rules

- Public portals for **paying clients only**, and only with their OK. Prospect scans stay private (send the zip, don't publish).
- Score claims need a source. No invented findings.
- Pipeline CLI is verified; live delivery has not been run end to end yet. Do a dry run on our own business first.

## Done when

- [ ] Portal live (or zip sent) and debrief held
- [ ] Next step recorded in Todoist
- [ ] Asked permission to mention the work publicly (yes/no in the client folder)
