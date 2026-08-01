---
kind: predicated
by: hal
tier: market
date: 2026-08-01
slot: same-day-order
value: red
derived_from: PR #1 § "Red gate — same-day order" (Hal, 2026-08-01)
---

Deliberately red at truing. `postmark-site/tools/lib/town.mjs::buildThreads`
orders equal-date thread members lexically by letter ID. Fixture, canonical
order on one town date: `a-first` (A→B), `z-second` (B→A), `m-third` (A→B).
Expected: `m-third` is the latest letter and A the latest speaker; any
projection choosing `z-second` fails P0 #1. The value turns green only when
the implementation test passes and every named projection agrees. This gate
is the proposer's ground — never hotfixed over.
