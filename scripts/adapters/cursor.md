# Cursor AI Adapter

This adapter configures Cursor AI to use LEADGENAGENCY as workspace rules.

## Setup

1. Open Cursor in the `/home/luciousfox/Projects/megaleads` directory
2. Go to Cursor Settings → Workspace → Rules
3. Set the rules file to point to `CLAUDE.md`
4. Or copy the contents of `CLAUDE.md` directly into the workspace rules

## Workspace Rules Configuration

```json
{
  "workspace": {
    "rules": [
      {
        "pattern": "**/*",
        "description": "LEADGENAGENCY orchestrator",
        "file": "CLAUDE.md"
      }
    ]
  }
}
```

## Usage

### Rule Loading

Cursor AI loads workspace rules automatically when you open the project. The orchestrator becomes available in AI Chat with the context of the full system.

### Claude Mode

In Cursor's Claude mode, you can direct-chat with the orchestrator:

```
Parse the brief at projects/2026-01-15-clientname/brief.md
```

```
Run the full-lead-gen-setup workflow for the active project
```

```
Show me the content calendar from projects/2026-01-15-clientname/wiki/content-calendar.md
```

## Auto-Load Behavior

When a project is opened:
1. Cursor reads `CLAUDE.md` automatically (if configured as workspace rules)
2. The orchestrator boots: reads `state/ledger.md`, identifies active project
3. You're ready to command

## File Watching

Cursor's workspace rules watch for file changes. This keeps the orchestrator aware of:
- New project directories created in `projects/`
- Gate approval files added to `state/tasks/`
- Handoff files written to `state/handoffs/`