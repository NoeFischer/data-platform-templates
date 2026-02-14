# Data Platform Templates

A collection of ready-to-use templates for data platform projects, focused on the areas that are hardest to get right: **project management**, **product management**, and **change management**.

## Who is this for?

Data consultants and platform teams who repeatedly build data platforms and want to stop reinventing the wheel on the management and governance side.

## Repository structure

```
.
├── 01-project-management/       # Run the project
│   ├── project-charter.md           # Define scope, goals, and constraints upfront
│   ├── raci-matrix.csv              # Clarify who does what (spreadsheet)
│   ├── status-report.md             # Weekly/biweekly stakeholder update
│   ├── risk-register.csv            # Track risks, owners, and mitigations (spreadsheet)
│   └── milestone-tracker.csv        # High-level timeline with deliverables (spreadsheet)
│
├── 02-product-management/       # Shape what gets built
│   ├── platform-roadmap.md          # Phased delivery plan with outcomes
│   ├── requirements-template.md     # Capture functional & non-functional requirements
│   ├── backlog-prioritization.csv   # Score and rank work items (spreadsheet)
│   └── user-story-template.md       # Consistent story format for platform features
│
├── 03-change-management/        # Help people adopt the platform
│   ├── stakeholder-analysis.csv     # Map influence, interest, and engagement (spreadsheet)
│   ├── impact-assessment.md         # Assess change impact on teams and processes
│   ├── communication-plan.csv       # Who gets told what, when, and how (spreadsheet)
│   ├── training-plan.md             # Plan skill-building for platform users
│   └── adoption-tracker.csv         # Measure adoption over time (spreadsheet)
│
├── 04-data-platform-specific/   # Data platform essentials
│   ├── architecture-decision-record.md  # Document key technical decisions (ADR)
│   ├── data-governance-checklist.md     # Ownership, quality, security, lineage
│   ├── migration-runbook.md             # Step-by-step migration playbook
│   └── platform-design-brief.md        # One-pager to align on platform vision
│
├── 05-focus-and-scope-control/  # Keep the project on track
│   ├── scope-change-request.md      # Force a cost/benefit analysis before adding scope
│   ├── scope-change-tracker.csv     # At-a-glance log of all scope changes (spreadsheet)
│   ├── priorities-alignment-canvas.md   # Get stakeholders to agree on what matters most
│   ├── weekly-focus-check.md        # 15-minute weekly exercise to catch drift early
│   └── decision-log.csv             # Record decisions so they don't get revisited (spreadsheet)
│
└── 06-technical-decisions/      # Fight over-engineering
    ├── complexity-check.md          # 10-minute checklist: am I making this too complicated?
    ├── technology-selection-scorecard.csv  # Weighted scoring biased toward simplicity (spreadsheet)
    ├── build-vs-buy.md              # Structured analysis — default answer is "buy"
    └── solution-design-one-pager.md # Describe the simplest version first, then justify additions
```

## How to use these templates

1. **Start a new engagement** — Copy the repo or the folders you need into your project workspace.
2. **Fill in the charter first** — `01-project-management/project-charter.md` sets the foundation. Do this before anything else.
3. **Pick what you need** — Not every project needs every template. A small project might only need the charter, RACI, and a roadmap. A large enterprise migration might use all of them.
4. **CSV files open in any spreadsheet tool** — The `.csv` files are designed to be opened in Excel, Google Sheets, or Numbers. They include headers and example rows you can delete.
5. **Adapt freely** — These are starting points, not rigid forms. Add columns, remove sections, rename things.

## Suggested workflow by project phase

| Phase | Key templates |
|-------|--------------|
| **Discovery / Scoping** | Project charter, Platform design brief, Stakeholder analysis, **Priorities alignment canvas** |
| **Planning** | Roadmap, RACI, Requirements, Risk register, Communication plan, **Technology selection scorecard** |
| **Design** | **Solution design one-pager, Complexity check, Build vs. buy**, ADRs |
| **Build** | User stories, Backlog prioritization, Status reports, **Weekly focus check** |
| **Migration / Rollout** | Migration runbook, Impact assessment, Training plan, Milestone tracker |
| **Adoption / Steady state** | Adoption tracker, Data governance checklist |
| **Ongoing (all phases)** | **Decision log, Scope change request, Scope change tracker** |

## Format choices

- **Markdown** (`.md`) — for narrative documents, checklists, and anything that benefits from prose and structure. Works well in Git, wikis, and Notion.
- **CSV** (`.csv`) — for tabular data like registers, trackers, and matrices. Opens directly in spreadsheet tools where filtering and sorting are useful.

## Keeping the project on track

Projects derail gradually, not suddenly. The `05-focus-and-scope-control/` folder exists specifically to fight the three most common failure modes:

1. **Scope creep** — The scope change request forces a cost/benefit analysis. The key question: "if we do this, what do we *not* do?" If nobody can answer that, the request shouldn't be approved.
2. **Priority misalignment** — Stakeholders often think they agree on priorities but actually don't. The priorities alignment canvas makes this visible early, before it causes months of building the wrong thing.
3. **Gradual drift** — The weekly focus check is a 15-minute habit that catches drift before it compounds. If you keep rolling the same priorities forward week after week, something structural is broken.

The decision log is the glue. Decisions made verbally in meetings get forgotten or relitigated. Write them down. When someone asks "why did we do X?", point them to the log instead of reopening the debate.

## Fighting over-engineering

The `06-technical-decisions/` folder exists because the most expensive mistakes in data platforms aren't picking the wrong tool — they're building too much. These templates are intentionally biased toward simplicity:

- **Complexity check** — 10 red-flag questions to ask yourself before committing to any approach. Includes a "what if I just..." exercise that forces you to consider the boring solution before the clever one.
- **Technology selection scorecard** — Weighted scoring where "time to value" and "simplicity of operation" have the highest weights, and "scalability" is deliberately low. Adjustable, but you have to justify changing the weights.
- **Build vs. buy** — The default answer is "buy." You have to make a strong, specific case to justify building. Includes the hidden costs people always forget (maintenance, documentation, onboarding new people).
- **Solution design one-pager** — Starts with "describe the dumbest possible version" (v0). You can only add complexity by showing a concrete scenario where v0 fails. Has a "what I'm deliberately not doing" section — the most important part for someone who tends to over-engineer.

## Tips from experience

- The **project charter** is the single most valuable document. If the client won't align on scope and success criteria upfront, everything downstream suffers.
- **RACI confusion** causes more delays than technical problems. Fill it in early, review it with stakeholders, and update it when roles shift.
- **Change management is not optional.** The best-architected platform fails if people don't use it. Budget real time for communication, training, and feedback loops.
- **ADRs compound in value.** Six months in, nobody remembers why you picked Snowflake over Databricks. Write it down when the decision is fresh.
- **"Not now" is more useful than "no."** Most scope change requests aren't bad ideas — they're just badly timed. Defer them explicitly so they don't sneak back in.
- **Run the weekly focus check even when things feel fine.** Especially when things feel fine. That's when drift is hardest to notice.
- **Always describe the boring solution first.** If you can't explain what's wrong with the simple version, you don't need the complex one. The solution design one-pager enforces this.
- **"We might need it later" is not a reason to build it now.** Write down the trigger condition that would justify it, and revisit when that trigger actually fires.
