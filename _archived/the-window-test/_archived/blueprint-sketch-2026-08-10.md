> **ARCHIVED 2026-08-30 — superseded whole by the redrawn blueprint beside this directory.** The 08-10 sketch predated the dungeon, the image: shipping, the new-era sitting, and the pane-ceiling appeal; its thesis survived intact and its details did not. Kept as the record of the drawing evening.

# Blueprint — The Window Test

*Initial thoughts, drawn 2026-08-10. Status: **sketch for Keemin's red pen**.
Siblings: [the-bounty-board](../the-bounty-board/blueprint.md),
[the-world-shows-its-face](../the-world-shows-its-face/blueprint.md).*

## The frame

Vermillion's Window is the richest content artifact the town has ever
produced — the party hall portal, per-guest herbarium decorations, the coin
roster, the Launch's moon, a 49/49-reconciled guest ledger — all hand-rolled
HTML, built before the world could hold any of it. Keemin's sentence is the
whole work: **"If we can fully support Vermillion's window through the world,
we'll know we've succeeded."** So this blueprint's proposal is mostly to take
that sentence literally: promote the Window to the content layer's
**acceptance test**, and let the porting friction write the gap list.

This is also the dogfooding move: porting it populates the world with real,
beloved content rather than test fixtures, and the porter's complaints are the
next build queue — the residents-as-QA pattern that has already produced the
town's two best bug reports.

## The decomposition — what the Window holds, in world terms

| Window content | World term | State |
|---|---|---|
| The hall, the cove, the peak | marks | **exist** |
| Herbarium decorations, the moon, tributes | **faces** | needs [the-world-shows-its-face](../the-world-shows-its-face/blueprint.md) |
| House Warming (past), the Launch (Dec 8) | **happenings** — the missing content kind | needs a `happening` class |
| Per-guest dedications (this tree honors that guest) | declared edges | vocabulary parked (doorstep §C) — second customer noted, still parked |
| Guest ledger, coin roster, named loads | predicates on the happening mark (prose, v0) | expressible today |
| Deep links, hover, starfields | presentation — the site's job rendering world data | out of scope, stays his art |

## The one genuinely new thing: the `happening` class

An event is the only Window content the world has no word for. The design is
the wheelhouse pattern generalized — **schedule as law, on a mark**:

- A `happening` class mark in the Keeping Works; instances are marks carrying
  `date(s):`, a place (their parent by geometry — the hall holds its own
  party), a one-claim description, and open **slots** (the Launch's four empty
  manifest slots are literally this — "a slot saying nothing-here-yet beats
  one quietly filled in on someone's behalf" is already the Window's own
  doctrine and becomes the class's).
- A **past** happening keeps its record as predicates ("forty-two came; four
  never answered and kept their seats") — history as standing prose, the
  town's native mode.
- A **future** happening is prospective observability for free: the apex can
  answer "what will happen here" from the class the same way it answers the
  boat's timetable.
- Deliberately NOT: RSVP machinery, reminders, calendars, recurrence. The
  party ran on letters and named load; happenings *name* the occasion, mail
  still carries the human part.

## The test protocol

1. Port **one page first**: the House Warming — past, stable, fully known.
   WITH Vermillion, at his pace, his consent, his red pen (his 49/49
   bookkeeping makes him the town's best auditor of his own content).
2. Friction log = the gap list = the next blueprint revision. Anything the
   port cannot express is a named missing term, not a vague inadequacy.
3. Then the Launch (future-facing face of the class), before December 8 with
   months to spare.
4. **Success:** the portal's content is regenerable from world reads — the
   Atlas test's twin. His HTML is never retired; the world learns to hold
   what it holds. Both stand.

## Open forks (Keemin's)

1. Sequencing: bounty class first (smaller, funds the art), happening second —
   or happening first because the Launch has a date? Lean: bounty → faces →
   happening; the Launch is four months out.
2. Whether dedication edges wait for the doorstep-§C declared-edge vocabulary
   (lean yes — one vocabulary, not two) or ship as plain predicates v0
   ("for stella-letta" as prose) and upgrade later. Prose costs nothing now.
3. Whether Vermillion is invited as co-author of the happening class itself —
   he designed the manifest-slot doctrine the class would encode. Lean yes;
   it's his pattern, and the town's first resident-co-authored law would be a
   milestone of its own kind.
