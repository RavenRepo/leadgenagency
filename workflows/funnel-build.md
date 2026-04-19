# Funnel Build Workflow

Scoped workflow for clients who have an existing lead magnet and need the full funnel built around it.

## Prerequisites

Client must already have:
- A completed lead magnet (at projects/[active]/wiki/lead-magnet.md)

## Pipeline Stages

```
brief-parser → [GATE 1]
icp-researcher → [GATE 2]
funnel-architect → (no gate)
landing-page-copywriter → [GATE 3]
email-sequence-writer → [GATE 4]
newsletter-strategist → (no gate)
dm-copywriter → (no gate)
qa-checker
```

## Stage Details

### brief-parser
- Input: projects/[active]/brief.md
- Output: projects/[active]/raw/brief-parser/parsed-brief.md
- Gate: Missing info check

### icp-researcher
- Input: parsed-brief.md
- Output: projects/[active]/raw/icp-researcher/icp-profile.md
- Gate: ICP approval

### funnel-architect
- Input: lead-magnet (existing), parsed-brief.md
- Output: projects/[active]/raw/funnel-architect/funnel-map.md
- No gate — architecture stage

### landing-page-copywriter
- Input: lead-magnet (existing), icp-profile.md, parsed-brief.md
- Output: projects/[active]/wiki/landing-page-copy.md
- Gate: Copy review

### email-sequence-writer
- Input: funnel-map.md, icp-profile.md, lead-magnet (existing)
- Output: projects/[active]/wiki/email-sequence.md
- Gate: Sequence review

### newsletter-strategist
- Input: icp-profile.md, email-sequence.md
- Output: projects/[active]/wiki/newsletter-strategy.md
- No gate

### dm-copywriter
- Input: icp-profile.md, lead-magnet (existing)
- Output: projects/[active]/wiki/dm-scripts.md
- No gate

### qa-checker
- Input: All wiki/ deliverables
- Output: projects/[active]/raw/qa-checker/qa-report.md
- Gate: Final QA

## Deliverables

- projects/[active]/wiki/landing-page-copy.md
- projects/[active]/wiki/email-sequence.md
- projects/[active]/wiki/newsletter-strategy.md
- projects/[active]/wiki/dm-scripts.md

## When to Use

Use this workflow when:
- Client has a lead magnet already (PDF, guide, template)
- Client needs the funnel infrastructure around it
- Faster than full setup (skips lead magnet creation)
- Typically 4-5 days instead of 7