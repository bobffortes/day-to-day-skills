# Day-to-Day Skills

A personal library of reusable research and decision-making skills, written as
plain Markdown "prompt playbooks." Each file is self-contained: copy it into
any AI agent, browser assistant, or workflow tool to apply the same standard
of rigor across projects — investing, travel planning, vendor research, or
any other web-based lookup task.

## Why this exists

Most research tasks — whether picking a stock, planning a trip, or choosing a
supplier — follow the same underlying loop:

```
Clarify -> Research -> Verify -> Compare -> Recommend -> Review
```

Instead of re-inventing that loop every time, this repo captures it once as a
set of general-purpose skills, plus domain packs that add the fields and
checks specific to a given context.

## Folder structure

| Folder | Purpose |
|---|---|
| [`general-skills/`](./general-skills) | Context-agnostic skills used in every project: research planning, source verification, structured extraction, comparison/scoring, and final QA. Skills only — no agent here, since it's meant to be reused inside every domain agent below. |
| [`finance-skills/`](./finance-skills) | Investment and financial research: company/sector analysis, valuation context, bull/bear cases, evidence logging, plus the **Investment Research Agent**. |
| [`tourism-skills/`](./tourism-skills) | Travel and itinerary research: destination discovery, comparison of transport/lodging, visa and safety checks, plus the **Travel Planning Agent**. |
| [`commercial-skills/`](./commercial-skills) | Vendor, supplier, and general commercial/product research and decision support, plus the **Vendor & Commercial Research Agent**. |

## Skills vs. agents

- **Skill files** (e.g. `research-planner.md`, `investment-research.md`) are
  static prompt templates — copy/paste instructions with no autonomy of
  their own.
- **Agent files** (e.g. `investment-research-agent.md`) describe an
  autonomous, tool-using role built on top of one or more skill files: they
  plan, search, extract, verify, compare, and loop on their own, only
  pausing for human approval before any real-world action (booking, buying,
  trading, contacting a third party, publishing).
- Each domain folder (finance, tourism, commercial) has exactly one agent
  file that orchestrates that domain's skill plus the shared
  `general-skills/`. `general-skills/` intentionally has no agent of its
  own — it's the shared toolbox every domain agent calls into.

## How to use a skill file

1. Open the relevant `.md` file.
2. Copy the prompt block (the section in the fenced code box) into your AI
   agent or assistant as a system/instruction message.
3. Fill in the bracketed placeholders (e.g. `[COMPANY / TICKER / SECTOR]`)
   with your specific request.
4. Always run the `general-skills/qa-fact-check-gate.md` skill before
   finalizing any deliverable that will be acted upon.

## Core principle: research vs. action

These skills are designed for **research and analysis only**. None of them
should be used to autonomously execute a booking, purchase, trade, account
change, or message without explicit human review and approval first.

## Adding a new skill

- Put context-agnostic skills (usable in any domain) in `general-skills/`.
- Put skills specific to one domain in that domain's folder. If a new domain
  doesn't exist yet, create a new top-level folder named `<domain>-skills/`.
- Keep each skill to one file, one clear purpose, and a ready-to-copy prompt
  block.
