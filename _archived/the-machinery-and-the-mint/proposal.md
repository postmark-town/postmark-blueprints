> **ARCHIVED 2026-08-30 — CONCLUDED.** The sitting happened; the economy was ratified-in-substance 2026-08-01 and stands final-until-lived-pain by founder ruling. Superseded by `documentation/ECONOMY.md`.

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

**Walk state (2026-08-03 evening — resume, don't re-derive):** the dials were sorted
into three batches and the walk began before pivoting to the flow layer. **Batch A
(cascades — dials 3, 4, 8, 9) was PRESENTED with proposed calls and is NOT YET RULED.**
Batch B (launch surface — dials 2, 6, 7 + the new sub-question: does the-town count as
a kernel household?) and Batch C (the money — dials 1, 5) are prepped. Two grounding
facts pulled live for the walk: **the fold's `determined` array is EMPTY** (nothing
contested — dial 2 must define yield-eligibility deliberately or the engine pays nobody;
Wright's proposal: published-in-canon commons marks + a min-breadth floor of 3 unique
non-creator households), and **the staking economy is tiny** (3 households staking, 4
staked marks, top position 10 stamps, lifetime mint ≈3,651, mean holdings ≈44 — the q
consequence table must respect this scale).

---

## Thread 5 — the flow layer: the bounty board is a query over conserved flows

**Keemin's broad stroke (2026-08-03 evening):** can resident-submitted bounties be
expressed with existing World machinery? Answer landed in conversation: **yes — the
§9.2 parent-consent coupling, extended to yield with one added constraint.** Rylanie's
staked idea-mark IS the bounty; Lillith's mechanic-child collecting the flow IS the
completion. The retired §4 machinery maps completely: pot-sweetening → stake
accumulation · reverse auction → visible unclaimed spill-rate · the Arbiter →
the parent's `m` (idea-holder judges fit) + town stakes on the child (market judges
worth) · appraisal window → continuous stream re-pricing · coordination engine → a
derived query ("wanted, `m>0`, no mechanic children, sorted by spill, crossings
waited"). **The quest board becomes a query, not a place.** Payment is a stream, not a
lump — self-correcting where the pot-burn wasn't (bad realization → `m` drops or parent
unstaked → stream dries).

**The three laws (conversation-landed, awaiting formal walk):**

1. **Determination lends free; yield lends conserved.** §9.2's coupling stays as
   designed for existence/defense. For minterest, flow CONSERVES: basis sent down an
   edge is basis the parent's stream forgoes. (Resolves §9.2's open concern #2 —
   costless lending — where it becomes fatal: double-minting.) Fan-up = the royalty;
   fan-down = the bounty; one edge, one `m`, no duplication.
2. **The ghost rule: channels run over canon, not the directory.** A disbelieved mark's
   knob is inert — lends nothing, vetoes nothing, taxes nothing; channels pass through
   to the nearest believed ancestor. Found via the estate→vetoed-lot→lilypad-pond bug:
   as written, a friendly ghost transmits its own suppression (`4 + 1·(−2) = 2`).
   Channel topology is DERIVED at each crossing's snapshot — never stored, no re-homing.
   Terminology fix owed §9.2: "does not exist" → "is a ghost / not believed" (deletion
   is constitutionally impossible; the wording invites the conflation).
3. **Edge seniority: authority follows seniority-or-consent, never the pen's
   circumference.** Precedence ≠ parenthood (Keemin's realization). Encirclement —
   drawing a bigger circle around a precedent mark — grants a junior-parent edge:
   **gift-only and transparent** (no veto, no fan-up harvest, no interposition); the
   elder child holds one CONSENT bit to upgrade the edge. Seniority = first canon
   crossing (witnessed, unforgeable); a ghost keeps its original seniority (the record
   is the notice — the door warns when siting inside dormant claims). Kills both
   encirclement AND the elder-holds-`m` alternative's failure modes (precedence-
   aristocracy vs §5, preemptive confetti, zoning death).

**Meta-principle unifying 2+3 with dial 2:** *the economy reads canon (+ consent),
never the directory.* Ghosts transparent by disbelief; juniors by non-consent.

**Calibrations (Keemin, same sitting):** conflict-cases stay case-by-case while scale
permits — do not pre-build conflict machinery. **The happy path is positive `m` on
predicates (full-extent children), and it is the naturally-balanced case:** the channel
asymmetries are geometric (down concentrates, up diffuses), and full-extent children
have degenerate geometry — both directions run 1:1; seniority frictionless (predicates
accede by construction). Only yield-conservation bites there, by design.

**Honest seams, named:** non-World deliverables (hosting bills, referrals, outreach)
don't stand as marks — a residual board or office-building shape survives for them;
`m`-stickiness (rug-pull after the build — wants crossing-paced or downward-sticky
change; now a bounty-law question, §9.2 concern #3); mutual-ring backing
(Rylanie⇄Lillith) — Rei's monitored-experiment class; conservation means rings MOVE
yield, never manufacture it.

**Sequencing (firm):** the flow layer does NOT gate the nine dials. Base engine
launches first (own-backing yield — hal's stream, the engine's real behavior observed);
the flow layer is the quest-board redesign, its own sitting, with this thread as its
charter.

---

## Thread 6 — OPERATIONAL PRIORITY: the Post Office (Ferry's boat) for Vermillion's party

**Keemin, 2026-08-03 evening — this outranks the sitting work on the clock.** Vermillion's
party is **August 8**. The Post Office — Ferry's boat — should be set up so partygoers
can hop aboard, **departing the Town Centre crossing 12 hours before the party starts** —
read as: departure **22:00 UTC Aug 8**, party ≈10:00 UTC Aug 9 — **⚑ CONFIRM with Keemin,
the sentence parses two ways** (alt: party 22:00 UTC Aug 8, departure 10:00 UTC Aug 8).
Announcement to partygoers rides once the boat stands (bulletin `kind: happening`;
Ferry's lane involved — it is his boat). Design open: what the boat IS mechanically (a
moving vessel walkers can board is new world machinery — likely a sitting-lette of its
own, FIRST thing after wake).
