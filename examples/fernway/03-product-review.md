# Product Review of the auto-fill PRD (v1)

_Skill: product-review · Run on my own draft before it went to the
founder · Fictional example_

## Overall
The thesis is good and grounded in discovery. But this reads like we
already know customers will accept short-notice spots, and we don't.
That's the bet. Cut this to the smallest thing that tests it, and fix
the metric before someone games it.

## Checklist
| Check | Result |
|---|---|
| Leads with status and what we learned | Pass |
| Unknowns called out explicitly | **Fail.** The riskiest assumption from discovery is missing |
| Metric hierarchy clear | **Fail.** No guardrail |
| Phased rather than big-bang | **Fail.** Smart waitlist is in scope with no evidence it's needed |
| Dependencies with owners | Partial. Processor check has no owner or date |

## Comments
1. **Risk flag, Overview:** "Success metric: % re-filled" can be hit by
   blasting the whole waitlist at once. Add notification opt-out rate as
   a guardrail, or this metric will reward annoying people.
2. **Clarity probe, AF-1:** Why 30 minutes? At 2 hours' notice, 30
   minutes per person means the spot reaches person four at the latest.
   Is that the point?
3. **Simplification, Epic 2:** Move smart waitlist out. You don't know
   yet whether anyone accepts, never mind who's most likely to.
4. **Risk flag, AF-1:** Charging on acceptance depends on the processor
   answer. That's a one-way door for the payments flow. Get the answer
   before engineering starts, with a name against it.
5. **Timeline reality:** This is about six weeks of build. A pilot with
   five studios is about two and would tell us if the other four are
   worth it.

## Fix before it goes to the founder
1. Add the riskiest assumption to the top, with how the pilot tests it
2. Add opt-out rate as a guardrail with a threshold (2 points)
3. Cut Epic 2. Note it as Next, pending pilot results
4. Put an owner and a date on the processor question
5. Reframe v1 as a four-week pilot with five studios and a clear pass
   mark (20% of late-cancelled spots re-filled)

## What happened
All five accepted. Decision logged in `context/decisions.md`, bet added
to `context/bets.md`.
