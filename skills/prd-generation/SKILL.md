---
name: "prd-generation"
description: "Use when turning a validated opportunity, strategy, or brief into an implementation-ready Product Requirements Document with user stories, functional and non-functional requirements. Trigger on requests like write a PRD, turn this into requirements, or draft user stories for X."
---

# Skill: PRD Generation

## Purpose
Turn a validated opportunity (a strategy, a roadmap item, a partial brief,
or just a conversation) into an implementation-ready Product Requirements
Document. An engineering team should be able to start building from the
output immediately.

## When to use
- Writing a PRD, spec, or requirements document
- Turning validated discovery/prototyping findings into user stories
- Asked "what should we build" and the answer needs to be specific enough to hand to engineering
- Reviewing someone else's PRD for gaps (run it against the quality checklist below)

## Inputs needed
Works from any of:
1. A full strategy, roadmap, or requirements page
2. A partial draft, brief, or linked source material
3. A conversation where the missing inputs are gathered first

If working from a conversation, gather before writing: who the users are,
what problem is being solved, what the product/feature should do, key
constraints, and how success will be measured. State assumptions
explicitly and label low-confidence gaps rather than guessing silently.

## Context first (pm-os)
Before starting, read whatever exists in `context/` (product, customers,
metrics, bets, decisions, glossary). Don't ask for anything that's already
written down there, and use the glossary's terms. When you finish, list
anything this work changed (a new decision, a sharper customer insight, a
metric definition) and offer to write it back to the right file in
`context/`. That loop is what keeps the system current.

## Step-by-step process

**1. Understand the context.**
If a strategy/roadmap exists, extract: vision, target users, strategic
pillars, the specific features in scope (focus on the now/P0 items),
constraints, success metrics. If working from a conversation, ask
targeted questions to establish the same context. At minimum: the
user, the problem, the proposed solution direction, and the constraints.

**2. Define the product overview.**
One-sentence vision, problem statement, target users, success metrics.
This is the context that makes every requirement make sense. A PRD
doesn't require a formal strategy doc to exist first, but it does
require clarity on who, what, and why.

**3. Write user stories, grouped into epics.**
Format:
```
[ID]: [Title]
As a [user type], I want to [action] so that [benefit].

Acceptance Criteria:
- [Testable criterion 1]
- [Testable criterion 2]
- [Testable criterion 3]
- [Testable criterion 4: edge case or error handling]

Priority: [Must Have / Should Have / Could Have / Won't Have]
Estimated Effort: [S / M / L / XL]
Strategic Link: [Which pillar/JTBD this serves]
```
Use sequential IDs (US-001, US-002...). 3-5 testable acceptance criteria
per story. Apply MoSCoW honestly (see Rules below).

**4. Define functional requirements.**
What the system must do. Format:
```
[FR-001]: [Requirement Title]
[Detailed description of the functionality]

Acceptance Criteria:
- [Specific, testable criterion]
- [Specific, testable criterion]

Dependencies: [Other requirements this depends on]
Priority: [Critical / High / Medium / Low]
User Stories: [US-001, US-003]
Strategic Objective: [Which pillar this enables]
```
Cover: Authentication & Authorisation, Core Features, Data Management,
Integration, Reporting & Analytics. Every requirement links back to a
user story and strategic objective. Traceability is mandatory.

**5. Define non-functional requirements, with numbers, not vibes.**
- **Performance:** API response times (ms at p95), page load time,
  concurrent users supported, database query performance (ms at p95)
- **Security:** authentication method, encryption at rest/in transit,
  compliance standard (GDPR / PCI-DSS / SOC 2 / etc.), audit logging scope
- **Scalability:** horizontal scaling approach, load handling (req/s),
  data volume
- **Reliability:** uptime % (measured over what period), RTO, RPO,
  backup frequency
- **Usability:** accessibility level (WCAG), browser support, mobile
  approach (responsive/native/both), max loading time
