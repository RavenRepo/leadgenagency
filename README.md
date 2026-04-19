# LeadGenAgency

### Turn audience attention into paying clients — automatically.

A fully orchestrated multi-agent system that delivers complete lead generation systems: from ICP research and lead magnets, through landing pages and email sequences, to content calendars and DM outreach scripts.

Built on the same patterns as [contentmarketingagency](https://github.com/your-org/contentmarketingagency) — scaled down to 13 focused agents instead of 34.

---

## How It Works

```
Client Brief → ICP Profile → Lead Magnet → Landing Page
→ Email Sequence → Content Calendar → DM Scripts → Done
```

**You give it a client's brief. It delivers a complete lead generation system.**

---

## The 7-Day Pipeline

| Day | Agent | Output | Gate |
|-----|-------|--------|------|
| 1 | **Brief Parser** | Parsed brief (structured intake) | Review |
| 2 | **ICP Researcher** | Deep customer profile | Approval |
| 2 | **Lead Magnet Strategist** | Format + title selection | Approval |
| 3 | **Lead Magnet Builder** | Complete lead magnet content | Review |
| 3 | **Landing Page Copywriter** | High-CVR landing page | Approval |
| 4 | **Funnel Architect** | Full funnel map + tech stack | — |
| 4 | **Email Sequence Writer** | 7-email nurture sequence | Approval |
| 5 | **Content Strategist** | 30-day content calendar | — |
| 5 | **Post Writer** | First 14 social posts | — |
| 6 | **Newsletter Strategist** | Ongoing newsletter structure | — |
| 6 | **DM Copywriter** | 6-type warm outreach system | — |
| 7 | **QA Checker** | Full quality audit | Final |

---

## What You Get

Every client engagement produces a complete deliverable set:

```
projects/YYYY-MM-DD-client/
├── wiki/                          # Final deliverables
│   ├── lead-magnet.md           # PDF/guide/blueprint content
│   ├── landing-page-copy.md     # High-converting page copy
│   ├── email-sequence.md         # 7-email sequence (D0–D10)
│   ├── content-calendar.md      # 30-day calendar
│   ├── newsletter-strategy.md    # Ongoing newsletter structure
│   ├── dm-scripts.md            # 6 DM script types
│   └── posts/                   # Individual social posts
│       ├── day-01-authority.md
│       ├── day-02-story.md
│       └── ...
├── raw/                          # Agent working files
│   ├── brief-parser/
│   ├── icp-researcher/
│   ├── lead-magnet-strategist/
│   └── ...
└── brief.md                      # Original client brief
```

---

## Quick Start

### 1. Initialize a project

```bash
./start "Acme Corp" /path/to/acme-brief.md
```

### 2. Run through the gates

```bash
./continue 2026-04-20-acme-corp   # After approving brief parser
./continue 2026-04-20-acme-corp   # After approving ICP
./continue 2026-04-20-acme-corp   # After approving lead magnet
# ... continue through all gates
```

### 3. Request revisions if needed

```bash
./revise 2026-04-20-acme-corp "The headline doesn't resonate with the ICP"
```

### 4. Check status

```bash
./status 2026-04-20-acme-corp
```

---

## The 13 Agents

| Agent | Role |
|-------|------|
| `brief-parser` | Transforms raw brief into structured intake |
| `icp-researcher` | Builds deep ICP: demographics, psychographics, VOC, watering holes |
| `lead-magnet-strategist` | Matches format + topic to ICP + offer |
| `lead-magnet-builder` | Writes the complete lead magnet |
| `landing-page-copywriter` | Crafts 60%+ CVR landing page copy |
| `funnel-architect` | Designs the full funnel architecture |
| `email-sequence-writer` | Writes 7-email nurture sequence |
| `content-strategist` | Builds 30-day content calendar |
| `post-writer` | Writes individual social posts |
| `newsletter-strategist` | Structures the ongoing newsletter |
| `dm-copywriter` | Writes warm outreach scripts |
| `qa-checker` | Audits all deliverables |
| `orchestrator` | Coordinates everything |

---

## The 6 Workflows

| Workflow | When to Use |
|----------|-------------|
| `full-lead-gen-setup` | Complete 7-day pipeline for new clients |
| `lead-magnet-creation` | Only need the lead magnet |
| `funnel-build` | Have a lead magnet, need the funnel |
| `content-calendar-setup` | Need content calendar + first posts |
| `dm-campaign-launch` | Need DM outreach system only |
| `gates` | Human approval checkpoint definitions |

---

## The 10 Skills

| Skill | What It Does |
|-------|--------------|
| `parse-brief` | Extraction rules, field definitions, [MISSING] flag protocol |
| `icp-research` | JTBD, Pain/Gain/Fear, VOC extraction |
| `lead-magnet-match` | Format scoring matrix, title formulas |
| `landing-page-copy` | 9-section structure, CVR benchmarks |
| `funnel-architecture` | 5-stage funnel, tech stack tiers, KPI benchmarks |
| `post-type-selection` | 5 post types, hook formulas, platform formatting |
| `newsletter-sequence` | PAS/AIDA/Story-Proof-Offer frameworks |
| `dm-sequence` | 6 script types, trigger conditions, escalation |
| `qa-check` | Full checklists, pass/fail criteria |
| `analytics-setup` | UTM setup, KPI tracking, dashboard |

---

## Human Gates

Every gate pauses for human review before the pipeline continues:

| Gate | What to Review |
|------|---------------|
| 1 | Brief parsing — all fields populated? |
| 2 | ICP profile — demographics, VOC ring true? |
| 3 | Lead magnet format + title — does it fit? |
| 4 | Lead magnet content — quick win, bridge? |
| 5 | Landing page copy — headline, bullets, CTA? |
| 6 | Email sequence — conversational? No pitch before E7? |
| 7 | Final QA report — any FAILs need fixing? |

---

## Self-Improving System

The `learning/` directory captures lessons from every project:

- `learning/global/` — cross-agent systemic patterns
- `learning/per-agent/` — per-agent lessons
- `knowledge/` — reusable benchmarks by industry

The system gets smarter with every client project.

---

## Project Structure

```
leadgenagency/
├── CLAUDE.md                    # Master orchestrator
├── agents/                     # 13 agent definitions
├── workflows/                   # 6 workflow definitions
├── skills/                     # 10 reusable skill modules
├── templates/                   # Input/output templates
│   ├── brief-template.md       # Client brief template
│   ├── frameworks/              # 6 framework templates
│   └── deliverables/           # 6 deliverable templates
├── state/                      # Orchestrator state
│   ├── ledger.md               # Master state
│   ├── PROTOCOL.md             # State management rules
│   ├── tasks/                  # Per-agent task files
│   └── handoffs/               # Agent handoff notes
├── learning/                   # Self-improving memory
├── knowledge/                  # Persistent research wiki
├── scripts/adapters/           # Tool integrations
└── projects/                   # Client project directories
```

---

## Powered By

- [Claude Code](https://claude.ai) / [Cursor](https://cursor.sh) / [OpenCode](https://github.com/sideninja/opencode) / [Aider](https://aider.chat)
- OpenAI-compatible orchestration
- File-based agent system

---

## Pattern Reference

Built from patterns in [contentmarketingagency](https://github.com/your-org/contentmarketingagency) — the full 34-agent marketing agency system. LeadGenAgency is the focused, lead-gen-only version for clients who need a complete funnel without the full-service engagement.

---

*Built with precision. Built to convert.*