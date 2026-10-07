---
name: "feedback-triage"
description: "Use to turn raw customer feedback (support tickets, sales notes, NPS comments, app reviews, call notes) into tagged themes linked to the metric tree and bets. Trigger on triage this feedback, what are customers saying, sort these tickets, or synthesise this week's feedback."
---

# Skill: Feedback Triage

## Purpose
Turn a messy pile of feedback into a short list of themes the team can
act on, each linked to a segment, a metric and a bet. It started as a
Slack automation I built to triage incoming tickets so PMs weren't
reading every single one by hand. This is the same logic as a skill
anyone can run.

## When to use
- Weekly, before the Weekly Product Review
- After a launch, to see what people are actually saying
- When someone senior says "customers keep asking for X" and you want to
  know if that's true

## Inputs needed
- The raw feedback, as an export, paste, or file. More is better.
- The time window it covers

## Context first (pm-os)
Read `context/customers.md` for the segments and existing themes,
`context/bets.md` for what's in flight, and `context/glossary.md` so
themes use the team's words.

## Step-by-step process

**1. Clean it.**
Remove duplicates, spam and anything that's purely a support how-to with
no product signal. Strip personal data (names, emails, account numbers)
before doing anything else.

**2. Tag each item.**
- **Type:** bug, friction, missing capability, pricing, praise, churn
  reason
- **Segment:** from `context/customers.md`
- **Severity:** blocks them / annoys them / nice to have
- **Linked bet:** if it relates to something in flight

**3. Cluster into themes.**
Name each theme as a customer problem, not a feature request ("can't
see what they've been charged until month end", not "add a billing
page"). Count items per theme and note which segments they come from.

**4. Rank by what matters, not by volume.**
Ten loud requests from a segment we've decided not to serve rank below
three from our core segment. Check `bets.md` and the "not doing" list.

**5. Pull the best quotes.**
Two or three verbatim quotes per top theme. These go into
`context/customers.md`.

**6. Call out what's new.**
What's here this week that wasn't last week? That's usually the most
useful line in the whole output.

## Output
A short table of themes (problem, count, segments, severity, linked bet,
best quote), a "new this week" line, and any items that need someone to
act now (a serious bug, an angry key customer).

## Rules
- Never put personal data in `context/`.
- Volume is a signal, not the answer. Always weigh by segment.
- Feature requests get rewritten as problems before they're counted.

## Quality checklist
- [ ] Personal data stripped
- [ ] Every theme is phrased as a problem
- [ ] Themes linked to segments and bets
- [ ] "New this week" called out
- [ ] Urgent items flagged separately

## Hands off to
- **Weekly Product Review**: as the customer signal section
- **Discovery**: for any theme that's big and not yet understood
- **Prioritisation and Roadmap**: when a theme should change what's next