- **Maintainability:** minimum test coverage %, documentation standard,
  deployment frequency capability

**6. List open questions and risks.**
What's unresolved and needs stakeholder input; what could go wrong
(technical, market, resource, dependency), each risk with a mitigation.

**7. Run a final clarity pass.**
Before sharing, do a dedicated editing pass for plain language and
tightness, cut hedging, jargon, and anything that doesn't help the
reader act. Don't skip this step for a first draft.

## PRD output template
```
# Product Requirements Document: [Product Name]

## 1. Product Overview
Vision: [One sentence]
Problem Statement: [What problem are we solving?]
Target Users: [Primary and secondary personas]
Success Metrics: [Key metrics with targets]
Strategic Context: [Which strategy pillar(s) this serves]

## 2. User Stories
### Epic 1: [Epic Name]
[US-001 through US-XXX using the format above]
### Epic 2: [Epic Name]
[Stories]

## 3. Functional Requirements
[FR-001 through FR-XXX using the format above]

## 4. Non-Functional Requirements
[NFR-001 through NFR-XXX with specific thresholds]

## 5. Technical Specifications
Recommended Tech Stack: [With rationale]
System Architecture: [Key patterns]
Core Data Models: [Entities and relationships]
API Design: [Key endpoints]
Third-Party Services: [External dependencies]

## 6. Constraints & Assumptions
Constraints: [Budget, timeline, technical, regulatory]
Assumptions: [User behaviour, market, technical, resources]

## 7. Success Criteria & Metrics
Launch Criteria: [Minimum for launch]
Success Metrics: [With targets and measurement methods]

## 8. Open Questions & Risks
Open Questions: [Unresolved decisions needing stakeholder input]
Risks: [Technical, market, resource, dependency, each with mitigation]

## Overall Confidence: [X]%
```

## Rules
- **Specific, not vague.** ❌ "The system should be fast" → ✅ "API
  responses must complete in <200ms for the 95th percentile." Every
  requirement must be testable.
- **Traceability is mandatory.** Every requirement links to a user need
  and a strategic objective. If you can't trace it back, it doesn't belong.
- **Not everything is P0.** MoSCoW honestly: Must Have is the MVP,
  Should Have is important but launchable without, Could Have is nice,
  Won't Have (this time) is explicit scope exclusion.
- **Cover the unhappy paths.** Error cases, edge cases, failure
  scenarios, security concerns. The happy path is easy; the unhappy
  path is where quality lives.
- **NFRs need numbers.** Response times (ms, at which percentile),
  uptime (% with measurement period), concurrent users (peak load),
  accessibility (WCAG level). No NFR without a testable threshold.
- **Preserve source language.** If a strategy doc uses specific terms
  for segments, features, or metrics, the PRD uses the same terms. Consistency prevents confusion.

## Quality checklist
- [ ] Product overview links to strategy (pillar, JTBD) or states there isn't one yet
- [ ] User stories in correct format with 3-5 acceptance criteria each
- [ ] MoSCoW prioritisation applied honestly, not everything Must Have
- [ ] Functional requirements are specific and testable
- [ ] NFRs have numeric thresholds, not "fast" or "secure"
- [ ] Every requirement traces to a user story and strategic objective
- [ ] Unhappy paths covered (errors, edge cases, failure scenarios)
- [ ] Technical specs guide without over-prescribing
- [ ] Open questions listed (a sign of intellectual honesty, not weakness)
- [ ] Risks identified with mitigations
- [ ] Terminology consistent with the source strategy/brief

## Hands off to
- **Experimentation**: launch-critical requirements often define the
  guardrail metrics an experiment needs to check
- **Prioritisation and Roadmap**: epics and MoSCoW
  priorities feed directly into roadmap sequencing
- **Product Review**: run the draft past it before it goes to
  engineering or leadership
- **Launch Readiness**: once it's built, the acceptance criteria become
  the launch checklist's starting point
