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
└── 04-data-platform-specific/   # Data platform essentials
    ├── architecture-decision-record.md  # Document key technical decisions (ADR)
    ├── data-governance-checklist.md     # Ownership, quality, security, lineage
    ├── migration-runbook.md             # Step-by-step migration playbook
    └── platform-design-brief.md        # One-pager to align on platform vision
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
| **Discovery / Scoping** | Project charter, Platform design brief, Stakeholder analysis |
| **Planning** | Roadmap, RACI, Requirements, Risk register, Communication plan |
| **Build** | User stories, Backlog prioritization, ADRs, Status reports |
| **Migration / Rollout** | Migration runbook, Impact assessment, Training plan, Milestone tracker |
| **Adoption / Steady state** | Adoption tracker, Data governance checklist |

## Format choices

- **Markdown** (`.md`) — for narrative documents, checklists, and anything that benefits from prose and structure. Works well in Git, wikis, and Notion.
- **CSV** (`.csv`) — for tabular data like registers, trackers, and matrices. Opens directly in spreadsheet tools where filtering and sorting are useful.

## Tips from experience

- The **project charter** is the single most valuable document. If the client won't align on scope and success criteria upfront, everything downstream suffers.
- **RACI confusion** causes more delays than technical problems. Fill it in early, review it with stakeholders, and update it when roles shift.
- **Change management is not optional.** The best-architected platform fails if people don't use it. Budget real time for communication, training, and feedback loops.
- **ADRs compound in value.** Six months in, nobody remembers why you picked Snowflake over Databricks. Write it down when the decision is fresh.
