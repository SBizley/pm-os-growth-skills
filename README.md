# pm-os: Product Development Skills Pack

This pack extends **pm-os** — Soph's Claude-powered PM operating system —
with five new skills covering the front end of the product lifecycle:
discovery, market sizing, experimentation, customer validation, and
prototyping. Existing pm-os skills (PRD writer, prioritisation, roadmap
builder, story bank, case prep, outreach drafter, investment portfolio
analyzer) cover craft and career; this pack covers the "should we build
this, and is it working" half of the job.

## Why these five

Together they cover the full loop a PM/GTM/ops person runs before and
during a bet:

```
DISCOVERY  →  MARKET SIZING  →  CUSTOMER VALIDATION  →  PROTOTYPING  →  EXPERIMENTATION
(what's the      (is it worth        (do real people        (make it        (did it
 problem?)         doing?)             want THIS?)           tangible)       work?)
```

They're designed to hand off into each other — a discovery brief feeds
market sizing inputs, validation findings feed prototype briefs,
prototype feedback feeds experiment design — the same way pm-os's
existing skills already reference each other.

## How to install into your existing pm-os

1. Drop the `skills/` subfolders into your pm-os `skills/` directory
   (or wherever your existing PRD writer / roadmap builder / etc. live).
2. Drop `templates/` into your existing `templates/` folder.
3. Drop `frameworks/frameworks-reference.md` into a `frameworks/` folder
   — or merge it into wherever you keep the reference material your
   other skills already point to.
4. If your pm-os uses context templates (company info, stakeholder
   profiles, writing style, PM background), these five skills are
   written to check that same context first — no separate setup needed.

## Skill index

| Skill | File | Use when |
|---|---|---|
| Discovery | `skills/discovery/SKILL.md` | You have a vague problem, signal, or exec ask and need to turn it into a scoped opportunity |
| Market Sizing | `skills/market-sizing/SKILL.md` | You need to know if an opportunity is big enough to justify the bet |
| Customer Validation | `skills/customer-validation/SKILL.md` | You need to test whether real customers have the problem / want the solution, before or after building anything |
| Prototyping | `skills/prototyping/SKILL.md` | You need something tangible to put in front of users, stakeholders, or engineers — fast |
| Experimentation | `skills/experimentation/SKILL.md` | You've shipped something (or a variant) and need to know if it worked |
| PRD Generation | `skills/prd-generation/SKILL.md` | A validated opportunity needs to become implementation-ready requirements |
| Product Strategy System | `skills/product-strategy/SKILL.md` | Setting or refreshing strategy for a product area, four phases with checkpoints |

Each `SKILL.md` follows the same shape: **Purpose → When to use → Inputs
needed → Step-by-step process → Output template → Quality checklist →
Hands off to**. That last section is what wires them together and into
the rest of pm-os.

## Templates

Ready-to-fill docs referenced by the skills above:
- `discovery-brief-template.md`
- `market-sizing-template.md`
- `validation-interview-guide-template.md`
- `prototype-brief-template.md`
- `experiment-design-doc-template.md`

## Frameworks reference

`frameworks/frameworks-reference.md` is a single reference doc covering
the frameworks the skills call on: Opportunity Solution Trees, JTBD,
TAM/SAM/SOM (top-down and bottom-up), ICE/RICE/PIE, the Riskiest
Assumption Test, Lean Startup build-measure-learn, and Pirate Metrics
(AARRR). It's written as a companion, not a substitute — the skills
tell you *when* to reach for each one.

`frameworks/discovery-method-library.md` is the quick-picker: 30+
named activities, recipes, and method categories, organized by what
you're trying to learn and how much time you have.

`frameworks/method-guides/` holds the full step-by-step facilitation
guide for 50 of those methods — purpose, when to use, materials,
timing, steps, a worked example, tips, and further reading for each.
Start at `frameworks/method-guides/INDEX.md`.

## A note on portability

These are written framework-and-process-first, not tool-first — they
work as a Claude Code / Claude Desktop skill pack, as plain markdown
you paste into a Claude.ai project, or as a printed process doc for a
new team that doesn't use Claude at all. That's deliberate: the goal is
a system you carry across jobs, not one tied to a specific setup.
