# PRD Skill

A Claude Code skill that generates professionally formatted Product Requirements Documents as Word files (`.docx`).

## Usage

Trigger with `/prd` or by describing your need:

- "Create a PRD for..."
- "Help me spec out this feature..."
- "Write product requirements for..."

Claude will ask 2–3 clarifying questions if needed, then generate the document.

## Prerequisites

```bash
npm install -g docx
```

## How It Works

1. Claude gathers context from your input (notes, docs, or a brief description)
2. Structures content into the PRD template schema
3. Runs the bundled script to produce a formatted `.docx`

```bash
node <skill-path>/scripts/generate_prd.js content.json output.docx
```

## Document Sections

Every PRD contains 13 sections: Problem Statement, Current State, Scope, Success Metrics, Flow Diagram (skipped), Basic Configurations, User Stories, Assumptions, Risks, Execution Plan, Test Cases, Open Questions, and Meeting Notes.

## Tips

- Use `[ASSUMPTION]` to flag gaps rather than leaving things vague
- Every KPI needs a baseline, target, and timeframe
- Define requirements, not implementation details

## File Structure

```
prd.skill
├── SKILL.md                   # Skill definition and Claude instructions
└── scripts/
    └── generate_prd.js        # Generates the .docx output
```
