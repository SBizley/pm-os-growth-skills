---
name: "launch-readiness"
description: "Use before shipping a feature or product to check it's actually ready: acceptance criteria met, metrics instrumented, support briefed, rollback plan, comms drafted. Trigger on are we ready to launch, launch checklist, go/no-go, or what have we forgotten before release."
---

# Skill: Launch Readiness

## Purpose
Catch the things that turn a good build into a bad launch: nobody told
support, the event that measures success was never instrumented, there's
no way to roll back, sales found out from a customer. Runs as a go/no-go
check a few days before release.

## When to use
- A few days before anything customer-facing ships
- Before a beta or pilot opens to real users
- When someone says "it's basically ready" (it rarely is)

## Inputs needed
- The PRD, or at least the acceptance criteria
- Release date and rollout plan (all at once, percentage rollout, beta
  list)
- Who needs to know: support, sales, success, partners, the founder

## Context first (pm-os)
Read `context/metrics.md` for the metric this launch should move and the
guardrails it mustn't break. Read `context/glossary.md` so customer-facing
copy uses the right words.

## Step-by-step process

**1. Check the build against the PRD.**
Go through every Must Have acceptance criterion. Each is Met, Not met, or
Met with a known issue. Anything Not met is either fixed, cut with a
decision logged, or a no-go.

**2. Check measurement.**
Can we see, on day one, whether this worked? Name the event(s), confirm
they fire in a test, and confirm the dashboard or query exists. If the
launch has an experiment, check the Experimentation skill's
pre-registration is done.

**3. Check the downside.**
- What breaks if this goes wrong, and for whom?
- How do we turn it off? Feature flag, rollback, or "we can't" (which
  needs a louder conversation)
- Which guardrail metric would tell us first, and who's watching it?

**4. Check the humans.**
Support has a short brief and the top five questions with answers. Sales
or success know what's changing and what to say. Anyone who'll be asked
about it has heard it from us first.

**5. Check the words.**
Release notes, in-app copy, help article. Run them through the Humaniser.

**6. Call it.**
Go, go with conditions, or no-go. Write the reason down either way.

## Output
A launch readiness table (area, status, owner, notes) ending in a clear
Go / Go with conditions / No-go and the reason. Template:
`templates/launch-checklist-template.md`.

## Rules
- "We'll add tracking after launch" is a no-go for anything with a
  success metric. You only get one clean before/after.
- A launch with no off switch needs the founder or eng lead to sign off
  explicitly.

## Quality checklist
- [ ] Every Must Have criterion checked
- [ ] Success event fires and is visible somewhere
- [ ] Rollback or kill switch confirmed
- [ ] Support briefed with real answers, not "contact product"
- [ ] Go / no-go decision written down with a reason

## Hands off to
- **Experimentation**: to read the result
- **Stakeholder Update**: the launch announcement
- **Weekly Product Review**: launch metrics go on the agenda for the next
  few weeks
