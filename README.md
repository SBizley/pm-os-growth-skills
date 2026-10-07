# pm-os

The product management system I'd bring to a new team, written down so
Claude can run it with me.

I'm Sophie Bizley, a Lead PM with 10+ years in product, mostly in
fintech and payments, and most of it 0 to 1. Over the last couple of
years I've moved more and more of my PM work into Claude: drafting PRDs,
reviewing my own docs before anyone else sees them, triaging customer
feedback, prepping strategy. This repo is that way of working, cleaned
up so another PM or a whole team could pick it up.

**If you're here from my CV and have five minutes:** read the
[worked example](examples/fernway/README.md), then the
[founding PM playbook](playbooks/founding-pm-first-90-days.md). That's
the clearest picture of how I work.

---

## What it is

Three layers:

```
context/      What's true about the product: customers, metrics, bets,
              decisions, glossary, voice. The brain.
                  ▲ every skill reads this first, and offers to write back
                  │
skills/       16 skills, from day-one setup to launch. The methods.
                  │
playbooks/    How to use it as a founding PM, or as product ops for an
              existing team. The plan.
```

The context layer is what makes this more than a folder of prompts.
Without it, every conversation with Claude starts from zero and every
PRD needs the product re-explained. With it, the PRD skill already knows
your customers, the review skill knows what you decided last month, and
a new engineer can read six short files instead of sitting through a
week of meetings.

## The skills

| Stage | Skill | What it does |
|---|---|---|
| Set up | [pm-os-setup](skills/pm-os-setup/SKILL.md) | Founder interview that fills in `context/` on day one |
| Discover | [discovery](skills/discovery/SKILL.md) | Turns a vague signal into a scoped opportunity with its riskiest assumptions named |
| | [market-sizing](skills/market-sizing/SKILL.md) | Top-down and bottom-up, so each sanity-checks the other |
| | [customer-validation](skills/customer-validation/SKILL.md) | Tests whether the problem is real before anyone builds |
| | [feedback-triage](skills/feedback-triage/SKILL.md) | Turns tickets and call notes into themes linked to segments and bets |
| Decide | [product-strategy](skills/product-strategy/SKILL.md) | Four phases with a human checkpoint between each |
| | [prioritisation-and-roadmap](skills/prioritisation-and-roadmap/SKILL.md) | Now / Next / Later / Not doing, every item tied to a metric |
| | [decision-log](skills/decision-log/SKILL.md) | So nobody re-argues the same decision in six months |
| Define | [prototyping](skills/prototyping/SKILL.md) | Matches fidelity to the question, not to ambition |
| | [prd-generation](skills/prd-generation/SKILL.md) | Implementation-ready requirements engineers can start from |
| Ship and learn | [launch-readiness](skills/launch-readiness/SKILL.md) | Go / no-go, including the boring stuff that sinks launches |
| | [experimentation](skills/experimentation/SKILL.md) | Pre-registered tests, read honestly |
| | [stakeholder-update](skills/stakeholder-update/SKILL.md) | Updates that lead with what changed and what you need |
| | [weekly-product-review](skills/weekly-product-review/SKILL.md) | The weekly ritual that keeps `context/` current |
| Challenge | [product-review](skills/product-review/SKILL.md) | A senior product leader's read on your doc before it reaches the room |
| | [humaniser](skills/humaniser/SKILL.md) | The last pass on anything with words in it |

The two in "Challenge" are the ones I use most. I run Product Review on
my own PRDs, and it regularly catches things I'd have been embarrassed to
have pointed out in a meeting.

There's also a [hub page](pm-hub.html) for browsing,
[templates](templates/) for every output, and the
[14 workshop methods](frameworks/method-guides/INDEX.md) I actually run.
I cut that library down from 50. A long catalogue looks thorough, but
the three I'd run first at a new company are Crazy 8s, Story Mapping and
a Value Proposition Exercise, and those are written the way I run them.

## Using it

**With Claude Code (or anything that reads Claude Code plugins).** This
is the full experience: skills, context and repo all in one place.
```
/plugin marketplace add SBizley/pm-os-growth-skills
/plugin install pm-os@pm-os
```
Then copy `context/` into your own product repo and run `pm-os-setup`.

**With Claude on the web or desktop.** Zip any folder in `skills/` and
upload it in Claude's Skills settings. Create a Project for
your product and add your filled-in `context/` files to it as project
knowledge. Skills will pick them up.

**Without Claude at all.** Every skill is plain markdown with a
step-by-step process and a checklist. A team that doesn't use AI can
still use them as a process doc.

## Decisions I made building it

A few calls worth explaining, because they're the ones I'd expect to be
asked about.

**A context layer instead of more skills.** The first version of this
repo was seven good skills and no memory. Every one of them started by
asking the same questions about the product. Adding `context/` did more
for output quality than any new skill would have.

**Human checkpoints, on purpose.** Discovery, strategy and the PRD skill
all stop and ask before moving on. Claude is very good at a first draft
and a second opinion. It shouldn't be the one deciding what a company
bets on. More on that in [How I work with AI](HOW-I-WORK-WITH-AI.md).

**Founding PM first, big team second.** The skills are sized for a
startup with one PM and a handful of engineers. There's a separate
[product ops playbook](playbooks/product-ops-mode.md) for rolling it out
to an existing team, and it's deliberately opt-in, because process that
gets mandated on day one gets ignored by day ten.

**My interview prep stays out.** I have skills for case interviews and
take-homes too. They're useful to me, but a company adopting this
doesn't need them, so they're not here.

**Nothing from a past employer.** Everything is genericised, and the
worked example is a made-up company. Where a skill grew out of something
I built at work, I've kept the method and dropped the content.

## Where my thinking got challenged

Honestly, the biggest one was this repo itself. I'd been calling it a
"PM operating system", and when I went back through it properly it was
a skill pack: no context, no setup, no way for someone else to start
using it on day one. The name was ahead of the thing. This version is
the thing catching up.

The [worked example](examples/fernway/README.md) has two more, including
a success metric I wrote that my own review skill caught as gameable.

## What it isn't

It isn't an agent, and I don't pitch it as one. It's the context and
methods that make an agent (Claude Code, Cowork) good at product work.
And it isn't a replacement for talking to customers. Several skills will
refuse to go further until you have.

## What's next

- Scheduled agents for the rituals: Friday feedback triage, Monday
  review pre-read, both stopping for a human before anything's decided
- Evals for the skills, so changes can be tested rather than eyeballed
- Running it for real with a team, and writing up what broke

## Credits and licence

Frameworks credited in [CREDITS.md](CREDITS.md). Code and original
content are MIT licensed.

If you're hiring a founding PM or product ops lead and this is how you'd
like product to work, I'd love to chat:
[LinkedIn](https://www.linkedin.com/in/sophiebizley/).
