# PRD: Waitlist auto-fill (draft v1, before review)

_Skill: prd-generation · Fictional example · This is the draft that went
into Product Review. See 03 for what changed._

## Overview
- **Vision:** a late cancellation shouldn't cost a studio money.
- **Problem:** about 11% of bookings are cancelled late, and most of
  those spots stay empty even when a waitlist exists.
- **Users:** studio owners (buyers), waitlisted customers (receivers)
- **Success metric:** % of late-cancelled spots re-filled

## Epic 1: Auto-offer freed spots

**AF-1: Offer a freed spot to the waitlist**
As a waitlisted customer, I want to be offered a spot as soon as one
frees up so that I can join a class I wanted.

Acceptance criteria:
- When a booking is cancelled, the first person on the waitlist gets a
  push notification and email within 1 minute
- They have 30 minutes to accept before it moves to the next person
- Payment is taken from their saved method on acceptance
- If nobody accepts by class start, the spot stays empty

Priority: Must Have · Effort: M

**AF-2: Studio controls**
As a studio owner, I want to turn auto-fill on per class type so that
I stay in control of my timetable.

Acceptance criteria:
- Toggle per class type, off by default
- Owner sees which spots were re-filled in the daily summary

Priority: Must Have · Effort: S

## Epic 2: Smart waitlist (Should Have)
Rank the waitlist by likelihood to accept (past behaviour, distance,
time of day).

## Non-functional
- Notification sent within 60 seconds of cancellation (p95)
- No double-booking under concurrent acceptances

## Risks
- Payment processor rules on charging saved cards without a fresh
  confirmation. Mitigation: check with processor before build.
