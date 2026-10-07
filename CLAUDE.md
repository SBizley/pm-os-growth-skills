# CLAUDE.md

Context for Claude Code when working in this repo. Read this before making changes.

## What this is

A modular product management skill system for a Lead PM, built to run
inside Claude (chat, and now Claude Code). It covers the full arc from
"vague signal" to "shipped requirements": Discovery → Market Sizing →
Customer Validation → Prototyping → Experimentation, plus PRD
Generation and a Product Strategy System that sits above the loop.
`pm-hub.html` is the single-file interactive index into all of it.

## Repo structure

```
skills/<name>/SKILL.md, one skill per folder, see format below
frameworks/frameworks-reference.md, reference frameworks (OST, JTBD, TAM/SAM/SOM, ICE/RICE, RAT, AARRR)
frameworks/discovery-method-library.md, quick-picker: 50 methods, recipes, categories
frameworks/method-guides/*.md, full facilitation guide per method (also embedded inline in pm-hub.html)
templates/*.md, fill-in-the-blank templates, one per skill output
pm-hub.html, standalone interactive hub (no build step, no dependencies)
README.md, repo overview
```

## SKILL.md format

Every skill file follows: Purpose → When to use → Inputs needed →
Step-by-step process → Output → Rules → Quality checklist → Hands off
to (which skill/template this feeds into next). Keep new skills in
this shape, it's what makes them usable as actual Claude instructions,
not just documentation.

## pm-hub.html conventions

- Single file, no build step, no external JS dependencies (fonts load
  from Google Fonts CDN, everything else is vanilla JS in two inline
  `<script>` blocks at the bottom).
- Design tokens (colors, fonts) are CSS custom properties near the top
  of the `<style>` block, change the palette there, not per-component.
- The method library table is data-driven: methods live in a `libData`
  JS array, full guide content in a `guideContent` object (both near
  the bottom script block). To add or edit a method, edit the array
  and the corresponding file in `frameworks/method-guides/`, then keep
  both in sync, `guideContent` is what actually renders in the panel.
- The markdown-to-HTML renderer (`mdToHtml`) is intentionally minimal
  (headers, bold/italic, links, lists, tables, blockquotes, bare-URL
  auto-linking). Extend it carefully, it's hand-rolled, not a library.
- All internal navigation goes through JS (`.jump` class + `openAndScroll`,
  or the global `a[href^="#"]` delegated handler) rather than native
  anchor navigation, this was a deliberate fix for preview-frame
  sandboxes that mishandle native fragment jumps.

## Critical rule: no employer-specific content

This repo is public / portfolio material. Every skill, template, and
example must be genericized, no employer name, no named colleagues,
no internal tool names, no real business figures or strategy content.
When pulling in new source material (from Notion exports, docs,
screenshots), strip anything identifying before it lands in this repo,
including in commit messages and code comments. If source material is
too specific to genericize cleanly (e.g. a live internal strategy doc),
extract the *structure* as a blank template instead of the content, that's the pattern used for the PRD and Product Strategy templates.

## Workflow

Changes should land as real, reviewable commits with descriptive
messages, this repo is also a demonstration of PM + AI-assisted
technical workflow, so commit hygiene matters as much as the content.
Prefer small, logical commits over one large one. Open a PR for
anything that changes more than a couple of files.
