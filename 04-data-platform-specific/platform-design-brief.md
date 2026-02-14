# Platform Design Brief: [Project Name]

> A one-page-ish document to align everyone on what we're building and why, before diving into detailed design. Share this early and get sign-off before committing to architecture decisions.

## The problem

_In 2-3 sentences: what's broken or missing today? What is the cost of not acting?_



## The vision

_In 1-2 sentences: what does the world look like when this platform is in place?_



## Who it's for

| User group | What they need from the platform | How they'll interact with it |
|-----------|--------------------------------|----------------------------|
| | | |
| | | |
| | | |

## Key use cases

_The top 3-5 things this platform must enable. If it doesn't do these, it has failed._

1.
2.
3.
4.
5.

## Design principles

_Guardrails that shape every decision. When in doubt, refer to these._

| Principle | What it means in practice |
|-----------|--------------------------|
| e.g. **Single source of truth** | One authoritative version of each metric; no duplicate pipelines |
| e.g. **Self-service first** | Business users can answer 80% of questions without filing a ticket |
| e.g. **Built for change** | Schema evolution, new sources, and new use cases are easy to add |
| | |

## High-level architecture

_A simple diagram or description of the main components. Keep it conceptual, not product-specific._

```
[Sources] → [Ingestion] → [Storage / Warehouse] → [Transformation] → [Serving / BI]
                                    ↕
                          [Governance / Catalog]
                          [Orchestration / Monitoring]
```

| Layer | Purpose | Likely approach / tool |
|-------|---------|----------------------|
| Ingestion | Extract from source systems | |
| Storage | Land and store raw + processed data | |
| Transformation | Business logic, cleaning, modeling | |
| Serving | Expose data to consumers | |
| Orchestration | Schedule and monitor workflows | |
| Governance | Catalog, quality, lineage, access | |

## What's in and out for v1

| In scope (v1) | Out of scope (v1, consider later) |
|---------------|----------------------------------|
| | |
| | |
| | |

## Known constraints

-
-
-

## Open questions

| Question | Impact | Owner | Target date for answer |
|----------|--------|-------|----------------------|
| | | | |
| | | | |

## Approvals

| Name | Role | Alignment | Date |
|------|------|-----------|------|
| | Sponsor | | |
| | Technical lead | | |
| | Product owner | | |
