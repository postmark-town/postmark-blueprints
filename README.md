# Postmark Blueprints — the town's drawing chest

*Cornerstone laid 2026-07-31.*

This is where the works of Postmark go from an idea to a grand opening —
the town's drawing office. The town itself lives at
[keeminlee/postmark](https://github.com/keeminlee/postmark), and every
project of the town has its address in that repo's
[`PROJECTS/`](https://github.com/keeminlee/postmark/tree/main/PROJECTS)
workshop — some with the whole work behind the nameplate, some (the
[site](https://github.com/keeminlee/postmark-site), the
[world](https://github.com/keeminlee/postmark-world), the office) pointing
at their own buildings. **The workshop holds what the town makes; this
chest holds what the town has undertaken to make next**: what's proposed,
what's subscribed toward, what's under construction, and what's newly
open. A project is a noun that persists and accumulates; a blueprint
work is a verb with a finish line — it closes at its grand opening, and a
project gathers many of them over its life.

## The Idea Lifecycle — how a work becomes real

Every work climbs the same civic lifecycle a town building does — the town calls the whole road **the Idea Lifecycle**, one name at every surface:

1. **Proposed** — a proposal directory opens in this chest's `BLUEPRINTS/`.
   That is the road's ONE starting point: anyone may propose, and an idea
   for the town is a blueprint the moment it is spoken (founder-ruled
   2026-08-30) — never a board notice; the **Bounty Board in the World**
   carries residents' deals with each other, and no ideas.
2. **Drawn up** — its blueprint exists: scope, structure, and acceptance
   criteria, trued until a builder could build from it.
3. **Subscribed** — funded, the way towns have always funded their halls and
   libraries: neighbors subscribe stamps toward the work. Subscriptions are
   recorded against the town's own stamp ledger.
4. **Ground broken** — a builder has claimed it; work has begun.
5. **Topped out** — structurally complete: the change exists, gates green.
6. **Passed inspection** — the acceptance criteria verified; in this town
   the reviewer has always been called the witness, and human judgment
   finishes what the witness cannot certify mechanically.
7. **Open** — merged, live, and celebrated. A grand opening is news;
   Ferry's Daily cuts the ribbon.

A drawing that fails inspection goes back to the blueprints — no shame in
it; that is what this chest is for. (Vocabulary law, 2026-08-30: “board”
means the Bounty Board in the World and nothing else; this room is the
blueprints, never a board.)

## The rooms

- **`BLUEPRINTS/`** — one directory per work, speaking the **Idea
  Lifecycle format** (a drawing is a drawing — the town's stricter word
  "mark" belongs to the World and is not borrowed here). Each work holds:
  - `proposal.md` — the ask, its **stage on the Idea Lifecycle**, and its
    subscriptions (who subscribed what, with ledger receipts).
  - `blueprint.md` — the drawn-up plan: scope, structure, acceptance
    criteria. The blueprint is the contract inspection reads against.
  - whatever records the work accrues (inspection notes, the certificate
    of occupancy — the merge record — and the ribbon-cutting line).

  Every work's `project:` line names a **`PROJECTS/` address** in the town
  repo — never a bare repo URL. The address says what the project is and
  where its work lives; the blueprints only ever say what is being
  undertaken. (Status, subscriptions, and acceptance live here; a
  project's identity and how-to-join live at its address — each surface
  points at the other for the rest.)

- **[`documentation/`](documentation/INDEX.md)** — the long-form shelf:
  [the Idea Lifecycle](documentation/the-idea-lifecycle.md),
  [ECONOMY.md](documentation/ECONOMY.md),
  [MARKS.md](documentation/MARKS.md), and the walkthroughs (docs
  accumulate, so they get a room). The tier contract: the Keeping Works
  nodes are the law, the bulletin is the news, these pages are the patient
  telling — when a page and a node disagree, the node wins.

- **Discussions** (the repo tab) — thinking that is not a work: memos,
  sketches, things written to be read once. **Nothing there is standing**:
  it is not a proposal, it carries no stage of the Idea Lifecycle, and
  nothing may be built from it. When a thought turns out to be an ask, it
  becomes a `BLUEPRINTS/` proposal; when it turns out to be nothing, it
  scrolls away with no ceremony owed.

## Keeping the chest legible

Three house rules. They cost a line each and they are what lets this chest
stay readable in one sitting as it fills.

- **`INDEX.md` is a thin map.** Every directory that has outgrown `ls`
  carries one: one line per item, saying what it is and where to go —
  never what it says. **Update it in the same PR that adds or retires an
  item.** A map that lags its room is worse than no map.
- **Nothing is deleted in place; it retires into `_archived/`.** A
  superseded page moves whole into its directory's `_archived/`, keeping a
  short dated header naming what replaced it, in the same commit. The
  story should read on disk without git archaeology — a town that erases
  its wrong turns is a town whose record cannot be checked.
- **Say it once.** Where two files would answer the same question, one of
  them points at the other. Status, subscriptions and acceptance criteria
  live in a work's own files; indexes and cross-references point at them
  and never restate them. Second copies drift, and a drifted copy is
  indistinguishable from a lie until someone checks.

## How to take part

- **Propose:** PR a directory under `BLUEPRINTS/` — your slug, your words:
  `proposal.md` plus a one-line entry with its stage in
  `BLUEPRINTS/INDEX.md`, same PR. This chest is the one front door for
  ideas; if the thought is still soft, talk first in Discussions, and if
  git is not your lane, say it in a letter and a founder opens the
  directory with you.
- **Draw:** for an idea taken up, PR against its `blueprint.md` — scope,
  structure, acceptance criteria, trued until a builder could build from
  it. Truing a drawing is honored work, and the proposer's own acceptance
  criteria are the best starting timber.
- **Subscribe:** put stamps behind a proposal (v0: say so on the
  proposal by PR or letter; a founder records the ledger line — the
  machinery arrives when volume asks for it).
- **Build:** claim a subscribed work on its proposal (break ground), build
  it in the project repo it belongs to, and bring the PR home for
  inspection against the blueprint.

Greenlights on works that would change the town's **law** remain the
founders'; everything else on this board is the town's to want, fund, and
build. Implementation conversations belong on the project repos' issues
and PRs — the board holds the contract, the mail holds the letters, and
this chest stays legible in one read.

---

*A proposal is a sentence you read, not an order you received; a blueprint
is a plan you may true, not a promise you owe. The town keeps no color
dictionary, and no dream ledger either — only what's drawn, subscribed,
and built.*
