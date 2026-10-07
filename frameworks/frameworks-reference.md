# Frameworks Reference

Companion doc for the discovery / market-sizing / customer-validation /
prototyping / experimentation skills. This is a "how it works" reference. The skills tell you *when* to reach for each one.

## Opportunity Solution Tree
Structure: **Desired Outcome** (a business metric you're trying to move)
at the top → **Opportunities** (customer needs, pain points, desires, in the customer's language) as the branch layer → **Solutions** only at
the leaves, and only after opportunities are prioritised.
Rule of thumb: if you're debating solutions before the opportunity
layer is agreed, stop and go back up the tree.

## Jobs-to-be-Done (JTBD)
People "hire" a product to make progress in a specific situation.
Format for a job story: *"When [situation], I want to [motivation], so
I can [expected outcome]."* Stronger than a persona-based user story
because it's anchored to context and causality, not demographics.
Use JTBD interviews (the "switch" interview) to uncover the job behind
a purchase/adoption/churn decision: walk through the timeline from
first thought of a solution to the moment of choosing (or leaving) one.

## TAM / SAM / SOM
- **TAM**: Total Addressable Market: full revenue opportunity at 100%
  penetration of the relevant market
- **SAM**: Serviceable Addressable Market: the slice reachable given
  your business model, geography, and product today
- **SOM**: Serviceable Obtainable Market: realistically capturable
  share within a defined time horizon given competition and GTM capacity
Always build both **top-down** (market-report driven) and **bottom-up**
(unit-economics driven) versions and triangulate, see the Market
Sizing skill for the full method.

## Prioritisation scoring: ICE vs RICE
- **ICE** = Impact × Confidence × Ease (simple, fast, good for early
  directional ranking)
- **RICE** = (Reach × Impact × Confidence) / Effort (adds a Reach term,
  better once you have real usage data to estimate reach)
Use ICE early in Discovery when data is thin; move to RICE once
opportunities are sized and reach is estimable.

## Riskiest Assumption Test (RAT)
For any opportunity or solution, list every assumption it depends on,
then identify the one that, if false, invalidates everything else.
Test that one first, cheaply, before investing further. This is what
turns a Discovery brief's "what's still unknown" section into an
actionable validation plan.

## Lean Startup: Build-Measure-Learn
Minimize the loop, not the build: the goal is the fastest possible
cycle through building the smallest testable thing, measuring real
behaviour, and learning, not minimizing product scope for its own
sake. Pairs directly with the Prototyping skill's fidelity-matching
step and the Experimentation skill's MDE/duration discipline.

## Pirate Metrics (AARRR)
**A**cquisition → **A**ctivation → **R**etention → **R**eferral →
**R**evenue. Useful as a checklist when scoping which stage of the
funnel an opportunity or experiment actually targets, many proposed
"growth" ideas turn out to target the wrong stage for the stated goal
(e.g. an acquisition tactic proposed to fix a retention problem).

## Driver trees
Break a top-line metric into its multiplicative or additive components
(e.g. `Revenue = Users × Activation Rate × ARPU × Retention`) to
identify which specific driver an opportunity or experiment is meant to
move, and to sanity-check whether the claimed impact is plausible given
the size of that driver relative to the whole.

## Choosing a validation/test method by assumption type
| You need to know... | Reach for... |
|---|---|
| Does the problem exist / matter? | JTBD interviews, switch interviews, support/churn analysis |
| Will people pay / prioritise this? | Concierge test, fake-door test, pre-sales conversations |
| Does the solution direction resonate? | Concept test, prototype walkthrough |
| Is a specific flow usable? | Moderated usability test on a low/mid-fi prototype |
| Did the shipped change actually work? | A/B test or sequential/holdout design, pre-registered |
