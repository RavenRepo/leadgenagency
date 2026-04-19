# OpenCode Adapter

This adapter configures OpenCode to run LEADGENAGENCY orchestrator.

## Setup

```bash
cd /home/luciousfox/Projects/megaleads
opencode --rules CLAUDE.md
```

## Configuration

Create `.opencode.json` in the project root:

```json
{
  "rules": ["CLAUDE.md"],
  "tools": ["read", "write", "edit", "bash", "glob", "grep"],
  "project": "/home/luciousfox/Projects/megaleads"
}
```

## Usage

### Interactive Mode

```bash
opencode run --prompt "Start a new project for Acme Corp with brief at ~/briefs/acme.md"
```

### Script Mode

```bash
opencode run --prompt "$(cat <<'EOF'
Initialize project 2026-01-15-acme
Workflow: full-lead-gen-setup
Begin with brief-parser agent
EOF
)"
```

## Tool Access

OpenCode needs these tools enabled:
- `read` — Read files, agent definitions, task files
- `write` — Write agent outputs, wiki deliverables
- `edit` — Update ledger, modify files
- `bash` — Create directories, run scripts
- `glob` — Find files across projects
- `grep` — Search content, find handoffs

## Session Management

Each OpenCode session:
1. Reads `CLAUDE.md` on start
2. Reads `state/ledger.md` to identify active project
3. Maintains context across turns
4. Writes outputs to `projects/[active]/raw/[agent]/`

## Exit Behavior

When exiting:
- State is persisted in `state/ledger.md`
- Next session resumes where this one left off
- Gate pending files remain for human review