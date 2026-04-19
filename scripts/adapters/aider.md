# Aider CLI Adapter

This adapter configures Aider to work with LEADGENAGENCY orchestrator.

## Setup

```bash
cd /home/luciousfox/Projects/megaleads
aider --rules CLAUDE.md --no-git
```

## Configuration

Add to `.aider.conf` or use flags:

```bash
aider \
  --rules CLAUDE.md \
  --no-git \
  --read .CLAUDE.md \
  --write-propose read,write,edit,bash,glob,grep
```

## Usage

### Single Command Mode

```bash
aider --message "Parse the brief at projects/2026-01-15-clientname/brief.md"
```

### Interactive Mode

```bash
aider
# Within aider session:
# /rules CLAUDE.md
# Parse brief for project 2026-01-15-clientname
```

## Tool Access

Aider requires these tools for orchestrator operation:
- `read` — Read agent definitions, briefs, state files
- `write` — Write agent outputs, wiki deliverables
- `edit` — Update ledger, modify files
- `bash` — Scripts, directory creation
- `glob` — File discovery
- `grep` — Content search

## Multi-File Operations

Aider can handle multiple files for workflow operations:

```bash
aider \
  --message "Run the full-lead-gen-setup workflow. Start with brief-parser."
```

## Session Persistence

Aider sessions persist state in `state/ledger.md`:
- Project progress tracked per agent
- Gate status updated
- Handoff notes written

## Limitations

- Aider is primarily a code editing tool — orchestration commands work but feel less natural than Claude Code
- For best experience, use Aider for file operations and Claude Code for orchestration commands