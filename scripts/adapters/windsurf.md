# Windsurf AI Adapter

This adapter configures Windsurf to use LEADGENAGENCY as workspace rules.

## Setup

1. Open Windsurf in the `/home/luciousfox/Projects/megaleads` directory
2. Go to Settings → Workspace → Rules
3. Add `CLAUDE.md` as the base rules file
4. Enable "Apply rules to all files in workspace"

## Windsurf Cascade Integration

Windsurf's Cascade feature can invoke the orchestrator directly:

### Starting a Session

1. Open Cascade in Windsurf
2. Navigate to the `/home/luciousfox/Projects/megaleads` directory
3. The orchestrator auto-loads from `CLAUDE.md`

### Direct Commands

```
Parse brief for: projects/2026-01-15-clientname/brief.md
```

```
Run workflow: full-lead-gen-setup on project 2026-01-15-clientname
```

```
Show status: state/ledger.md
```

## Supercomplete Context

Windsurf's Supercomplete feature provides context from:
- `state/ledger.md` — current project state
- `projects/[active]/brief.md` — active project brief
- `state/tasks/` — pending task files
- `state/handoffs/` — recent handoff notes

## Rule File

The `.windsurf/` directory in the project root can contain:

```json
{
  "rules": [
    {
      "file": "CLAUDE.md",
      "description": "LEADGENAGENCY Orchestrator"
    }
  ]
}
```