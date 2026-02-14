# Data Platform Templates

A curated set of templates for data platform consulting. Organized around how you actually work: joining a project, making decisions, delivering, and getting better over time.

## Who is this for?

A consultant or engineer who joins data platform projects — often mid-flight, often not as the lead — and wants a small set of tools that work even if nobody else on the team uses them.

## What's in here (and what's not)

21 templates in 4 folders. That's it. No status report templates (that's the PM's job), no backlog CSVs (that's what Jira is for), no communication plans (that's a change management lead's deliverable). Everything here is something you can use yourself, regardless of your role on the project.

## Repository structure

```
.
├── 01-joining-and-alignment/       # When you arrive
│   ├── engagement-kickoff-checklist.md  # First 2 weeks: what to do, who to meet, what to ask
│   ├── situation-assessment.md          # Your "fresh eyes" findings after week 1-2
│   ├── stakeholder-map.csv             # Who matters, what they care about, how to engage them
│   └── priorities-alignment-canvas.md  # Force stakeholders to agree on what matters most
│
├── 02-decisions/                    # When you decide
│   ├── architecture-decision-record.md  # Document the "why" behind key technical choices
│   ├── decision-log.csv                 # Every decision, written down so it doesn't get relitigated
│   ├── complexity-check.md              # 10-minute gut check: am I making this too complicated?
│   ├── solution-design-one-pager.md     # Describe the boring version first, then justify additions
│   ├── build-vs-buy.md                  # Default answer is "buy" — make the case otherwise
│   └── technology-selection-scorecard.csv  # Weighted scoring biased toward simplicity
│
├── 03-delivery/                     # When you build
│   ├── project-charter.md              # Scope, goals, constraints — or a diagnostic if one doesn't exist
│   ├── raci-matrix.csv                 # Who does what (open in a spreadsheet)
│   ├── risk-register.csv               # Track risks before they become problems (spreadsheet)
│   ├── scope-change-request.md         # Force a cost/benefit analysis before adding scope
│   ├── migration-runbook.md            # Step-by-step migration playbook
│   └── data-governance-checklist.md    # Ownership, quality, security, lineage
│
└── 04-personal-effectiveness/       # Your private toolkit
    ├── where-to-focus.md                # Monday thinking tool: where does my time create the most impact?
    ├── meeting-prep.md                  # 5-minute prep before any meeting that matters
    ├── personal-weekly-retro.md         # Friday reflection: how you worked, not just what
    ├── lessons-learned-log.csv          # Cross-engagement pattern library (spreadsheet)
    └── engagement-close-out.md          # End well: handover, relationships, learning
```

## How to use these

1. **When you start a new engagement** — Work through `01-joining-and-alignment/engagement-kickoff-checklist.md`. It's written for the common case: you're joining a project already in motion.
2. **After your first 1-2 weeks** — Write your `situation-assessment.md`. Share it with your sponsor. This is the highest-value thing you can produce early.
3. **Pick what you need from 02 and 03** — Not every engagement needs every template. A short engagement might only need ADRs and the decision log. A large migration might use everything in `03-delivery/`.
4. **04-personal-effectiveness stays with you** — These tools follow you across engagements. The lessons learned log and weekly retro are career assets, not project artifacts.
5. **CSV files open in any spreadsheet tool** — The `.csv` files are designed for Excel, Google Sheets, or Numbers. They include example rows you can delete.
6. **Adapt freely** — These are starting points, not rigid forms.

## The three tiers of use

You don't need to be the project lead to get value from these. Think of them in tiers:

| Tier | How you use it | Templates |
|------|---------------|-----------|
| **Use privately** | Nobody needs to know | Stakeholder map, decision log, weekly retro, where to focus, lessons log, meeting prep, complexity check, situation assessment |
| **Suggest when you see a gap** | "I noticed we don't have this — want me to set it up?" | ADRs, risk register, scope change process |
| **Propose if you're leading** | Requires buy-in from the team | Project charter, RACI, priorities alignment canvas |

The private tier is where most of the value is. The best consultants aren't the ones who introduce new processes — they're the ones who understand the project better than anyone because they wrote things down.

## What was cut (and why)

This repo used to have 30 templates in 7 folders. Here's what got removed and the reasoning:

- **Status reports, milestone trackers** — PM artifacts. If you need them, your PM tool has them.
- **Roadmaps, backlog prioritization, user stories** — Product management artifacts that live in the team's ticketing system. A CSV backlog alongside Jira is a recipe for drift.
- **Impact assessments, communication plans, training plans, adoption trackers** — Change management deliverables. If you're hired to do change management, build these from scratch for the specific context. Generic templates for these do more harm than good.
- **Platform design brief** — Overlapped with the solution design one-pager, which is better.
- **Scope change tracker** — The decision log already captures this.
- **Weekly focus check** — Folded into the personal weekly retro (the "Am I working on what matters?" section).

The principle: if a template requires a specific role to be useful, or if it duplicates something that lives in a better tool, cut it.

## The decision tools

The `02-decisions/` folder is intentionally biased toward simplicity. These templates exist because the most expensive mistakes in data platforms aren't picking the wrong tool — they're building too much.

- **Complexity check** — 10 red-flag questions before committing to any approach. Includes the "what if I just..." exercise: describe the boring solution before the clever one.
- **Solution design one-pager** — Starts with "describe the dumbest possible version" (v0). You can only add complexity by showing a concrete scenario where v0 fails.
- **Build vs. buy** — The default answer is "buy." You have to make a strong, specific case to justify building. Includes the hidden costs everyone forgets.
- **Technology selection scorecard** — Weighted scoring where "time to value" and "simplicity of operation" are weighted highest, "scalability" is deliberately low.

## Tips from experience

- The **project charter** is the most valuable document — even when one already exists. Read it. If it doesn't match reality, that's your first finding.
- **RACI confusion** causes more delays than technical problems. If decisions are stalling, the RACI is wrong (or missing).
- **ADRs compound in value.** Six months in, nobody remembers why you picked Snowflake over Databricks. Write it down when the decision is fresh.
- **"Not now" is more useful than "no."** Most scope requests aren't bad ideas — they're badly timed. Defer explicitly.
- **Always describe the boring solution first.** If you can't explain what's wrong with the simple version, you don't need the complex one.
- **"We might need it later" is not a reason to build it now.** Write down the trigger condition that would justify it, and revisit when that trigger actually fires.
- **Your personal weekly retro is the highest-ROI habit in this entire repo.** 15 minutes on Friday. Non-negotiable. It's how you get better over time instead of just getting busier.
- **Monday: where to focus. Friday: how did I do.** These two bookend your week. The focus tool points you forward, the retro looks back. Together they create a feedback loop that compounds.
- **The situation assessment is your first deliverable.** It earns trust, demonstrates judgment, and forces you to synthesize everything you've learned. Don't skip it.
