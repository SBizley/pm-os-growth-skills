# Skill: Prototyping

## Purpose
Make an opportunity tangible enough to react to — for users,
stakeholders, or engineers — as cheaply and quickly as the question
requires. The core discipline here is matching prototype fidelity to
the question being asked, not defaulting to the highest-effort option.

## When to use
- After problem validation, to test whether a specific solution
  direction resonates
- Before writing a full PRD, to de-risk direction with stakeholders
  cheaply
- When engineering needs something more concrete than a written spec
  to scope effort
- When a concept needs to survive a usability test before build

## Inputs needed
- The validated opportunity and job story from Discovery/Validation
- The specific question the prototype needs to answer (this determines
  fidelity — see step 1)
- Design/brand context if available (existing component library, style
  guide)
- Time and tooling constraints (what's realistic to produce in the time
  available — Claude artifacts, Figma, clickable mockup tools, or a
  real coded prototype)

## Step-by-step process

**1. Name the question before picking a fidelity level.**
Every prototype should be built to answer ONE primary question. Match
fidelity to that question:
- *"Does this concept make sense at all?"* → sketches, a single static
  screen, or a one-paragraph concept description
- *"Does this flow make sense?"* → clickable low-fi wireframes (grey
  boxes, no visual polish) — polish here is wasted effort and can
  distract testers from flow issues
- *"Does this feel right / would people trust it?"* → high-fidelity
  visual mockup, on-brand
- *"Does this actually work end-to-end?"* → a coded prototype or
  Wizard-of-Oz test (real front end, manually-operated or faked back
  end)
- *"Will people really do this, not just say they would?"* → a smoke
  test / fake-door test in a real environment (a real landing page, a
  real "join waitlist" button, a real ad)

**2. Write the prototype brief before building.**
Use `templates/prototype-brief-template.md`: the question, the
fidelity level chosen and why, the specific flow/scenario to cover, and
what "useful signal" looks like when testing is done. This prevents
scope creep into building more than the question requires.

**3. Build the smallest version that answers the question.**
Resist adding edge cases, extra screens, or polish that don't serve the
primary question — every extra element is something a test participant
might react to instead of the thing you actually need feedback on.

**4. Decide the test format alongside the build.**
- **Moderated**: you walk a participant through it live, watching
  behaviour and asking follow-ups — best for early-stage or ambiguous
  concepts
- **Unmoderated**: participants use it alone and you review recordings
  — better once the flow is concrete enough that your presence would
  bias behaviour
- **In-context / smoke test**: dropped into a real environment (a real
  page, a real email) to measure actual behaviour rather than stated
  reaction — the strongest signal, but only answers narrow questions

**5. Run it against the Customer Validation skill's method.**
Hands off directly — same interview/test-guide discipline applies:
past-behaviour framing, don't lead the witness, synthesise across
sessions.

**6. Capture build-relevant output alongside user-reaction output.**
If this prototype is also meant to help engineering scope effort,
explicitly separate "what we learned about user reaction" from "what we
learned about technical complexity" — they're different outputs for
different audiences and shouldn't be blended into one document.

## Output
A prototype (at the chosen fidelity) plus a short brief covering: the
question it answers, fidelity rationale, the scenario/flow covered, and
— once tested — a findings summary in the same format as Customer
Validation's readout.

## Quality checklist
- [ ] The primary question is stated explicitly, and fidelity matches it
- [ ] Nothing was built beyond what the question requires
- [ ] The test format (moderated/unmoderated/in-context) matches the
      concept's maturity
- [ ] Findings distinguish user-reaction signal from technical-scoping
      signal, if both were gathered

## Common failure modes to catch
- Defaulting to high-fidelity because it's more impressive to
  stakeholders, when the question only needed a wireframe
- Polishing visuals before flow is validated, wasting rework when flow
  changes
- Treating stakeholder enthusiasm for the prototype as equivalent to
  user validation — they're different audiences with different biases

## Hands off to
- **Customer Validation** — uses the same test-guide and synthesis
  discipline for the actual sessions
- **Experimentation** — a prototype that tests well moves to a
  quantitative experiment before full build, where the sample size
  justifies it
- **pm-os PRD writer** — the prototype and its findings become the
  PRD's "what we tried and learned" section, and often its wireframe
  reference
