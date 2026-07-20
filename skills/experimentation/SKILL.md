# Skill: Experimentation

## Purpose
Design and read experiments that actually answer the question they're
meant to answer — turning "did that work?" into a pre-registered,
statistically sound test rather than a post-hoc story fitted to
whatever the dashboard shows afterward.

## When to use
- You've shipped a change (or a validated concept) and need to know its
  real impact, not just whether metrics moved
- Before launch, to pre-register what success looks like and avoid
  post-hoc metric shopping
- Reading someone else's experiment results and need to sanity-check
  the conclusion
- Prioritising which of several ideas to test first, given limited
  traffic/sample

## Inputs needed
- The hypothesis and the specific metric it should move (ideally
  inherited directly from the driver tree in Market Sizing, or the
  validated concept from Customer Validation/Prototyping)
- Baseline data: current metric value, variance, typical traffic/volume
  through the relevant flow
- Constraints: minimum test duration the business will tolerate,
  seasonality risk, any regulatory/compliance limits on what can be
  tested live (relevant in payments/fintech — check what needs
  compliance sign-off before launch)
- Analytics/experimentation tooling available (in-house platform,
  third-party tool, or manual cohort analysis)

## Step-by-step process

**1. Write the hypothesis in a falsifiable, single-variable form.**
"If we [change], then [metric] will [move in direction] because
[mechanism]." One primary metric, one primary change. If multiple
variables are changing at once, you won't know which one caused the
result.

**2. Pre-register success criteria before launch.**
Primary metric, minimum detectable effect (MDE) you actually care
about, and the decision rule ("if primary metric improves by X% with
statistical significance, we ship; if not, we don't") — written down
*before* the data comes in. This is the single biggest defence against
post-hoc rationalisation and metric shopping.

**3. Calculate required sample size and duration up front.**
Given baseline conversion/metric rate, desired MDE, and traffic volume,
estimate how long the test needs to run to reach significance. State
this explicitly rather than "peeking" and stopping whenever the result
looks favourable — early stopping on a favourable-looking result
inflates false positive rates substantially.

**4. Choose the right design for the question.**
- **A/B test**: standard for a single change with enough traffic to
  reach significance in a reasonable window
- **A/B/n**: multiple variants, more traffic required, adjust
  significance threshold for multiple comparisons
- **Sequential/holdout**: when true randomisation isn't feasible
  (e.g., B2B sales-assisted flows) — compare a held-out group over time
  instead
- **Pre/post with strong caveats**: last resort when neither is
  possible — flag confounding risk explicitly (seasonality, concurrent
  changes) rather than presenting it with false confidence

**5. Define guardrail metrics.**
Alongside the primary metric, name 1-3 metrics that must NOT move in
the wrong direction (e.g., a conversion lift that tanks retention or
support volume isn't a win). Check these even if the primary metric
looks great.

**6. Run it for the full pre-registered duration.**
Resist calling it early. Note any external events (holidays, outages,
marketing pushes) that occurred during the window as caveats to the
final read.

**7. Read the results against the pre-registered plan, not
retroactively.**
Report: did the primary metric hit the pre-registered bar, at what
confidence level, what happened to guardrails, and what the decision
rule says to do. If the result is ambiguous or the effect is real but
smaller than the MDE, say so — "no detectable effect at this sample
size" is a different, more honest conclusion than "it didn't work."

**8. Write the experiment readout.**
Use `templates/experiment-design-doc-template.md` (doubles as the
pre-registration doc and the readout — fill the top half before launch,
the bottom half after).

## Output
An experiment design doc (pre-launch) and readout (post-launch):
hypothesis, primary metric + MDE, sample size/duration calculation,
design type, guardrails, and — after running — the result read against
the pre-registered decision rule.

## Quality checklist
- [ ] Hypothesis names one mechanism and one primary metric
- [ ] Success criteria and decision rule were written before results
      came in
- [ ] Sample size/duration was calculated up front, not eyeballed
- [ ] Guardrail metrics were checked, not just the primary metric
- [ ] The test ran its full pre-registered duration (or the early stop
      is explicitly justified and flagged)
- [ ] The conclusion distinguishes "no effect" from "no detectable
      effect at this sample size"

## Common failure modes to catch
- **Peeking and stopping early** on a favourable-looking result
- **Metric shopping** after the fact — reporting whichever secondary
  metric moved instead of the pre-registered primary one
- **Multiple simultaneous changes** making it impossible to attribute
  the result
- **Ignoring guardrails** because the primary metric looked good
- **Underpowered tests** presented with unwarranted confidence

## Hands off to
- **Discovery** — a "no effect" or invalidated result feeds back into
  the opportunity tree as new evidence, often reframing the original
  opportunity
- **pm-os prioritisation / roadmap builder** — validated wins get
  scaled and rolled into the roadmap; invalidated ones get deprioritised
  with evidence attached, not just dropped silently
