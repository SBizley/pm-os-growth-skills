---
name: "weekly-product-review"
description: "Use to run a weekly product review: metrics against the tree, bets status, new customer signal, decisions needed. Also keeps context/ up to date. Trigger on weekly product review, run our product review, prep the Monday metrics session, or what changed this week."
---

# Skill: Weekly Product Review

## Purpose
The ritual that keeps a small product team honest and keeps `context/`
from going stale. Thirty minutes a week: look at the numbers, check the
bets, hear what customers said, make the decisions that are waiting. It's
also the thing I'd set up first as a product ops or chief of staff hire,
because almost everything else hangs off it.

## When to use
- Same time every week, ideally Monday
- As a one-off to get a new team into a rhythm

## Inputs needed
- This week's numbers for the metrics in `context/metrics.md`
- Anything new from customers (tickets, calls, interviews, churn
  reasons). The Feedback Triage skill's output is ideal.
- Status from whoever owns each bet

## Context first (pm-os)
Read all of `context/`. This skill is the one that most often writes
back to it.

## Step-by-step process

**1. Build the pre-read (before the meeting).**
One page:
- North star and input metrics: this week, last week, four-week trend,
  target. Flag anything that moved more than you'd expect.
- Guardrails: anything near its threshold
- Bets: On track / At risk / Off track, one line each
- Customer signal: the three most important things heard this week, with
  quotes
- Decisions needed: what's waiting, who owns it, by when

**2. Ask "why" on anything surprising.**
For each unexpected metric movement, write the most likely explanation
and how confident you are. "We don't know yet" is a fine answer. Making
something up isn't.

**3. Run the meeting (30 minutes).**
Numbers (10 min), bets (10 min), decisions (10 min). Customer signal gets
woven in wherever it's relevant. Don't let it become a status round where
everyone reads their update aloud.

**4. Write back.**
- Update `context/metrics.md` baselines if they've meaningfully shifted
- Update bet statuses in `context/bets.md`
- Log any decisions with the Decision Log skill
- Add strong new quotes to `context/customers.md`

## Output
A one-page pre-read before the meeting, and updated `context/` files plus
a short list of actions after it. Template:
`templates/weekly-review-template.md`.

## Rules
- Pre-read goes out before the meeting, not in it.
- If a bet has been At risk three weeks running, it needs a decision, not
  another status.
- Fewer metrics is better. If nobody acts on a number, take it off.

## Quality checklist
- [ ] Every metric has a comparison and a trend
- [ ] Every surprise has an explanation and a confidence level
- [ ] Every decision has an owner and a date
- [ ] `context/` updated afterwards

## Hands off to
- **Decision Log**: for anything decided
- **Discovery**: for anything surprising that nobody can explain
- **Stakeholder Update**: the review is most of the founder update already
