# Parse Brief Skill

Extraction rules, field definitions, and [MISSING] flag protocol for the brief-parser agent.

## Extraction Rules

### Rule 1: Extract Only, Never Invent
Read the brief exactly. Do not:
- Assume what the client meant
- Fill gaps with generic information
- Infer business model details not in text
- Project optimistic outcomes

### Rule 2: Surface All Missing Information
Every field that cannot be confidently extracted must be marked [MISSING: field-name]

### Rule 3: Preserve Original Wording
Where possible, use client's exact words in quotes for key phrases.

## Field Definitions

### offer_description
What does the client sell? Products, services, pricing tiers if mentioned.
- Look for: "I offer", "we sell", "my service", pricing pages sections
- Extract: product name, key features, what makes it different

### target_audience
Who do they sell to?
- Look for: "I help", "my clients are", "target market", ICP mentions
- Extract: job titles, industries, company sizes, pain points mentioned

### current_lead_gen
What are they doing now to get leads?
- Look for: "currently", "I've tried", "we're doing", what channels they mention
- Extract: specific tactics (LinkedIn, cold email, referrals, ads, etc.)

### revenue_goals
What do they want to achieve?
- Look for: "I want to", "goal is", "aiming for", revenue mentions
- Extract: specific numbers if given, timeframe if stated

### platform_focus
Where do they want to focus efforts?
- Look for: platform mentions, "I want to grow on", "focused on"
- Extract: specific platforms (LinkedIn, X, email, etc.)

### existing_assets
What do they already have?
- Look for: "I have", "we already", existing infrastructure mentions
- Extract: landing pages, email lists, lead magnets, tools, team

### timeline_budget
What's their timeline and budget?
- Look for: "by", "within", "budget of", urgency language
- Extract: specific dates or timeframes, budget ranges if mentioned

## [MISSING] Flag Protocol

Format: `[MISSING: field-name]`

When a field is missing:
1. Write exactly: `[MISSING: field-name]`
2. In notes section, suggest what to ask client
3. Do NOT guess — wait for human to provide

Example missing entry:
```
platform_focus: [MISSING: platform_focus]
Note: Client did not mention preferred platforms. Ask: "Where do you
want to focus your lead generation efforts?"
```

## Quality Checklist

Before marking brief-parser complete:
- [ ] offer_description is filled or [MISSING]
- [ ] target_audience is filled or [MISSING]
- [ ] current_lead_gen is filled or [MISSING]
- [ ] revenue_goals is filled or [MISSING]
- [ ] platform_focus is filled or [MISSING]
- [ ] existing_assets is filled or [MISSING]
- [ ] timeline_budget is filled or [MISSING]
- [ ] No invented information in any field
- [ ] Original client language preserved where possible