# Build vs. Buy Decision: [Capability Name]

> The default answer should be **buy** (or use an existing tool). Building is almost always more expensive than it looks. This template is intentionally biased toward buying — you have to make a strong case to justify building.

| Field | Details |
|-------|---------|
| **Decision** | |
| **Date** | |
| **Capability needed** | |
| **Decision maker** | |

---

## 1. What do you need?

_Describe the capability in terms of the outcome, not the solution. Don't say "we need a custom ingestion framework" — say "we need to reliably move data from 8 source systems into the warehouse daily."_

**Outcome needed:**



**Who uses it:**



**How critical is it:** Core to the platform / Important but not core / Nice to have

## 2. Can you buy it?

_List existing tools, services, or platforms that could do this. Include tools you already have._

| Option | Cost (annual) | Covers what % of the need | What's missing | Effort to adopt |
|--------|-------------|--------------------------|---------------|----------------|
| | | | | |
| | | | | |
| | | | | |

**Is anything already in the org's tech stack that does this?**



## 3. What would building look like?

_Be brutally realistic. Include the costs people usually forget._

| Cost category | Estimate | Notes |
|--------------|----------|-------|
| Initial build time | ___ person-weeks | |
| Ongoing maintenance | ___ person-hours / month | Bugs, upgrades, compatibility |
| Documentation | ___ person-days | Someone has to write it |
| Onboarding new team members | ___ days per person | Custom tools have no Stack Overflow |
| Testing and QA | ___ person-days | |
| Opportunity cost | | What else could the team build instead? |
| **Total first-year cost** | | Be honest |

## 4. The hard questions

| Question | Answer |
|----------|--------|
| Are you building because it's genuinely better, or because it's more interesting? | |
| If the person who builds this leaves, can the team maintain it? | |
| Have you gotten a demo of the buy option, or are you assuming it can't do what you need? | |
| Is the gap between "what the tool does" and "what we need" really worth building for? | |
| Will this custom solution still be the right choice in 2 years? | |

## 5. The 80/20 question

_Most buy options cover 80% of what you need. The question is whether the remaining 20% is worth the full cost of building._

**What the buy option covers:**
-
-
-

**What's in the 20% gap:**
-
-

**Is the 20% gap critical to the business outcome, or is it a preference?**



## 6. Decision

| Option | Recommendation |
|--------|---------------|
| **Buy** | Use [tool]. Accept the 20% gap or work around it. |
| **Build** | Build [what], because [specific justification]. |
| **Buy + extend** | Use [tool] and build a thin layer on top for [specific gap]. |
| **Defer** | We don't need this yet. Revisit when [trigger]. |

**Decision:**

**Rationale:**



---

_If you chose to build: create an ADR documenting the decision. Set a calendar reminder for 6 months to reassess whether the build is delivering the expected value._
