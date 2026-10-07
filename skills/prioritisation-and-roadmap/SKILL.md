---
name: "prioritisation-and-roadmap"
description: "Use when deciding what to build next and turning it into a Now / Next / Later roadmap tied to metrics. Scores options with RICE or ICE, then challenges the scores. Trigger on prioritise this backlog, what should we build next, build a roadmap, or re-plan after something slipped."
---

# Skill: Prioritisation and Roadmap

## Purpose
Turn a pile of ideas, requests and opportunities into a short, defended
list of what the team does now, next and later, with the metric each item
should move. The scoring framework is the easy part. The real job is
saying no to good ideas and writing down why.

## When to use
- Planning a new quarter or cycle
- A big new request lands and something has to move to make room
- A dependency slipped and the roadmap is now fiction
- The team is busy but nobody can say which metric the work is moving

## Inputs needed
- The candidate list (backlog, opportunities from Discovery, requests
  from sales or the founder)
- Team capacity for the period, honestly estimated
- Any hard commitments already made (contracts, regulatory dates)

## Context first (pm-os)
Read `context/metrics.md`, `context/bets.md` and `context/decisions.md`
before scoring anything. Every item should map to a metric in the tree.
If it doesn't, that's the first question to ask, not a reason to give it
a low score quietly.

## Step-by-step process

**1. Clean the list.**
Merge duplicates. Rewrite anything framed as a solution ("add CSV
export") as the problem it solves ("finance teams can't reconcile without
re-keying data"). Drop anything with no plausible link to a metric, or
park it with a note.

**2. Score it, roughly.**
Use RICE when you have reach data, ICE when you don't. Keep the inputs
visible in a table so anyone can argue with a specific number rather than
the total. Confidence is the most important column and the one people
inflate most. Below 50% confidence, the item probably needs Customer
Validation before it needs a roadmap slot.

**3. Challenge the ranking.**
Look at the top five and ask:
- Is anything here only high because someone senior asked for it?
- Is there a small, boring item that unblocks three others?
- Are we stacking everything on one segment or one metric?
- What's the cost of *not* doing the number one item this cycle?
Move things if the answers say so, and note why the score was overridden.
Scores are an input to judgement, not a replacement for it.

**4. Fit it to capacity.**
Fill "Now" until capacity is used, leaving roughly 20% slack for bugs,
support and the thing nobody predicted. Most roadmaps fail because "Now"
has 130% of the team's time in it.

**5. Write Now / Next / Later / Not doing.**
Each item gets: the problem, the metric it should move, confidence, owner
and one line on why it's in that column. "Later" means we've thought
about it and it's not yet. "Not doing" means no, with a reason and a
revisit trigger.

**6. Update `context/bets.md`.**
The roadmap and the bets file should say the same thing.

## Output
A Now / Next / Later / Not doing table, the scoring table behind it, and
a short paragraph explaining the two or three hardest calls. Use the
roadmap template in `templates/roadmap-template.md`.

## Rules
- No dates on Next or Later unless there's a hard external commitment.
  Dates on uncertain work turn into promises.
- Every Now item has a metric. No exceptions.
- If you override a score, say so and say why.

## Quality checklist
- [ ] Every item framed as a problem, not a solution
- [ ] Every Now item maps to a metric in `context/metrics.md`
- [ ] Now fits inside realistic capacity with slack
- [ ] Not doing list exists, with reasons
- [ ] The hardest calls are written down, not just made

## Hands off to
- **PRD Generation**: for each Now item
- **Customer Validation**: for anything high-impact but low-confidence
- **Stakeholder Update**: to tell people what moved and why
- **Decision Log**: for any call someone's going to question later
