# Complexity Check

> Run this checklist **before** committing to any technical approach. It takes 10 minutes and exists for one reason: to catch yourself before you over-engineer. Be honest — nobody sees this but you and your future self who has to maintain what you build.

## The decision

**What are you about to build / choose / implement?**



**Who asked for this?**



## The red flag questions

_Answer each one honestly. Every "yes" is a warning sign, not a blocker — but if you're hitting 4+ red flags, step back and simplify._

| # | Question | Answer | Notes |
|---|----------|--------|-------|
| 1 | Are you solving a problem that hasn't actually happened yet? | Yes / No | |
| 2 | Are you designing for a scale you don't currently have (and may never have)? | Yes / No | |
| 3 | Would you need to draw a diagram to explain this to a senior stakeholder? | Yes / No | |
| 4 | Are you introducing a new tool or technology that the team hasn't used before? | Yes / No | |
| 5 | Does this require more than one team to operate or maintain? | Yes / No | |
| 6 | Are there more than 3 components / services involved? | Yes / No | |
| 7 | Could a competent new joiner understand this in their first week? | Yes / No → worry | |
| 8 | Are you building something that an off-the-shelf tool already does? | Yes / No | |
| 9 | Is the time to first value more than 4 weeks away? | Yes / No | |
| 10 | If you had to maintain this yourself for the next 2 years, would you still build it this way? | Yes / **No → stop** | |

**Red flag count:** ___ / 10

## The simplicity test

_For each layer of complexity, justify it or remove it._

| Complexity you're adding | Why it's necessary | What happens if you don't do it | Keep it? |
|-------------------------|-------------------|-------------------------------|----------|
| e.g. Event-driven architecture | "We might need real-time later" | Batch runs every 15 minutes; users wouldn't notice | No — defer |
| e.g. Custom orchestration framework | "Airflow doesn't handle our edge case" | Small workaround in Airflow; 90% of use cases are standard | No — use Airflow |
| | | | |
| | | | |
| | | | |

## The "what if I just..." test

_Before going with your current approach, spend 5 minutes on each of these alternatives:_

**What if I just used a spreadsheet / manual process for now?**
_Could this work for the current scale? For how long?_



**What if I just used the simplest tool in the stack I already have?**
_What's the gap between "good enough now" and "perfect"?_



**What if I built the dumbest possible version first?**
_Describe the version with zero cleverness. Flat files, simple SQL, no abstraction layers. What's actually wrong with it?_



## Decision

After running through this:

- [ ] **Proceed as planned** — complexity is justified
- [ ] **Simplify** — remove [specific things] and proceed
- [ ] **Start with the simple version** — revisit when [specific trigger]
- [ ] **Rethink entirely** — the approach has too many red flags

**What I'm changing based on this check:**



---

_The goal isn't to never build complex things. It's to make sure every piece of complexity earns its place._
