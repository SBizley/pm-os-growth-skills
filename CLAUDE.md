# CLAUDE.md

Context for Claude Code when working in this repo. Read this before
making changes.

## What this is
pm-os: a product management operating system for Claude. It's also my
public portfolio piece, so how it's built (commits, structure, honesty
about what it is) matters as much as what's in it.

Three layers:
1. **`context/`**: what's true about a product. Every skill reads it first
   and offers to write back.
2. **`skills/`**: 16 skills, one folder each, installable as a Claude Code
   plugin (`.claude-plugin/`) or uploadable to Claude one by one.
3. **`playbooks/`**: how to use it as a founding PM, or as product ops.

Plus `examples/fernway/` (a fictional worked example), `templates/`,
`frameworks/` (reference and the 14 method guides I actually use), and `pm-hub.html` (the
browsable hub).

## Repo structure
```
.claude-plugin/          plugin.json + marketplace.json
context/                 the brain: product, customers, metrics, bets, decisions, glossary, voice
skills/<name>/SKILL.md   one skill per folder, YAML frontmatter required
playbooks/               founding PM 90 days, product ops mode
examples/fernway/        fictional end-to-end worked example
templates/               fill-in templates the skills point to
frameworks/              frameworks reference, method library, method-guides/
pm-hub.html              standalone hub, no build step
HOW-I-WORK-WITH-AI.md    the chat > skills > workflows > agents ladder
CREDITS.md, LICENSE      attribution and MIT licence
```

## SKILL.md format
YAML frontmatter (`name` matching the folder, `description` saying when
to trigger), then: Purpose, When to use, Inputs needed, Context first
(pm-os), Step-by-step process, Output, Rules, Quality checklist, Hands
off to. Keep new skills in this shape. Run `claude plugin validate .`
after adding one.

## Writing rules
- **No em dashes.** Anywhere. Use a full stop, comma or colon.
- Run the Humaniser over any new prose. It should sound like me, not
  like Claude.
- British spelling.
- Don't overclaim. These are skills, not agents. Say what it is.

## Critical rule: no employer-specific or private content
This repo is public. Nothing from a past employer: no company names in
examples, no colleague names, no internal tool names, no real business
figures or strategy content. If source material is too specific to
genericise, extract the structure as a blank template and leave the
content out. Examples use fictional companies, clearly labelled. Never
commit personal data, credentials, or anything from my own job search.

## pm-hub.html conventions
- Single file, no build step, no external JS. Fonts from Google Fonts.
- Design tokens are CSS custom properties at the top of `<style>`.
- Method library is data-driven: `libData` array and `guideContent`
  object in the bottom script. Keep both in sync with
  `frameworks/method-guides/`.
- `mdToHtml` is a minimal hand-rolled renderer. Extend carefully.
- Internal navigation goes through JS (`.jump` + `openAndScroll`, or the
  delegated `a[href^="#"]` handler) because preview sandboxes mishandle
  native fragment jumps.
- Keep the method library short. Add a method only if I actually run it.
- After structural changes, check every method guide still opens in the
  panel (a jsdom script that clicks each row works well).

## Workflow
Small, logical commits with messages that explain why. Open a PR for
anything touching more than a couple of files.
