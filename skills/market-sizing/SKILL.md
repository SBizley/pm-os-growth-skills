---
name: "market-sizing"
description: "Use when estimating whether an opportunity is big enough to justify investment. Produces a TAM/SAM/SOM view plus a bottom-up impact estimate. Trigger on requests like size this market, how big is this opportunity, or TAM/SAM/SOM for X."
---

# Skill: Market Sizing

## Purpose
Answer "is this big enough to matter" with a number you can defend in
front of a CFO or exec team, not a vibe. Produces a TAM/SAM/SOM view
plus an impact-sizing estimate for a specific opportunity, using both
top-down and bottom-up methods so one can sanity-check the other.

## When to use
- Deciding whether an opportunity from Discovery is worth resourcing
- Quarterly/annual planning, ranking opportunities against each other
- Building a business case for a new bet, especially where you own
  commercial/P&L framing (pricing, monetisation impact)
- An exec asks "how big is this, really?" and a gut-feel answer won't
  survive the room

## Inputs needed
- The scoped opportunity from Discovery (problem, target segment, job
  story)
- Whatever internal data exists: current user/customer counts, ARPU or
  average transaction value, conversion rates, existing segment
  penetration
- External data: industry reports, competitor disclosures, analyst
  estimates, census/demographic data, published market sizing studies. Cite sources, don't invent figures
- The metric that actually matters for the business case (ARR, take
  rate, transaction volume, activation rate, whatever ties to the P&L
  you're arguing in front of)

## Context first (pm-os)
Before starting, read whatever exists in `context/` (product, customers,
metrics, bets, decisions, glossary). Don't ask for anything that's already
written down there, and use the glossary's terms. When you finish, list
anything this work changed (a new decision, a sharper customer insight, a
metric definition) and offer to write it back to the right file in
`context/`. That loop is what keeps the system current.

## Step-by-step process

**1. Define the addressable unit precisely.**
Before any maths: who exactly is in scope? "SMB merchants" is not
precise enough, "SMB merchants in the UK processing £10k-£500k/month
in card-not-present transactions" is. Precision here is what makes the
rest of the sizing defensible.

**2. Top-down: TAM → SAM → SOM.**
- **TAM** (Total Addressable Market): the full revenue opportunity if
  you captured 100% of the relevant market globally/in-scope-geo
- **SAM** (Serviceable Addressable Market): the slice you could
  realistically serve given your product, geography, and business model
  constraints today
- **SOM** (Serviceable Obtainable Market): what you could realistically
  capture in a defined time horizon (usually 1-3 years) given
  competition, GTM capacity, and realistic penetration rates

State the formula and every input explicitly, e.g.:
`TAM = (# of UK SMB merchants) × (avg annual card-not-present volume) × (take rate)`
Every number in that formula needs a source or an explicit assumption
flag.

**3. Bottom-up: build it from unit economics.**
Independently estimate using what you actually know: current
conversion funnel, existing customer ARPU/take rate, addressable
segment size in your own data. Bottom-up is usually more defensible
than top-down because it's grounded in real unit economics rather than
industry-report multipliers.

**4. Triangulate.**
Top-down and bottom-up should land in the same order of magnitude. If
they're off by 10x, that's a signal. Find out which assumption is
wrong before presenting either number. Present both, with the gap
explained, rather than picking the more flattering one.

**5. Size the specific opportunity's impact, not just the market.**
Market size answers "is this space big enough." A driver tree answers
"what would THIS opportunity actually move." Break the target metric
into its drivers (e.g., Revenue = Users × Activation Rate × ARPU ×
Retention) and estimate which driver(s) the opportunity affects and by
how much, using comparable benchmarks or pilot data where available.

**6. Stress-test with a range, not a point estimate.**
Give conservative / expected / optimistic scenarios. A single number
invites false precision and is easy to pick apart; a range with stated
assumptions per scenario is more credible and survives scrutiny better.

**7. Write the sizing doc.**
Lead with the range and the
recommendation, then show the maths. Don't bury the answer under the
methodology.

## Output
A sizing document with: precise addressable-unit definition, TAM/SAM/SOM
(top-down), bottom-up cross-check, driver tree impact estimate,
conservative/expected/optimistic range, sourced assumptions list, and a
one-line recommendation.

## Quality checklist
- [ ] Every number traces to a source or is explicitly flagged as an
      assumption
- [ ] Top-down and bottom-up are both shown, with any gap explained
- [ ] The addressable unit is precise enough that someone else could
      reproduce the calculation
- [ ] A range is given, not a single point estimate
- [ ] The sizing ties to a metric the business actually tracks (not a
      vanity number)

## Common failure modes to catch
- Using a headline "global market size" figure lifted from a report
  without adjusting for your actual SAM
- Point estimates presented with false confidence
- Sizing the market instead of sizing the opportunity's specific impact
- No source trail: numbers that can't survive "where did that come
  from?"

## Hands off to
- **Prioritisation and Roadmap**: sized opportunities are
  what gets ranked and slotted
- **Customer Validation**: if sizing looks promising but confidence in
  the underlying assumptions is low, validate before committing resource
- **Experimentation**: the driver-tree impact estimate becomes the
  hypothesis an experiment is designed to test
