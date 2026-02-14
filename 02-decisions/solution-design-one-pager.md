# Solution Design: [Name]

> This is not a full architecture doc. It's a one-pager that forces you to describe the simplest version first, then justify every addition. If you can't fill in the "simplest version" section, you don't understand the problem well enough yet.

| Field | Details |
|-------|---------|
| **Author** | |
| **Date** | |
| **Status** | Draft / In Review / Approved |
| **Related ADR** | ADR-[NNN] (create one if this gets approved) |

---

## The problem

_What's broken or missing? Describe the pain, not the solution. Two sentences max._



## Who has this problem and how often?

| Who | How often | Impact when it happens |
|-----|-----------|----------------------|
| | | |
| | | |

## The simplest version (v0)

_Describe the dumbest, most boring solution that could work. No new tools. No abstractions. No "future-proofing." Just solve the problem._

**Approach:**



**Tools used:** _(only things the team already has)_



**What it looks like:**

```
[Simple diagram or data flow — keep it to one line if possible]
[Source] → [simple step] → [destination]
```

**Time to deliver:**

**Limitations of this version:**
-
-

**Is v0 good enough?**
- [ ] **Yes** → Ship it. Stop here. Revisit only if the limitations actually cause problems.
- [ ] **No** → Justify below.

## Why v0 isn't enough

_Only fill this in if you checked "No" above. Be specific — "it won't scale" is not specific._

| Limitation | Concrete scenario where it fails | How likely is this scenario | When would it happen |
|-----------|--------------------------------|---------------------------|---------------------|
| | | Very likely / Likely / Unlikely | Now / 3 months / 6+ months |
| | | | |

## The proposed version (v1)

_What's the minimum you need to add to v0 to address the real limitations?_

**What's added on top of v0:**

| Addition | Why it's needed | What it costs |
|---------|----------------|--------------|
| | | |
| | | |

**What it looks like:**

```
[Diagram — should be only slightly more complex than v0]
```

**New tools or dependencies introduced:**

| Tool / Dependency | Why existing tools can't do this | Operational cost |
|------------------|--------------------------------|-----------------|
| | | |

**Time to deliver:**

## What I'm deliberately not doing

_Name the things you're tempted to add but are choosing not to. This is the most important section for someone who tends to over-engineer._

| Tempting addition | Why it's tempting | Why I'm not doing it | Revisit when |
|------------------|------------------|---------------------|-------------|
| e.g. Event-driven architecture | Feels more "modern" | Batch is fine for our volume and latency needs | Daily volume exceeds [X] or latency requirement drops below [Y] |
| e.g. Custom abstraction layer | Would make adding sources easier | We have 5 sources, not 50; the abstraction costs more than the repetition | Source count exceeds 15 |
| | | | |
| | | | |

## Risks

| Risk | Mitigation |
|------|------------|
| | |
| | |

## Review

| Reviewer | Feedback | Date |
|---------|---------|------|
| | | |
| | | |
