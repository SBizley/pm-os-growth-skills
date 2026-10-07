# Product ops and chief of staff mode

The founding PM playbook is about running the product yourself. This one
is about setting pm-os up for a product team that already exists, as a
product ops lead or chief of staff. Different job, same toolkit.

The goal here isn't to make every PM work the way I do. It's to make the
things that should be consistent, consistent (how decisions get made and
recorded, how metrics are defined, what a "ready" PRD looks like), and
leave everything else to the PMs.

## What I'd standardise, and what I wouldn't

| Standardise | Leave to each PM |
|---|---|
| Metric definitions (`context/metrics.md`) | Which discovery methods they use |
| Decision log format and where it lives | How they run their stand-ups |
| What "PRD ready for engineering" means (the PRD quality checklist) | PRD length and style |
| Launch readiness go/no-go | Prototyping tools |
| Weekly product review format | Their own rituals inside the squad |

## Rollout, roughly four weeks

**Week 1: listen.** Interview each PM and eng lead: where do they lose
time, what do they re-explain constantly, what went wrong at the last
launch? Run `feedback-triage` on the answers like they're customer
feedback (they are).

**Week 2: one shared context.** Set up `context/` for the product as a
whole, with a folder per squad if needed. The metric tree is the first
fight worth having.

**Week 3: one ritual.** Start the weekly product review. Don't add
anything else yet.

**Week 4: opt-in skills.** Show the team the skills, install them for
whoever wants them, and let usage spread. Anything mandated on day one
gets resented on day ten.

## How I'd know it's working
- PMs spend less time writing updates (I'd ask them, not guess)
- Fewer "why did we decide this?" threads
- New joiners onboard from `context/` instead of a week of meetings
- Launches stop missing the same three things

## How to install it for a team
See the "Using it" section of the main README. For a team, I'd use the
Claude Code plugin route for anyone technical and a shared Claude Project
(with `context/` and the skills uploaded) for everyone else.
