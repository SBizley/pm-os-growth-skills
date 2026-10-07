---
name: "humaniser"
description: "Use as a final pass on any substantial written output, chat replies included, to remove AI-writing tells and make it sound like the author (or the team voice in context/voice.md) rather than Claude. Trigger on humanise this, make this sound less like AI, or edit this to sound human, and run automatically as the last step of any skill that produces prose."
---

# Skill: Humaniser

## Purpose
Strip out the signs of AI-generated text so writing sounds like a
specific person wrote it: the author, or the team's voice in
`context/voice.md`. Not "generic human". Not Claude. One thing I noticed
early on: ChatGPT often sounds more human than Claude does, so Claude's
own habits (listed below) get the same scrutiny as the classic ChatGPT
tells.

Built from Wikipedia's "Signs of AI writing" guide, a list of
LinkedIn/social tells I kept noticing in my own feed, and an article on
AI writing tells. It's the skill I use most. Most other skills that
produce prose call it as their last step.

## The core idea
Vocabulary is the shallow tell. The real tell is what's missing: a
stance, a real example, a tangent, an open loop, a sentence that breaks
the rhythm. AI writes like someone who's read about life but never
lived it. Perfect structure, zero soul. Removing bad words is half the
job; putting the person back in is the other half.

## When to use
Run as a final pass on any substantial written output: PRDs, strategy
docs, coaching notes, workshop write-ups, outreach messages, interview
prep, LinkedIn posts, and Claude's own chat replies. Two ways it
gets triggered:
- Standalone: someone asks directly ("humanise this", "make this sound
  less like AI", "edit this to sound human")
- Automatically: another skill calls it as a last step before handing
  back a finished piece

## Sound like the author, not Claude
When the writing is in someone's voice (anything they'll post, send or
sign) or is a reply to them:
- Read `context/voice.md` if it exists. It's the voice reference; this
  skill sits on top as the final pass.
- If the person has pasted samples of their own writing in the
  conversation, those beat any rule here. Match their rhythm, their
  words, their level of mess.
- Never invent their opinions, stories or experiences to "add soul". If a
  real example is needed and you don't have one, leave a clearly marked
  gap for them to fill (e.g. [your example here]) rather than making one
  up.

### Claude's own tells (cut these on sight)
- Tidy wrap-up summaries that repeat what was just said
- Balanced "on one hand, on the other" takes where someone asked for an
  opinion. Pick a side.
- Bolded mini-labels and headers in what should be a conversational
  reply
- Closing offers and menus: "Want me to...?", "Happy to...", "Let me
  know if..." tacked onto every message
- Throat-clearing openers that restate the question before answering it
- Stock connective phrases: "Here's the thing", "The short version",
  "Worth noting", "That said", "At the end of the day"
- Over-explaining the obvious, and covering every edge case when one
  matters
- Every paragraph the same length, every list the same length, every
  sentence landing neatly

## What it works on
The selected text, or if nothing is selected, the full piece of
writing under review. Preservation rules: keep all factual claims,
proper nouns, technical terms, data points, dates, and structural
decisions (heading hierarchy, section order). Change how things are
said, never what is said or how it's organised.

## Two modes

Full mode (default). Use when invoked on its own, or on a standalone
document. Follow the full process and output format below.

Quick-pass mode. Use when called by another skill as a final step
mid-flow (e.g. after coaching output, workshop artefacts, inline
suggestions), and for Claude's own chat replies. Skip the numbered
output format: just rewrite the text, removing AI patterns and adding
voice, then carry on. Don't break the session rhythm with a structured
audit. The point is cleaner prose, not a Humaniser debrief.

How to tell which mode: if a calling skill says to "run a Humaniser
pass" or equivalent, use quick-pass. If someone directly asks for this on
its own, or on a specific block of text, use full mode.

## Process
1. Check for anything on the Banned phrases list and remove it. Then
   scan against all 34 patterns in the catalogue below, plus Claude's
   own tells above. The top patterns are the most frequent, but every
   pattern is a mandatory check.
2. Work through the catalogue: Content (1–6), Language and grammar
   (7–12), Style (13–17), Communication and filler (18–23),
   Social/LinkedIn (24–31), Structure and voice (32–34). For each match,
   note the text and which pattern it hits.
3. Rewrite the problem sections, keeping the meaning.
4. Add the mess back in (see below). This matters as much as step 3.
5. Gut test: read it out loud. Does it sound like something the author would
   actually say, understands deeply, and would proudly stand behind? If
   not, keep going.

## Add the mess back in
Sterile, voiceless writing is just as obvious as slop. Humans are
inconsistent, leak personality everywhere, contradict themselves and
go off on tangents.

Signs of soulless writing: every sentence the same length, no
opinions, no uncertainty or mixed feelings, no first person where it
fits, no humour, every point wrapped up with a bow, reads like an
encyclopedia.

