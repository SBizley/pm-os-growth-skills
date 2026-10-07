# How I work with AI

People use "AI agent" to mean everything from a chatbot to a fully
autonomous system, so here's how I think about it, where pm-os actually
sits, and what I've built at each level.

## The ladder

| Level | What it is | Who decides the steps | Example from my work |
|---|---|---|---|
| 1. Chat | You ask, it answers. Starts from zero every time. | You | Drafting, rewording, thinking out loud |
| 2. Context | It knows your stuff before you ask: projects, files, a `CLAUDE.md`, memory. | You | `context/` in this repo |
| 3. Skills | Reusable instructions it loads when the task matches. Your way of working, packaged. | You, guided by the skill | Every folder in `skills/` |
| 4. Workflows | An AI step inside a fixed pipeline that runs on a trigger. Code decides the order; the model does the judgement bit. | The pipeline | Slack automation that triaged incoming tickets |
| 5. Agents | Give it a goal and tools. It plans, acts, checks the result and loops until it's done, deciding the steps itself. | The model, within limits you set | Claude Code building and committing this repo |

The difference between 4 and 5 is the one that matters. A workflow
always does the same steps in the same order. An agent works out the
steps. That's more powerful, and it's exactly why it needs checkpoints.

## Where pm-os sits

pm-os is levels 2 and 3: context and skills. It isn't an agent, and I
don't pitch it as one. **It's what makes an agent good at product work.**
Point Claude Code or Cowork (both agents) at this repo and they pick up
how I'd run discovery, what a ready PRD looks like, and what's true about
the product, without being told every time.

The human checkpoints are deliberate. Discovery, strategy and PRD skills
all stop and ask before moving on, because the judgement calls (what to
prioritise, what to cut, which customer to serve) should be argued over
by a person. AI is brilliant at the first draft and the second opinion.
It's not the one who should decide what the company bets on.

## What I've actually built

**At my last company (a UK payments scale-up), as Lead PM:**
- AI-drafted PRDs and roadmap updates from source material, so PMs
  started from a structured draft rather than a blank page
- A Slack automation that triaged incoming tickets into Jira, so PMs
  weren't reading every one by hand (that logic is now
  `skills/feedback-triage`)
- I estimate it saved my squad 5+ hours a week and the wider PM team about
  a day a week

**Since then:**
- This repo: 16 skills, a context layer, playbooks and a worked example,
  built and committed with Claude Code
- My portfolio site, deployed through GitHub
- Skills I run every day, including the Humaniser (the most-used one) and
  Product Review (which I run on my own work before anyone else sees it)

## How this repo was built

With Claude Code, as an agent. The split was roughly this:
- **Me:** the skills' content and opinions (most of it started life in my
  own working docs and Notion), what goes in and what stays out, the
  no-employer-content rule, and every judgement call in the worked
  example
- **Claude:** restructuring, packaging, the hub's code, tests, finding
  inconsistencies, and drafts I then edited
- **Both:** arguing. Several decisions in here changed because Claude
  pushed back, and some didn't because I pushed back harder. That's the
  bit I'd want an interviewer to ask me about.

## Where I'd take it next (level 5)

The obvious next step is to make the rituals agentic: a scheduled agent
that runs `feedback-triage` every Friday, builds the `weekly-product-review`
pre-read on Monday morning, and drafts the decisions it thinks are
waiting, then stops for a human. The skills already exist. It's the
trigger and the checkpoint design that's left.
