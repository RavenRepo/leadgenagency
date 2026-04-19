# DM Campaign Launch Workflow

Scoped workflow for ICP profiling and DM outreach system.

## Pipeline Stages

```
brief-parser → [GATE 1]
icp-researcher → [GATE 2]
dm-copywriter → (no gate)
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

### dm-copywriter
- Input: icp-profile.md, lead-magnet-brief.md (if exists), content-calendar.md (if exists)
- Output: projects/[active]/wiki/dm-scripts.md
- No gate

## Deliverables

- projects/[active]/wiki/dm-scripts.md (6 script types)

## Outputs Included

1. Post Engager DM — for post commenters
2. Lead Magnet Delivery DM — for comment-trigger leads
3. Profile Viewer DM — for profile visitors
4. Connection Follow-Up DM — after connection accepted
5. Warm Lead Nurture DM — for multi-engagers
6. Re-engagement DM — for cold warm leads

## Also Includes

- Outreach schedule (how many DMs per day)
- Response handling guidelines
- Escalation to call/cold email path

## When to Use

Use this workflow when:
- Client is ready to start outreach immediately
- Client needs DM scripts to start conversations
- Fast turnaround needed (can complete in 1 day)
- Part of broader content-led lead gen