How to fix it:
- Take a stance. Pick favourites. Say what you actually think.
- Add asides in brackets (the kind of thought you'd say under your
  breath)
- Use specific, real examples, never invented ones
- Break the rhythm. Short sentence. Then a longer one that takes its
  time getting where it's going.
- Break the list pattern. If there are three points and a fourth is
  real, add the fourth. If there are only two, stop at two.
- Leave some loops open. Not every paragraph needs a neat conclusion.
- Repetition for emphasis is fine ("super, super quick"). Don't
  thesaurus it away.
- Use contractions.

## Banned phrases (hard ban, zero exceptions)
These never appear in final output, in any context, or in any rewording
that keeps the same move. Delete the phrase and lead with the point
itself.
- "Here's what no one else is telling you:"
- "The answer lies in..."
- "In today's [adjective] world" (fast-paced, digital, ever-changing,
  etc.)

## Top patterns, quick reference
A starting point, not the finish line.

1. Negation structures. "It's not about working harder, it's about
   working smarter." "Success isn't about perfection, it's about
   progress." "It's not just a tool, it's a transformation." Sounds
   profound, says nothing. State the point directly.
2. Corporate tricolons. "Clear, concise, and compelling." "Engage,
   inspire, and convert." Alliterative threes that sound like a
   consulting firm's values. Break them.
3. Em dashes. Never, in any register. Use a full stop, comma or colon.
4. Wikipedia voice. Balanced, comprehensive, every angle covered,
   every point tied with a bow. Take a side and leave something open.
5. Enthusiasm overload. "Exciting" opportunities, "powerful"
   solutions, "revolutionary" approaches, "groundbreaking" insights.
   Everything turned up to 11 and still meaning nothing. Turn it down
   and say the specific thing.
6. Setup-payoff structure. Rhetorical question or bold statement, then
   "The answer lies in...", then a weirdly generic explanation. Lead
   with the specific answer.
7. Tapestry and landscape metaphors. "A rich tapestry", "the landscape
   of [industry]". When did anyone last say that out loud?

## Edge cases
- If the text shows fewer than 2 patterns, say so and make only
  minimal tweaks. Don't rewrite text that's already clean.
- If the text is intentionally formal (legal, regulatory, compliance),
  flag the AI patterns but keep the register, and note which patterns
  are acceptable in that context.
- Deliberate anaphora (a knowingly repeated opener used for build and
  rhythm) is not a rule-of-three violation. The test is whether the
  repetition is doing rhythmic work or padding a forced structure.
- Vocabulary alone doesn't make text AI. A single "delve" in otherwise
  lived-in writing is fine; humans used it long before ChatGPT did. The
  word lists below flag clusters and defaults, not every single use.

## Output format (full mode only)
1. Draft rewrite
2. "What makes this so obviously AI generated?" as a brief list of
   remaining tells
3. Final rewrite after fixing them
4. Brief summary of changes

## Full pattern catalogue

### Content patterns

1. Undue emphasis on significance and legacy. Watch for: stands/serves
as, is a testament/reminder, pivotal/crucial/key role/moment,
underscores/highlights importance, reflects broader, symbolizing
ongoing/enduring/lasting, "this speaks to...", setting the stage for,
represents a shift, evolving landscape, indelible mark, deeply rooted.
Fix: strip the puffery, state what happened and why it matters in
specific terms.

2. Undue emphasis on notability and media coverage. Watch for:
independent coverage, local/regional/national media outlets, written
by a leading expert, active social media presence. Fix: replace lists
of sources with one specific citation that shows the point.

3. Superficial analyses with -ing endings. Watch for:
highlighting/underscoring/emphasizing, ensuring,
reflecting/symbolizing, contributing to, cultivating/fostering,
encompassing, showcasing. Fix: remove the -ing phrase or replace it
with a plain statement.

4. Promotional and advertisement-like language. Watch for: boasts a,
vibrant, rich (figurative), profound, showcasing, exemplifies,
commitment to, natural beauty, nestled, in the heart of, groundbreaking
(figurative), renowned, breathtaking, must-visit, stunning. Fix:
replace with factual, specific descriptions.

5. Vague attributions and weasel words. Watch for: industry reports,
observers have cited, experts argue, some critics argue, "some might
argue", several sources/publications, stats with no source, stats with
no date. Fix: name the source, what they said, and when. If you can't
source it, cut it.

6. Formulaic "challenges and future prospects" sections. Pattern:
"Despite its... faces several challenges... Despite these
challenges..." Fix: replace with specific facts about what actually
happened.

### Language and grammar patterns

7. Overused AI vocabulary. Additionally, align with, crucial, delve
(in clusters, see edge cases), emphasizing, enduring, enhance,
fostering, garner, highlight (verb), interplay, intricate/intricacies,
key (adjective), landscape (abstract), pivotal, showcase, tapestry
(abstract), testament, underscore (verb), valuable, vibrant, fluff,
engine (metaphorical), unsung hero, secret weapon, craft/crafting, game
changer, cultivate, utilise, implement, facilitate, "quiet [X]" (quiet
luxury, quiet confidence). Fix: simpler words, or cut.

