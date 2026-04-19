# Lead Magnet Creation Workflow

Scoped workflow for clients who need only the lead magnet component.

## Pipeline Stages

```
brief-parser → [GATE 1]
icp-researcher → [GATE 2]
lead-magnet-strategist → [GATE 3]
lead-magnet-builder → [GATE 4]
qa-checker (lead magnet only)
```

## Stage Details

### Stage 1: brief-parser
- Input: projects/[active]/brief.md
- Output: projects/[active]/raw/brief-parser/parsed-brief.md
- Gate: Confirm all fields extracted correctly

### Stage 2: icp-researcher
- Input: parsed-brief.md
- Output: projects/[active]/raw/icp-researcher/icp-profile.md
- Gate: Confirm ICP is accurate

### Stage 3: lead-magnet-strategist
- Input: icp-profile.md, parsed-brief.md
- Output: projects/[active]/raw/lead-magnet-strategist/lead-magnet-brief.md
- Gate: Approve format + title

### Stage 4: lead-magnet-builder
- Input: lead-magnet-brief.md, icp-profile.md
- Output: projects/[active]/wiki/lead-magnet.md
- Gate: Review full content

### QA: qa-checker (lead magnet scope)
- Input: lead-magnet.md
- Output: projects/[active]/raw/qa-checker/qa-report.md
- Gate: Final approval

## Deliverables

- projects/[active]/wiki/lead-magnet.md

## When to Use

Use this workflow when:
- Client only needs a lead magnet (not full funnel)
- Client has an existing funnel and just needs new lead magnet content
- Client wants to test a lead magnet concept before committing to full setup
- Fast turnaround needed (can complete in 1-2 days)