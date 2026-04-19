# QA Check Skill

Full QA checklists, pass/fail criteria, revision request format for the qa-checker agent.

## QA Process

### Step 1: Load All Deliverables
Read all files in projects/[active]/wiki/

### Step 2: Run Each Checklist
For each deliverable, run the applicable checklist below

### Step 3: Rate Each Item
- PASS: Meets criteria fully
- FAIL: Does not meet criteria, needs revision
- NEEDS REVISION: Partially meets, needs improvement

### Step 4: Write QA Report
Format per template at templates/frameworks/qa-report-template.md

## Lead Magnet Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | ICP VOC language used throughout | PASS/FAIL |
| 2 | Quick win delivered in first 20% | PASS/FAIL |
| 3 | Each section has actionable takeaway | PASS/FAIL |
| 4 | Bridge to paid offer feels natural | PASS/FAIL |
| 5 | Tone matches ICP sophistication | PASS/FAIL |
| 6 | Length appropriate to format | PASS/FAIL |
| 7 | Designer notes included | PASS/FAIL |

## Landing Page Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | Headline: specific, not clever | PASS/FAIL |
| 2 | Subheadline: deliverable + ICP named | PASS/FAIL |
| 3 | All 5 hero bullets name results | PASS/FAIL |
| 4 | Social proof block present | PASS/FAIL |
| 5 | Above-fold complete without scrolling | PASS/FAIL |
| 6 | Every bullet names a result | PASS/FAIL |
| 7 | CTA button is first-person | PASS/FAIL |
| 8 | 5 CTA button variants provided | PASS/FAIL |
| 9 | Meta description 160 chars max | PASS/FAIL |
| 10 | A/B test headline variants included | PASS/FAIL |

## Email Sequence Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | Subject lines max 8 words | PASS/FAIL |
| 2 | Preview text completes subject | PASS/FAIL |
| 3 | One CTA per email | PASS/FAIL |
| 4 | No salesy language before email 7 | PASS/FAIL |
| 5 | Sequence reads as conversation | PASS/FAIL |
| 6 | Each email has one job only | PASS/FAIL |
| 7 | PS on emails 1, 4, 7 only | PASS/FAIL |
| 8 | Email 7 has clear urgency | PASS/FAIL |

## Content Calendar Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | Post type ratios correct (25/20/20/20/15) | PASS/FAIL |
| 2 | Every post has a clear CTA | PASS/FAIL |
| 3 | Lead magnet CTA appears 2x+ per week | PASS/FAIL |
| 4 | Posting schedule included | PASS/FAIL |
| 5 | Hashtag strategy included | PASS/FAIL |
| 6 | Content repurposing map included | PASS/FAIL |
| 7 | All 30 days covered | PASS/FAIL |

## DM Scripts Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | No script opens with "I" | PASS/FAIL |
| 2 | No pitch in first-touch scripts (1-4) | PASS/FAIL |
| 3 | Max 1 question per script | PASS/FAIL |
| 4 | All 6 script types included | PASS/FAIL |
| 5 | Trigger conditions specified | PASS/FAIL |
| 6 | Scripts feel handwritten | PASS/FAIL |
| 7 | Escalation path clear | PASS/FAIL |

## Newsletter Strategy Checklist

| # | Criteria | Status |
|---|----------|--------|
| 1 | Newsletter name and tagline present | PASS/FAIL |
| 2 | Cadence specified (weekly/biweekly) | PASS/FAIL |
| 3 | Issue template repeatable | PASS/FAIL |
| 4 | Monetization ladder phased | PASS/FAIL |
| 5 | Growth loops specified | PASS/FAIL |
| 6 | Reactivation sequence included | PASS/FAIL |

## FAIL Item Fix Instructions

For every FAIL item, provide:
1. Which file has the issue
2. What specifically is wrong
3. How to fix it (specific instruction)

Example:
```
FAIL #3: Lead Magnet - Hero bullets name features not results

File: wiki/lead-magnet.md

Issue: "You'll get our proven framework" — "framework" is a feature, not a result.

Fix: Replace with specific outcome. Example: "You'll have a complete
go-to-market strategy ready to implement in 2 hours"
```

## Quality Thresholds

- 0-2 FAILs: Approve for delivery
- 3-5 FAILs: Send back for revision
- 6+ FAILs: Significant revision needed, gate re-review required

## QA Report Output Format

```markdown
# QA Report: [project-id]
## Date: YYYY-MM-DD

## Overall Status: PASS / FAIL / NEEDS REVISION

## Deliverable Breakdown

### lead-magnet.md
- FAILs: [count]
- NEEDS REVISION: [count]
- [List of specific issues]

### landing-page-copy.md
...

## FAIL Items Requiring Fix

1. [FAIL description + fix instruction]
...

## Final Recommendation

[Approve for delivery / Send back for revision]
```