---
name: "discovery"
description: "Use when turning a vague signal (an exec ask, a support trend, a competitor move, a gut feeling) into a scoped, evidence-backed opportunity worth sizing and validating. Trigger on requests like scope this opportunity, what's actually going on here, or is this worth pursuing."
---

# Skill: Discovery

## Purpose
Turn a vague signal (an exec ask, a support trend, a sales objection, a
gut feeling, a competitor move) into a scoped, evidence-backed
opportunity worth sizing and validating. Discovery is where most PMs
either waste months chasing the wrong thing, or skip straight to
solutions. This skill forces the "what's actually going on" step first.

## When to use
- You've been handed a one-line brief ("we need to reduce churn",
  "look into X competitor feature") and need to turn it into something
  actionable
- A metric moved and you don't know why yet
- You're kicking off a new quarter/cycle and need a fresh opportunity
  backlog
- Someone has jumped straight to a solution and you need to pressure-test
  whether it solves a real problem

## Inputs needed
- The raw signal (verbatim ask, ticket, metric chart, quote, whatever
  triggered this)
- Access to whatever evidence exists already: analytics, support
  tickets, sales call notes, past research, churn/NPS data
- Company/strategy context (North Star, current bets, what's explicitly
  out of scope this cycle)
- Known constraints: timeline, team capacity, regulatory/compliance
  boundaries (relevant in fintech/payments)

## Context first (pm-os)
Before starting, read whatever exists in `context/` (product, customers,
metrics, bets, decisions, glossary). Don't ask for anything that's already
written down there, and use the glossary's terms. When you finish, list
anything this work changed (a new decision, a sharper customer insight, a
metric definition) and offer to write it back to the right file in
`context/`. That loop is what keeps the system current.

## Step-by-step process

**1. Restate the signal as a question, not a solution.**
"Add a dark mode toggle" becomes "why are users asking for this, and
what job is it actually serving?" If the input already arrived as a
solution, this is the single most important re-framing step. Do not
skip it even under time pressure.

**2. Build (or update) an Opportunity Solution Tree.**
Desired outcome at the top → opportunities (customer needs, pain
points, desires, in the customer's language, not yours) as branches →
candidate solutions only at the leaves. This is what
stops the org from debating solutions before agreeing on the problem.

**3. Pull existing evidence before generating new evidence.**
Check analytics, support tickets, past research, sales notes, churn
reasons. Look for convergence across at least two independent sources
(e.g., a support trend *and* a churn survey theme) before treating a
pattern as real. Note explicitly what's assumption vs. what's evidenced.

**4. Apply a Jobs-to-be-Done lens.**
For the strongest 2-4 opportunities, write the job story: "When
[situation], I want to [motivation], so I can [expected outcome]." This
keeps the opportunity anchored to a real context rather than a feature
wish.

**5. Score and shortlist opportunities.**
Use a lightweight framework, RICE or ICE, to rank opportunities relative to each other. At this stage the scoring
inputs are directional, not precise; the point is relative ordering,
not false precision.

**6. Flag what's still unknown.**
Every opportunity should leave with an explicit "what would change our
mind" list: the assumptions that, if wrong, kill the opportunity. This
feeds directly into customer validation.

**7. Write the discovery brief.**
Keep it to one page. This
is a decision document, not a research report. Its job is to get a
"yes, size it" / "no, park it" / "need more evidence" decision.

## Output
A completed discovery brief containing: the reframed
problem statement, the opportunity solution tree (or top branches),
evidence summary with sourcing, job story, riskiest assumptions, and a
recommendation on next step.

## Quality checklist
- [ ] The problem is stated as a customer need, not a feature
- [ ] At least two independent evidence sources support the top
      opportunity, or the gap is explicitly flagged
- [ ] Solutions are NOT decided yet: only opportunities
- [ ] The riskiest assumption is named explicitly, not buried in prose
- [ ] A named person can read the brief and make a go/no-go/more-evidence
      call in under 5 minutes

## Common failure modes to catch
- **Solution creep**: language like "we should build" appearing before
  the opportunity is validated, flag and strip it back to the need
- **Single-source conviction**: one loud customer or one exec anecdote
  driving the whole brief
- **Scope inflation**: trying to solve every branch of the tree at once
  instead of picking the highest-leverage one

## Hands off to
- **Market Sizing**: once an opportunity is scoped, size it before
  investing further
- **Customer Validation**: the riskiest assumptions list becomes the
  validation plan's test list directly
- **PRD Generation or Prioritisation and Roadmap**: a validated, sized
  opportunity is what those skills expect as input
