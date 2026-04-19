<div align="center">

# LeadGenAgency

### Turn audience attention into paying clients — automatically

<p>

<img src="https://img.shields.io/badge/Agents-13-0F766E?style=for-the-badge" alt="13 agents" />
<img src="https://img.shields.io/badge/Workflows-6-EA580C?style=for-the-badge" alt="6 workflows" />
<img src="https://img.shields.io/badge/Skills-10-7C3AED?style=for-the-badge" alt="10 skills" />
<img src="https://img.shields.io/badge/Human%20Gates-7-1D4ED8?style=for-the-badge" alt="7 human gates" />

</p>

<p>**Brief** | **ICP** | **Lead Magnet** | **Landing** | **Email** | **Content** | **DM**</p>

<p>📋 🔍 🎯 📄 📧 📅 💬</p>

</div>

---

## Why This Repo Exists

Most AI marketing setups break when tasks become cross-functional.
This system solves that by giving you:

- A single orchestrator that routes work to the right specialist agent
- File-based state for resumable projects and predictable handoffs
- QA validation before delivery
- Human approval gates before risky actions

---

## What You Can Do

- Build a complete lead generation system from a client brief
- Generate ICP profiles with psychographics, VOC, and watering holes
- Create high-converting lead magnets (checklists, blueprints, templates, courses)
- Write landing page copy targeting 60%+ opt-in rates
- Design full funnels with email nurture sequences
- Plan 30-day content calendars across 5 post types
- Write warm DM outreach scripts that get replies

---

## Quick Start

### 1) Configure your provider

```bash
cp config.env.example config.env
# Then edit config.env and set one of:
# PROVIDER=claude
# PROVIDER=opencode
# PROVIDER=copilot
```

### 2) Start your AI client in this repo

```bash
cd leadgenagency
claude
```

### 3) Give the orchestrator a real task

```text
"Create a full lead gen system for a B2B SaaS founder who sells a course"
"Build me a lead magnet and landing page for a executive coach"
"Generate a 30-day LinkedIn content calendar for a marketing agency"
```

---

## Example Prompts You Can Copy

### Full pipeline example

```text
Run full-lead-gen-setup workflow for Acme Corp. Brief is at projects/2026-04-20-acme/brief.md
```

### Lead magnet only example

```text
Use lead-magnet-creation workflow: brief at projects/2026-04-20-acme/brief.md
```

### ICP research example

```text
Run icp-researcher agent on projects/2026-04-20-acme/raw/brief-parser/parsed-brief.md
```

---

## Shell Orchestrator Commands

These wrappers call the orchestrator.

### Create a project

```bash
./start "Acme Corp" ./brief.md
```

Creates:

- projects/YYYY-MM-DD-acme-corp/
- raw/ and wiki/ subdirectories
- brief.md copied in

### Continue a project (after gate approval)

```bash
./continue 2026-04-20-acme-corp
```

### Request revisions

```bash
./revise 2026-04-20-acme-corp "The headline doesn't match the ICP"
```

### Check status

```bash
./status 2026-04-20-acme-corp
```

---

## The 13 Agents

| Agent | Role |
|---|---|
| `brief-parser` | Transforms raw brief into structured intake |
| `icp-researcher` | Builds deep ICP: demographics, psychographics, VOC |
| `lead-magnet-strategist` | Matches format + topic to ICP + offer |
| `lead-magnet-builder` | Writes complete lead magnet content |
| `landing-page-copywriter` | Crafts 60%+ CVR landing page copy |
| `funnel-architect` | Designs 5-stage funnel + tech stack |
| `email-sequence-writer` | Writes 7-email nurture sequence |
| `content-strategist` | Builds 30-day content calendar |
| `post-writer` | Writes individual social posts |
| `newsletter-strategist` | Structures ongoing newsletter |
| `dm-copywriter` | Writes warm outreach scripts |
| `qa-checker` | Audits all deliverables |
| `orchestrator` | Coordinates everything |

---

## The 7-Day Pipeline

| Day | Agent | Gate |
|---|---|:---:|
| 1 | Brief Parser | Review |
| 2 | ICP Researcher | ✅ |
| 2 | Lead Magnet Strategist | ✅ |
| 3 | Lead Magnet Builder | ✅ |
| 3 | Landing Page Copywriter | ✅ |
| 4 | Funnel Architect | — |
| 4 | Email Sequence Writer | ✅ |
| 5 | Content Strategist | — |
| 5 | Post Writer (batch 1-14) | — |
| 6 | Newsletter Strategist | — |
| 6 | DM Copywriter | — |
| 7 | QA Checker | ✅ |

---

## Human Approval Gates

Before the pipeline continues, you review and approve:

- **GATE 1** — Brief parsing: all fields populated?
- **GATE 2** — ICP profile: demographics + VOC ring true?
- **GATE 3** — Lead magnet: format + title approved?
- **GATE 4** — Lead magnet content: quick win, bridge?
- **GATE 5** — Landing page: headline, bullets, CTA?
- **GATE 6** — Email sequence: conversational? No pitch before E7?
- **GATE 7** — Final QA: any FAILs need fixing?

---

## The 6 Workflows

| Workflow | When to Use |
|---|---|
| `full-lead-gen-setup` | Complete 7-day pipeline |
| `lead-magnet-creation` | Lead magnet only |
| `funnel-build` | Existing lead magnet → full funnel |
| `content-calendar-setup` | 30-day calendar + posts |
| `dm-campaign-launch` | DM outreach system only |
| `gates` | Human approval definitions |

---

## Project Structure

```text
leadgenagency/
├── CLAUDE.md                 # Master orchestrator
├── agents/                   # 13 agent definitions
├── workflows/                # 6 workflow definitions
├── skills/                  # 10 reusable skill modules
├── templates/               # Input/output templates
│   ├── brief-template.md  # Client brief template
│   ├── frameworks/          # 6 framework templates
│   └── deliverables/        # 6 deliverable templates
├── state/                   # Orchestrator state
│   ├── ledger.md           # Master state
│   ├── PROTOCOL.md         # State management rules
│   ├── tasks/             # Per-agent task files
│   └── handoffs/          # Agent handoff notes
├── learning/               # Self-improving memory
├── knowledge/              # Persistent benchmarks
├── scripts/adapters/       # Claude, Cursor, OpenCode
└── projects/              # Client project directories
```

---

## Provider Support

Current script adapters included:

- claude
- opencode
- copilot

To switch provider, edit config.env:

```env
PROVIDER=claude
```

---

## Deliverable Standard

All outputs follow this shape:

```markdown
# [Deliverable Title]
**Agent**: [agent-name]
**Date**: YYYY-MM-DD
**Client/Project**: [name]
**Status**: Draft | Review | Final

## Executive Summary
[2-3 sentence overview]

## [Section]
[Structured content]

## Quality Criteria
[Self-check before marking done]

## Handoff Notes
[What the next agent needs to know]
```

---

<div align="center">

## Ready To Run

Start with one line:

```bash
./start "Your Client" ./brief.md
```

Then ask your AI tool:

```text
"Run full-lead-gen-setup for the active project"
```

</div>