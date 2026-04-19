# Full Lead Gen Setup Workflow

The complete 7-day end-to-end pipeline for a full lead generation system.

## Pipeline Stages

```
Day 1 → brief-parser → [GATE 1: missing info check]
Day 2 → icp-researcher → [GATE 2: human ICP approval]
Day 2 → lead-magnet-strategist → [GATE 3: format + title approval]
Day 3 → lead-magnet-builder → [GATE 4: content review]
Day 3 → landing-page-copywriter → [GATE 5: copy review]
Day 4 → funnel-architect → (no gate)
Day 4 → email-sequence-writer → [GATE 6: sequence review]
Day 5 → content-strategist → (no gate)
Day 5 → post-writer (batch: first 7 days) → (no gate)
Day 6 → newsletter-strategist → (no gate)
Day 6 → dm-copywriter → (no gate)
Day 7 → qa-checker → [GATE 7: final QA]
```

## Stage Details

### Day 1

**brief-parser**
- Input: projects/[active]/brief.md
- Output: projects/[active]/raw/brief-parser/parsed-brief.md
- Gate: Present parsed brief. Human confirms fields are correct, fills [MISSING] items.

### Day 2 AM

**icp-researcher**
- Input: parsed-brief.md
- Output: projects/[active]/raw/icp-researcher/icp-profile.md
- Gate: Present ICP profile. Human confirms demographics, psychographics, VOC phrases ring true.

**lead-magnet-strategist** (runs after icp-researcher gate passes)
- Input: icp-profile.md, parsed-brief.md
- Output: projects/[active]/raw/lead-magnet-strategist/lead-magnet-brief.md
- Gate: Human approves format choice and title.

### Day 3

**lead-magnet-builder**
- Input: lead-magnet-brief.md, icp-profile.md
- Output: projects/[active]/wiki/lead-magnet.md
- Gate: Human reviews full lead magnet content.

**landing-page-copywriter** (can run parallel to lead-magnet-builder)
- Input: lead-magnet-brief.md, icp-profile.md, parsed-brief.md
- Output: projects/[active]/wiki/landing-page-copy.md
- Gate: Human approves landing page copy.

### Day 4

**funnel-architect**
- Input: landing-page-copy.md, lead-magnet-brief.md, parsed-brief.md
- Output: projects/[active]/raw/funnel-architect/funnel-map.md
- No gate — this is architecture, not client-facing copy.

**email-sequence-writer**
- Input: funnel-map.md, icp-profile.md, lead-magnet-brief.md
- Output: projects/[active]/wiki/email-sequence.md
- Gate: Human reviews full email sequence.

### Day 5

**content-strategist**
- Input: icp-profile.md, parsed-brief.md, lead-magnet-brief.md
- Output: projects/[active]/wiki/content-calendar.md
- No gate — calendar is a plan, not final copy.

**post-writer** (batch: Days 1-7 of calendar)
- Input: content-calendar.md, icp-profile.md
- Output: projects/[active]/wiki/posts/day-01-authority.md through day-07-*.md
- No gate — spot-check only.

### Day 6

**newsletter-strategist**
- Input: icp-profile.md, email-sequence.md, content-calendar.md
- Output: projects/[active]/wiki/newsletter-strategy.md
- No gate.

**dm-copywriter**
- Input: icp-profile.md, lead-magnet-brief.md, content-calendar.md
- Output: projects/[active]/wiki/dm-scripts.md
- No gate.

### Day 7

**qa-checker**
- Input: All wiki/ deliverables
- Output: projects/[active]/raw/qa-checker/qa-report.md
- Gate: Human reviews QA report. Approves or sends back for revisions.

## Deliverables

Final wiki/ directory contains:
- lead-magnet.md
- landing-page-copy.md
- email-sequence.md
- content-calendar.md
- newsletter-strategy.md
- dm-scripts.md
- posts/ (30 individual post files)

## Gate Summary

| Gate | Agent | Pause Point |
|------|-------|-------------|
| 1 | brief-parser | After missing info check |
| 2 | icp-researcher | After ICP profile |
| 3 | lead-magnet-strategist | After brief |
| 4 | lead-magnet-builder | After content |
| 5 | landing-page-copywriter | After copy |
| 6 | email-sequence-writer | After sequence |
| 7 | qa-checker | Final delivery |