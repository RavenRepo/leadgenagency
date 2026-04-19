# Content Calendar Setup Workflow

Scoped workflow for clients who need a 30-day content calendar and initial posts fast.

## Pipeline Stages

```
brief-parser → [GATE 1]
icp-researcher → [GATE 2]
content-strategist → (no gate)
post-writer (batch: first 14 days) → (no gate)
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

### content-strategist
- Input: icp-profile.md, parsed-brief.md
- Output: projects/[active]/wiki/content-calendar.md
- No gate — plan stage

### post-writer (first 14 days)
- Input: content-calendar.md, icp-profile.md
- Output: projects/[active]/wiki/posts/day-01-authority.md through day-14-*.md
- No gate — spot-check only

## Post Coverage

This workflow produces posts for Days 1-14. The remaining Days 15-30 can be:
- Produced in a second batch with another post-writer run
- Handled by client with calendar as guide
- Produced weekly as part of ongoing content service

## Deliverables

- projects/[active]/wiki/content-calendar.md (full 30-day calendar)
- projects/[active]/wiki/posts/day-01-authority.md through day-14-*.md

## When to Use

Use this workflow when:
- Client needs content fast (launch week)
- Client has existing lead magnet and funnel
- Client's primary need is social content
- Testing content approach before full funnel investment