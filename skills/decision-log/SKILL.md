---
name: "decision-log"
description: "Use whenever a product decision is made that someone might question later. Captures the decision, options considered, reasoning, and what would make us revisit it, then writes it to context/decisions.md. Trigger on log this decision, we decided, write this down, or why did we decide X."
---

# Skill: Decision Log

## Purpose
Stop the team re-arguing the same decision every few months, and give
anyone who joins later the reasoning behind the product as it is. In a
startup, the decision log is the closest thing to institutional memory.
It's also the single most useful file for onboarding a new PM or
engineer.

## When to use
- Straight after a meeting where something was decided
- When someone asks "why do we do it like this?" and the answer only
  lives in one person's head
- When a decision is reversed (log the reversal, don't edit the original)

## Inputs needed
- What was decided, and roughly why
- Who was in the room

## Context first (pm-os)
Read `context/decisions.md` to check this isn't already logged, or
doesn't contradict something that is. If it contradicts an earlier
decision, say so and log it as a reversal that links to the original.

## Step-by-step process

**1. Get the decision in one sentence.**
If it takes three, it might be two decisions.

**2. Ask for the options.**
At least two, including "do nothing". If only one option was considered,
note that honestly. It's useful to know later.

**3. Get the real reason.**
Push past "it's the best option". What trade-off did we accept? What did
we give up?

**4. Set a revisit trigger.**
A metric threshold, a date, or an event ("if churn in segment B goes
above 5%", "after the pricing test reads out"). Decisions without
triggers never get revisited, even when they should.

**5. Mark reversibility.**
Cheap to reverse, costly to reverse, or one-way door. One-way doors
deserve more scrutiny before they're made, so if this one wasn't
scrutinised, say so.

**6. Write it to the top of `context/decisions.md`.**

## Output
A new entry at the top of `context/decisions.md` in the standard format.

## Rules
- Never edit an old decision. Add a new one that reverses or updates it.
- Log the reasoning as it was at the time, even if it looks wrong now.
- Roles, not names, if the repo is shared beyond the team.

## Quality checklist
- [ ] One-sentence decision
- [ ] At least two options listed
- [ ] The trade-off is named
- [ ] Revisit trigger is specific
- [ ] Reversibility marked

## Hands off to
- **Stakeholder Update**: if people outside the room need to know
- **Prioritisation and Roadmap**: if the decision moves a bet
