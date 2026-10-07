---
name: "customer-validation"
description: "Use when testing whether customers actually have a problem, or whether a proposed solution addresses it, before committing engineering time. Trigger on requests like validate this assumption, design a customer interview, or test this idea with users."
---

# Skill: Customer Validation

## Purpose
Test whether real customers actually have the problem you think they
have, and whether your proposed direction actually solves it, before
you spend engineering time finding out the hard way. Covers both
problem validation (does this pain exist and matter) and solution
validation (does this direction address it).

## When to use
- After Discovery has produced a riskiest-assumptions list
- Before writing a PRD for anything non-trivial
- After Prototyping, to test a concept/prototype with real users
- When a stakeholder is convinced of a solution and you need evidence
  either way before committing

## Inputs needed
- The riskiest assumptions from the Discovery brief (this skill is
  built to test those specifically, not to run generic research)
- Access to customers or a recruitment channel (existing user base,
  sales/CS relationships, a panel, or a recruiting tool)
- A prototype or concept, if this is solution validation rather than
  problem validation
- Any existing research on this segment, so you're not re-asking
  questions already answered

## Context first (pm-os)
Before starting, read whatever exists in `context/` (product, customers,
metrics, bets, decisions, glossary). Don't ask for anything that's already
written down there, and use the glossary's terms. When you finish, list
anything this work changed (a new decision, a sharper customer insight, a
metric definition) and offer to write it back to the right file in
`context/`. That loop is what keeps the system current.

## Step-by-step process

**1. Turn the riskiest assumption into a falsifiable test.**
"Users want this feature" is not testable. "SMB merchants abandon
onboarding because they can't estimate settlement time, not because the
form is too long" is testable. State what evidence would prove the
assumption wrong, not just what would confirm it. This is the
single biggest quality differentiator in validation work.

**2. Choose the validation method to match the assumption type.**
- **Problem exists / matters** → JTBD-style interviews, support ticket
  analysis, "switch" interviews with people who churned or chose a
  competitor
- **Willingness to pay / prioritise** → concierge tests, fake-door
  tests, pricing conversations, pre-sales
- **Solution direction resonates** → concept tests, prototype walk-throughs,
  smoke tests
- **Usability of a specific flow** → moderated usability sessions with
  a prototype (hands off to Prototyping skill for the artifact itself)

Don't default to interviews for everything. Match the method to what
you're actually trying to learn.

**3. Write the interview/test guide before recruiting.**
For interviews: ask about past behaviour, not future intentions ("tell me about the
last time you tried to do X" beats "would you use a feature that does
X?"). Hypothetical questions about hypothetical features produce
unreliable signal: people are poor predictors of their own future
behaviour.

**4. Recruit for the segment, not for convenience.**
State the target segment explicitly and recruit against it. A sample
of enthusiastic existing power users will systematically overstate
demand; include some skeptics, churned users, or non-users where the
assumption concerns broader appeal.

**5. Run the sessions with a clear separation of roles.**
One person asks questions, one takes notes. Don't do both if you can
help it, note-taking degrades listening quality. Ask open questions,
resist the urge to pitch or defend the idea, and let silence sit
instead of filling it.

**6. Synthesise across sessions, not within a single one.**
Don't over-index on one compelling anecdote. Look for patterns across
at least 5-8 conversations before drawing conclusions on a problem
validation question; solution/usability testing can show real signal
with 5 sessions since usability issues repeat quickly. Tag findings by
theme, not by participant, and count how many participants hit each
theme.

**7. Write the validation readout.**
State the original assumption, what was tested, what was found, and
whether the assumption is validated / invalidated / inconclusive. Inconclusive is a legitimate outcome and should be reported as such
rather than forced into a direction.

## Output
A validation readout: assumption tested, method used, sample
(size + who), synthesised findings by theme with supporting quotes/counts,
and a clear validated/invalidated/inconclusive call with recommended next
step.

## Quality checklist
- [ ] The assumption was falsifiable, and the test could have
      disproven it
- [ ] Questions asked about past behaviour, not hypothetical future
      behaviour
- [ ] Findings are synthesised across sessions, not driven by one
      anecdote
- [ ] Recruitment matched the target segment, not just who was easy to
      reach
- [ ] The readout gives a clear call, including "inconclusive" if that's
      honest

## Common failure modes to catch
- Leading questions ("wouldn't it be great if...") that produce
  false-positive enthusiasm
- Confusing politeness for validation: people are reluctant to say an
  idea is bad to your face; watch behaviour and past-tense stories more
  than stated opinions
- Stopping at the first session that confirms the hypothesis you wanted

## Hands off to
- **Prototyping**: problem-validated opportunities are what get a
  prototype built for solution testing
- **Experimentation**: solution-validated concepts that need
  quantitative confirmation at scale move to an experiment
- **PRD Generation**: validated opportunities are the evidence base
  a PRD's problem statement should cite
