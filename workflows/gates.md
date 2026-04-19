# Human-in-the-Loop Gates

Defines all 7 human approval checkpoints across the full-lead-gen-setup workflow.

## Gate Definitions

### GATE 1: Brief Parsing Check
**Agent:** brief-parser
**Pauses after:** parsed-brief.md created
**What human reviews:**
- All 8 fields populated or [MISSING] flagged
- No invented information (only extracted)
- Missing fields noted for follow-up

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to brief-parser

---

### GATE 2: ICP Approval
**Agent:** icp-researcher
**Pauses after:** icp-profile.md created
**What human reviews:**
- Demographics are accurate
- Psychographics resonate (VOC phrases sound right)
- Watering holes are specific and correct
- Buying triggers make sense

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to icp-researcher

---

### GATE 3: Lead Magnet Format + Title
**Agent:** lead-magnet-strategist
**Pauses after:** lead-magnet-brief.md created
**What human reviews:**
- Format choice justified against ICP
- Title passes: specific, desirable, believable
- Outline connects to paid offer

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to lead-magnet-strategist

---

### GATE 4: Lead Magnet Content
**Agent:** lead-magnet-builder
**Pauses after:** lead-magnet.md (in wiki/) finalized
**What human reviews:**
- VOC language used throughout
- Quick win in first 20%
- Each section actionable
- Paid offer bridge feels earned

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to lead-magnet-builder

---

### GATE 5: Landing Page Copy
**Agent:** landing-page-copywriter
**Pauses after:** landing-page-copy.md (in wiki/) finalized
**What human reviews:**
- Headline specific, not clever
- All bullets name results
- CTA button copy first-person
- Social proof present

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to landing-page-copywriter

---

### GATE 6: Email Sequence
**Agent:** email-sequence-writer
**Pauses after:** email-sequence.md (in wiki/) finalized
**What human reviews:**
- Subject lines max 8 words
- One CTA per email
- No salesy language before email 7
- Sequence reads as conversation

**Approve:** `./continue [project-id]`
**Revise:** `./revise [project-id] "[feedback]"` — goes back to email-sequence-writer

---

### GATE 7: Final QA
**Agent:** qa-checker
**Pauses after:** qa-report.md created
**What human reviews:**
- All checklist items PASS / FAIL / NEEDS REVISION
- FAIL items with specific fixes
- Final decision: approve for delivery or send back

**Approve:** `./continue [project-id]` — marks project COMPLETE
**Revise:** `./revise [project-id] "[feedback]"` — sends back to specific agent

---

## Gate File Format

Gate pending files are written to: `state/tasks/GATE-[n]-[name]-PENDING.md`

```markdown
# GATE [n]: [Gate Name]
## Project: [project-id]
## Paused At: [agent-name]
## Output Location: [path]

## What to Review
- [Specific items]

## Status: PENDING HUMAN REVIEW

## Approve → Run
`./continue [project-id]`

## Revise → Run
`./revise [project-id] "[feedback]"`
```

## Revision Cycles

- Maximum 3 revision cycles per gate
- After 3 cycles, flag for escalation (human-to-human discussion)
- Each revision cycle resets the counter for that specific gate

## Skip Conditions

Gates cannot be skipped except:
- P0 emergency (client explicitly requests)
- Documentation that all fields were pre-confirmed in brief
- Orchestrator documents skip reason in ledger.md