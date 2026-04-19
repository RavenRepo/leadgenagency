# Claude Code Adapter

This adapter enables Claude Code to run LEADGENAGENCY as a Claude Project or via CLI.

## Setup

### Option A: Claude Projects (Recommended)

1. Open Claude Code in the `/home/luciousfox/Projects/megaleads` directory
2. Claude Code automatically reads `CLAUDE.md` at session start
3. You're ready to run — just describe what you want to build

### Option B: CLI with `--system-flag`

```bash
claude -p "$(cat CLAUDE.md)" --allowedTools "Bash,Read,Write,Edit,Glob,Grep" "Your message here"
```

## Usage

### Starting a New Project

```bash
cd /home/luciousfox/Projects/megaleads
./start "Client Name" /path/to/brief.md
```

### Continuing After Gate Approval

```bash
cd /home/luciousfox/Projects/megaleads
./continue 2026-01-15-clientname
```

### Requesting Revisions

```bash
cd /home/luciousfox/Projects/megaleads
./revise 2026-01-15-clientname "Feedback text"
```

### Checking Status

```bash
cd /home/luciousfox/Projects/megaleads
./status 2026-01-15-clientname
```

## Script Files

The project root contains shell scripts for orchestrator commands:

- `start` — Initialize new project, parse brief, pause at GATE 1
- `continue` — Resume after human gate approval
- `revise` — Send project back for revision with feedback
- `status` — Show current workflow stage and gate status

All scripts should be executable (`chmod +x start continue revise status`).

## Direct Orchestration

You can also speak directly to the orchestrator:

```
Parse the brief for project 2026-01-15-clientname and show me the parsed output.
```

```
Run the full-lead-gen-setup workflow for 2026-01-15-clientname.
```

```
Show me the current status of all active projects.
```

## Tool Access

The orchestrator needs these tools to function:
- File Read/Write/Edit
- Bash (for creating directories, running scripts)
- Glob (for finding files)
- Grep (for searching content)