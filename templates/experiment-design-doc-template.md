# Experiment: [Name]

**Author:** · **Date launched:** · **Pre-registered by (fill before
launch):**

## PRE-LAUNCH (fill before results come in)

### Hypothesis
If we [change], then [metric] will [move in direction] because
[mechanism].

### Primary metric & minimum detectable effect (MDE)
Metric: · Baseline: · MDE we care about: ___%

### Sample size / duration calculation
Traffic/volume available: · Required sample: · Estimated duration:

### Design
- [ ] A/B
- [ ] A/B/n
- [ ] Sequential / holdout
- [ ] Pre/post (last resort — flag confounds below)

Confound risks (seasonality, concurrent changes, compliance limits):

### Guardrail metrics
1. — must not move by more than ___
2. — must not move by more than ___

### Decision rule
If primary metric improves by ≥___% at significance level ___, we
[ship / scale]. If not, we [don't ship / iterate / kill], because
[reasoning].

---

## READOUT (fill after full pre-registered duration)

### Did it run the full duration?
Yes / No — if no, why:

### Primary metric result
Observed effect: · Confidence level: · Hit pre-registered bar? Y/N

### Guardrail check
| Guardrail | Moved? | Within bounds? |
|---|---|---|
| | | |

### External events during test window

### Conclusion
- [ ] Effect confirmed — ship/scale
- [ ] No effect
- [ ] No detectable effect at this sample size (different from "no
      effect" — note if a follow-up with more power is warranted)

### Next step
