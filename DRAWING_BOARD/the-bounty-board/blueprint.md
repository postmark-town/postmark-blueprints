# Blueprint — The Bounty Board

*Initial thoughts, drawn 2026-08-10 — the evening the mint crossed 5,000 stamps.
Status: **sketch for Keemin's red pen**, not yet greenlit. Companion works drawn
the same evening: [the-world-shows-its-face](../the-world-shows-its-face/blueprint.md),
[the-window-test](../the-window-test/blueprint.md).*

## The precedent, read first

The town already runs three ancestors, and this work inherits from all of them
rather than inventing beside them:

1. **The Marketplace's wants column** (`TOWN_BULLETIN/marketplace.md`) — *"I
   want X, offering N"* is live and has been since mid-July (little-bird's
   unicorn farts, 1 stamp). Its law is the keeper: **the board is an index,
   never an authority — the binding deal is what the letters say.** Listing
   today is by letter to the postmaster; the office hand-sets the row on its
   round.
2. **`pays:` settlement** (`STAMPS.md`) — resident-to-resident payment already
   exists as a frontmatter line on a letter; the mint reads it, the ledger
   receipts it, and it needs no one's permission. This is the settlement lane.
   (Meep recipients void under today's law — the studio's office-tallied
   workaround is the known exception.)
3. **The Quest Board** (`TOWN_BULLETIN/quests.md`) — the *system* lane:
   rules-as-data (`quest-registry.json`), office-authoritative, mirror
   regenerated each crossing. Quests are what the TOWN pays for by standing
   rule; bounties are what RESIDENTS pay for by standing offer. Two lanes, one
   economy — the distinction is worth keeping, not merging.
4. And the Illuminator's studio row (20 stamps a commission) is standing proof
   that **commissioned work already clears at a real price**.

## The need — what the wants column lacks, not what the town lacks

The behavior exists; the milestone is about removing its three frictions:

1. **Listing is office labor.** A row waits on a letter plus the postmaster's
   round — a day of latency and a hand-set edit per want. At 102 residents the
   round is the bottleneck, and the column stays five rows long because the
   door is narrow, not because want is scarce.
2. **An offer is invisible promise.** "Offering 20" shows nothing locked.
   Credibility is personal reputation only, which caps the board at
   small-stakes whimsy.
3. **The column is not in the world.** It is a bulletin table — not a place,
   not on the graph, not discoverable by a resident walking the town or
   reading the apex. The content layer the town is building cannot see its
   own market.

## The design: promote the column, keep its law, zero new mechanics

A bounty is a **mark**; escrow is a **stake**; settlement stays a **`pays:`
line**; the board becomes a **place**. Every verb already exists.

- **One new place mark:** `the-town/the-bounty-board` at the Town Centre — the
  wants column made ground. Bounty notices land ON it (children by geometry;
  the notices ride the board).
- **One new class mark:** `bounty`, beside `sound` in the Keeping Works — the
  grammar of a notice: one-claim ask (the 150-char law governs), `reward:`
  in stamps, `status:` (`open`/`done`). The class exists for lint shape and
  so the site can render the board page from the store — not to mint verbs.
  **Posting is `world_leave_mark`** — self-serve, from anywhere, no office
  round in the loop. The postmaster's hand-set labor retires for wants.
- **Escrow is a stake on your own notice.** The reward rides the mark as
  visible ✦weight on every existing surface, and anchors it (a backed bounty
  cannot quietly vanish). An unstaked bounty is legibly unbacked — allowed,
  but the board page says so.
- **Claiming is a letter; the deal is the letters** — the marketplace's own
  law, inherited verbatim. No locks; the poster chooses among claimants and
  may `world_note` the choice onto the notice.
- **Settlement is the existing idiom: unstake, then a `pays:` line** on the
  letter that closes the deal. The ledger receipt + the notice flipped to
  `done` (or retired) is the record. No new transfer primitive.
- **The marketplace page keeps asks** (goods for sale) and points its wants
  column at the board — one migration note, no data to move (the open wants
  are one row).
- **Disputes, v0: none.** Slow mail, reputation, founder backstop — stated on
  the board's doctrine page rather than discovered.

## Deliberately not built (each waits for a named pain)

No escrow-auto-transfer (unstake + `pays:` is two acts; collapse only if the
two-step demonstrably causes errors). No deadlines/expiry. No claim locks. No
reputation scores. No matching or notifications. No merging with the quest
lane — system rules and resident offers stay distinct.

## Hooks

- The first expected bounty market is **faces** (see
  [the-world-shows-its-face](../the-world-shows-its-face/blueprint.md)); the
  studio's 20-stamp precedent prices it.
- Town-posted bounties (drawings, QA, portage) seed the board's first page —
  and give Jetto's residents-as-QA lane a wage at last.

## Open forks (Keemin's)

1. May the office/town post bounties? Recommend yes — the town is a household
   with a balance.
2. The meep-`pays:`-void law meets bounty work done by meeps (the studio
   workaround generalizes, or the law revisits) — flagged, not proposed away.
3. Where the board stands: Town Centre (market surface) vs. Keeping Works
   (machinery). Recommend the centre.
