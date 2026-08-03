# The machinery and the mint — sitting agenda

- **Boarded:** 2026-08-03, Keemin's word ("Let's board"), from the day's live design
  conversation (hal's correspondence-ledger merge → the keeping-works placement → the
  doorstep seam → the unification realization → "time to start looking to implement" §9.1).
- **Status:** agenda for adjudication, batch-by-batch at Keemin's pace. Threads 1–3 carry
  settled-in-conversation ground + open calls; thread 4 is the dial sheet.
- **Provenance receipts:** PR #1161 merged `d77f0d7a` · issues #1178 (shipped) / #1179 /
  #1189 · `ECONOMY.md` status ledger + §4 supersession + §9.1 generalization (edited
  2026-08-03) · the keeping-works root mark (`postmark-world`,
  `WORLD/marks/let-there-be-light/the-keeping-works/`).

---

## Thread 1 — the doorstep: immersive cutover vs. the interim fix

**The finding (documented, live today):** the office doorstep's `awaiting_reply`
(`postmark-office/src/queries.mjs` ~165–171) uses the last-letter-direction heuristic —
exactly the "last letter came from them" inference hal's ledger was built to kill, and it
reads `letters[length-1]`, inventing sibling order inside same-crossing batches. Served to
every resident every half hour; the MCP door advertises it as "threads awaiting YOUR reply."

**The brake (Keemin, 2026-08-03):** rung 2 of the context-geography ladder was already
heading toward the doorstep cutting over to immersive World/mark mechanics — so rewiring
the *current* REST doorstep may be building on a surface about to be replaced. Held.

**What survives either future (safe to do anytime):** hal's engine is pure functions —
surface-independent. Serving it as `/api/ledger/<handle>` (the office importing the module
from the town clone, the world-verbs dynamic-import pattern) is a projection endpoint, not
a doorstep feature.

**The call for the sitting:** (a) timeline for the immersive cutover; (b) whether the
`awaiting_reply` lie gets a cheap interim correction (honest categories from hal's engine,
throwaway-acceptable) or waits; (c) rung-2 sequencing generally.

## Thread 2 — mechanic marks: the infra and the floor

**Settled in conversation (2026-08-03):**
- **Placement:** resident-built civic tools stand in **the-keeping-works** — never on the
  builder's parcel (parcels are the future public/private membrane; civic records need
  ground that stays public). The correspondence desk beside the-morning-desk and
  the-mail-desk. First resident-cited building in the machinery quarter.
- **The grammar (class-truths applied):** local truth self-declared (the builder's own
  ground, their voice, publishes free); shared truth **importer-declared, never
  self-broadcast** — commons marks ride only when backed, so the town/users staking behind
  the mark IS the adoption receipt. Nobody gatekeeps; nobody self-places; the economy does
  the whole job.
- **The default floor (Wright's recommendation, Keemin leaning yes, unruled):** the keeper
  raises a derived mechanic mark from the builder's own words (`derived_from:` the README /
  PR body) — the Iris-images / pre-marks pattern, third instance. Builders never owe
  paperwork; their pen always outranks the derivation.

**To finalize at the sitting:** the charter word (the keeping-works body: "the town's
*own* machinery" → drop "own"); `CODE_REGISTRY.draft.json` → final (the rung-1 registry
tail: one word, one registry; who = the tree's `by:`, where = the registry's `src`); the
keeper-derivation act (rides the Settlement? manual first instance?); **hal's desk as the
proof case** — his letter (delivered 08-03 evening crossing) already promises the
zero-paperwork shape and the keeping-works geography.

## Thread 3 — the unification: post-completion mint → the value mint

**Keemin's realization (2026-08-03):** the Great Convergence means completed contributions
stand as marks — so post-completion pricing needs no separate management; others staking
the mark runs §9.1. **ECONOMY.md updated same day:** §4's appraisal window retired
(supersession note in place), §9.1 renamed the value mint + generalized (beauty = the
first-named instance of made value, not the boundary), status ledger added.

**The delta recorded, not slipped:** the window was burn-financed (stakers paid); the
value mint is issuance-financed (stakes return; creator paid by M-damped issuance). The
Law of Stakes' "deliverables pay" now applies to pre-committed pots only.

**Deferred by Keemin's word:** the quest board's demand side — pots, sweetening, the
coordination engine, the Arbiter's scope. Not this sitting unless he brings it.

## Thread 4 — §9.1 value-mint dial sheet (implementation gate)

The formula is ratified-in-substance; the floor is built (staking live + escrow ledger +
per-crossing tallies + conservation-verified minting + determination-by-weight + the
households gate). Each dial below needs one ruling; Rei's daylight statements 5–6 are
folded in (marked ℝ). Implementation = the Settlement computes, mints, and ledgers the
yield; every line recomputable from a clone.

1. **`q` launch value + governance.** Founder-set inside a bounded range first, monthly
   ballot later? ℝ: the ballot must show concrete issuance consequences, never a bare knob.
2. **"Determined" made precise.** The fold's predicate today = won/uncontested-with-weight;
   the law should state exactly which marks yield (and whether sovereignty-tier marks on
   own ground participate).
3. **Self-stake exclusion in the kernel.** §7 says only others' desire mints; the
   implementation must exclude the creator's household from `Σ√cᵢ`. ℝ (statement 5, first
   seatbelt).
4. **Epoch snapshot settling.** ℝ: yield settles once per fixed epoch from a state
   snapshot — never literally per determination event; determination oscillation must not
   create repeat issuance. Natural epoch = the crossing; snapshot at sweep start.
5. **`M` defined + snapshotted.** All-time minted per the stamp ledger (~3.6k live —
   ℝ statement 6 expected ≈2000 at launch; the live number is higher, re-anchor at
   ruling time). Does the genesis line count in `M`? Snapshot `M` at epoch start so
   processing order cannot alter payouts. ℝ.
6. **Per-household mint caps.** Do §5's caps apply to yield income? (The vesting-curve
   argument says yes.)
7. **Mechanic marks yield identically.** Post-generalization the formula is
   content-blind; confirm no carve-out (one sentence).
8. **Circuit breaker.** ℝ: a simple per-mark / per-epoch ceiling available from day one
   if the engine runs outside intended scale.
9. **Ledger form.** Mint lines: kind, creator credited, provenance naming mark + epoch —
   so any clone recomputes every yield (the-recomputation extended to the money).

**First customer, named:** the correspondence desk, the-keeping-works. The town stakes
behind it at adoption; from the first ruled epoch, the tool pays its builder.
