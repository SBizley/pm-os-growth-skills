# Worked example: Fernway

**Fernway is made up.** The company, customers, quotes and numbers are
invented so I can show the whole system working end to end without
using anything from a real employer. The process is real: it's how I
work.

Fernway is a booking and payments app for independent fitness studios
(think a yoga or reformer Pilates studio with 3 to 10 instructors).
Studios use it to run their class timetable, take bookings and take
payment.

## The story in five steps

1. **Setup.** I ran `pm-os-setup` with the (imaginary) founder. Output:
   [`context/`](context/).
2. **The signal.** The founder said: "Studios keep asking us for no-show
   fees. Let's build them." I ran `discovery` instead of writing a spec.
   Output: [`01-discovery-brief.md`](01-discovery-brief.md).
3. **What discovery found.** No-shows weren't really the problem.
   Late cancellations were, and studio owners hated the idea of charging
   their regulars. The opportunity became "fill the spot", not "fine
   the customer".
4. **The PRD.** I drafted it with `prd-generation`:
   [`02-prd.md`](02-prd.md). Then I ran `product-review` on my own draft:
   [`03-product-review.md`](03-product-review.md). The review caught that
   I'd picked a north star the feature could game, and that I'd skipped
   the riskiest assumption (will a waitlisted customer actually take a
   spot at two hours' notice?).
5. **The decision.** We cut v1 down to a waitlist auto-fill test with
   five studios before building anything bigger. Logged in
   [`context/decisions.md`](context/decisions.md).

## Where my first instinct got challenged

Twice, and both mattered:
- **"Build no-show fees."** That was the founder's ask, and honestly it
  was mine too at first. It's what customers literally asked for.
  Discovery showed the request was a proxy for "I lose money on empty
  spots", and fees were the solution owners least wanted to use.
- **My own PRD's success metric.** I'd written "% of cancelled spots
  re-filled". The review pointed out that we could hit it by spamming the
  waitlist with notifications, while annoying the very customers studios
  most want to keep. The fix: measure re-filled spots *and* waitlist
  opt-out rate as a guardrail.

That second one is the reason I run Product Review on my own work. It's
easy to spot gaming risk in someone else's metric and much harder in
your own.
