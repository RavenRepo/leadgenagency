# State Management Protocol

## Ledger (Single Source of Truth)

`state/ledger.md` is the master state file. Only the orchestrator writes to it. Structure:

```markdown
# LEADGENAGENCY Master Ledger
Last Updated: [YYYY-MM-DD HH:MM]

## Active Project
Client: [name]
Project Dir: projects/YYYY-MM-DD-[name]/
Workflow: [workflow-name]
Current Stage: [stage name]
Current Agent: [agent name]
Status: IN_PROGRESS | GATE_PENDING | COMPLETE

## Completed Stages
- [x] [agent-name] → output: [path] [GATE PASSED]

## Open Gates
GATE [n]: [Gate Name] — PENDING HUMAN REVIEW
Location: [path]

## Notes
[Flags, issues, human comments]
```

## Task Files

`state/tasks/` contains per-agent task files. Format: `[agent-name]-task.md`

```markdown
# Task: [Agent Name]
## Project: [project-id]
## Created: [timestamp]

## Input Sources
- [path to source file]
- [path to source file]

## Instructions
[Specific instructions for this run, including any constraints from human gate feedback]

## Constraints
- [Any limitations or must-follow rules from gate feedback]
- [Must-complete requirements]

## Expected Output
[What this agent should produce]
```

## Handoff Files

Before any agent completes, it writes a handoff to `state/handoffs/`. Format: `[from-agent]-to-[to-agent].md`

```markdown
# Handoff: [From Agent] → [To Agent]
## Project: [project-id]
## Date: [timestamp]

## Current State
[What just completed]

## Output Location
[Path to the output file]

## What [Next Agent] Needs to Know
[Critical context, decisions made, things to watch for]

## Pending Gates
[Any gates still to pass before this work is final]
```

## Gate Files

Gate pending files at `state/tasks/GATE-[n]-[name]-PENDING.md`:

```markdown
# GATE [n]: [Gate Name]
## Project: [project-id]
## Paused At: [stage name]
## Output Location: [path to review]

## What to Review
[Specific items the human must evaluate]

## Approve → Run
`./continue [project-id]`

## Revise → Run
`./revise [project-id] "[feedback]"`
```

## File Lock Rules

When multiple agents might write to the same file:
- Create `learning/.lock` before writing, delete after
- If lock exists, wait 2 seconds and retry (max 5 retries)
- Orchestrator cleans stale locks older than 60 seconds

## Stage Naming Convention

Stages match workflow step names exactly. Use:
- `brief-parser`
- `icp-researcher`
- `lead-magnet-strategist`
- `lead-magnet-builder`
- `landing-page-copywriter`
- `funnel-architect`
- `email-sequence-writer`
- `content-strategist`
- `post-writer`
- `newsletter-strategist`
- `dm-copywriter`
- `qa-checker`

## Status Values

| Status | Meaning |
|--------|---------|
| IN_PROGRESS | Agent currently working |
| GATE_PENDING | Human review required before continuing |
| COMPLETE | All stages done, deliverables ready |
| ON_HOLD | Waiting for external input (client feedback, etc.) |