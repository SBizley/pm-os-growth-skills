# context/

This folder is the brain. Everything else in pm-os is method; this is the
stuff that's actually true about *your* product right now.

Every skill reads these files before it asks you anything, and offers to
write back to them when it learns something. So the PRD skill already
knows who your customers are, the strategy skill already knows what you
decided last month, and nobody has to re-explain the product to Claude
(or to the new engineer) for the fifth time.

| File | What lives here | Who updates it |
|---|---|---|
| `product.md` | What the product is, who it's for, how it makes money, what's live | PM, after anything ships |
| `customers.md` | Segments, personas, jobs to be done, real quotes | Anyone who talks to a customer |
| `metrics.md` | North star, the metric tree under it, current baselines | PM + whoever owns data |
| `bets.md` | What we're working on now, next and later, and why | PM, at planning |
| `decisions.md` | Every decision that matters, with the reasoning | Whoever made the call |
| `glossary.md` | The words we use, so docs and code use the same ones | Everyone |
| `voice.md` | How we write, so the Humaniser can make docs sound like us | PM or founder, once |

## Rules I'd keep

- **Short beats complete.** A half-page that's true is worth more than ten
  pages nobody updates.
- **Date anything that'll go stale.** "Activation is 34% (Sept 2026)" not
  "activation is 34%".
- **Facts here, opinions in docs.** If it's a bet or a hypothesis, it goes
  in `bets.md` with a confidence level, not in `product.md` as gospel.
- **Never put secrets in here.** No customer names you don't have
  permission to use, no credentials, no salaries. If the repo's private
  that helps, but treat it like it isn't.

Run the `pm-os-setup` skill to fill these in from scratch. It takes about
45 minutes with a founder.

For a filled-in example, see `examples/fernway/context/`.