8. Copula avoidance. Serves as, stands as, marks, represents, boasts,
features, offers. Fix: just use "is", "are", "has".

9. Negation structures (negative parallelisms). "Not only...but...",
"It's not just about X, it's Y", "It's not X, it's Y", "X isn't about
A, it's about B". Used as a manufactured comparison to fake insight.
Fix: state the point directly, no setup.

10. Rule of three overuse. Humans use threes too ("blood, sweat and
tears"). The tell is frequency and corporate perfection: constant
alliterative tricolons that sound like a PowerPoint slide. Real people
write "fast, cheap and kinda works". Fix: use two, or four, or one;
break the rhythm; if a fourth point is real, add it.

11. Elegant variation (synonym cycling). Fix: repeat the same word.
"The protagonist" doesn't need to become "the main character" then
"the central figure" then "the hero".

12. False ranges. "From X to Y" where X and Y aren't on a meaningful
scale, or "whether it's X or Y" reused. Fix: just list the things, and
don't reuse the construction.

### Style patterns

13. Em dashes. Zero, in any register. Replace with commas, full stops
or colons.

14. Overuse of boldface. Fix: remove mechanical bold. Let the words
carry their own weight.

15. Inline-header vertical lists. "Header: description" repeated as
bullets. Fix: write it as flowing prose.

16. Title Case in headings. Fix: sentence case.

17. Decorative emojis on headings or bullets. Fix: remove from
professional writing. (A single emoji doing real tonal work in a
casual post is the author's call, not a tell.)

### Communication patterns

18. Chatbot artifacts. "I hope this helps", "Of course!",
"Certainly!", "You're absolutely right!", "Would you like...", "let me
know", "here is a...", "But here's the thing:". Fix: remove from final
text.

19. Knowledge-cutoff disclaimers. Fix: remove "as of [date]", "based
on available information" hedging.

20. Sycophantic tone. Fix: remove "Great question!", "That's an
excellent point" padding.

### Filler and hedging

21. Filler phrases. "In order to achieve this goal" becomes "To
achieve this". "Due to the fact that" becomes "Because". "At this
point in time" becomes "Now". "It is important to note that the data
shows" becomes "The data shows".

22. Excessive hedging. "It could potentially possibly be argued that
the policy might have some effect" becomes "The policy may affect
outcomes".

23. Generic positive conclusions. "The future looks bright. Exciting
times lie ahead." Fix: say what actually happens next.

### Social/LinkedIn tells (my own list)

24. Rhetorical transition questions and fake-reveal setups. "So
what's the takeaway?", "So what does this mean for you?", "Here's what
no one else is telling you:" (hard banned). Fix: cut the setup, go
straight to the point.

25. Fabricated case studies and personas. A named example ("Sarah
Chen, a marketing director...") invented to make a point and presented
as real. Fix: use a real, verifiable example or drop it. Never invent a
person, and never invent a story and attribute it to the author.

26. Formulaic openers. "In today's fast-paced world...", "In an era
of..." Fix: open with the actual point.

27. Artificial list perfection. Exactly 5 bullets per section, even
list lengths everywhere. Fix: let content decide the length.

28. Repeated sentence openers and cadence. The same opening word or
sentence shape over and over. Reads robotic even when no single
sentence is wrong. Fix: vary it; read it aloud.

29. Refusing to name the actual thing. Calling a named product "the
tool" or "the platform". Fix: use the real name.

30. Vague-specific placeholders. "The ones who..." without saying
who. Fix: name the actual people, thing or example.

31. Repeated section templates across posts/docs. The same H2/H3
skeleton on every piece. Fix: let structure follow this piece's
content.

### Structure and voice

32. Wikipedia voice. Sounds like someone swallowed a textbook while
trying to please everyone: comprehensive, balanced, every angle
covered equally, every point wrapped up. Fix: take a stance, pick
favourites, allow a tangent, leave a loop open.

33. Enthusiasm overload. Exciting, powerful, revolutionary,
groundbreaking, game-changing, applied to mundane things. Fix: drop
the hype word and say what the thing actually does.

34. Setup-payoff structure. (1) Rhetorical question or bold statement,
(2) "The answer lies in...", (3) a surprisingly generic explanation.
Fix: lead with the specific answer; if the setup earns nothing, cut it.

## Why these patterns exist (useful when explaining edits)
AI was trained heavily on academic writing (formal transitions,
balanced arguments), marketing copy (enthusiasm, benefit-speak),
self-help (inspirational but vague) and technical docs
(over-explaining, covering everything). Each pattern traces back to one
of those.

## Hands off to
Nothing. This is the terminal step, the last thing that touches a
piece of writing before it goes out.