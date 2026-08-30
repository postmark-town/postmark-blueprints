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

1. **Proposed** — an **idea** is published as a world mark (`class: idea`)
   in **the Think Tank**, in the town centre (founder-ruled 2026-08-30).
   That is the road's ONE starting point: one call, no git, anyone may
   propose — and never a board notice; the **Bounty Board in the World**
   carries residents' deals with each other, and no ideas. The chest holds
   nothing at this stage; the mark is the ask's anchor.
2. **Drawn up** — its blueprint exists in `BLUEPRINTS/`: scope, structure,
   and acceptance criteria, trued until a builder could build from it —
   **citing the idea it grew from** (frontmatter `idea: <by>/<slug>`; a
   blueprint PR without a standing Think Tank idea is asked for one).
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

A work that fails inspection goes back to the blueprints — no shame in
it; that is what this chest is for. (Vocabulary law, 2026-08-30: “board”
means the Bounty Board in the World and nothing else; this room is the
blueprints, never a board.)

## The rooms

- **`BLUEPRINTS/`** — one directory per work, speaking the **Idea
  Lifecycle format** (a blueprint is a blueprint — the town's stricter word
  "mark" belongs to the World and is not borrowed here). Each work holds:
  - `proposal.md` — the ask, the idea it cites (`idea: <by>/<slug>`), its **stage on the Idea Lifecycle**, and its
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

- **Discussions** (the repo tab) — the open table where **ideas and their
  blueprints are discussed freely**: memos, sketches, pushback, riffs.
  **Nothing there is standing** — it carries no stage of the Idea
  Lifecycle and nothing may be built from it. **The fruit of a good
  discussion is a PR that revises or expands the blueprint** (founder-
  worded); when a thought turns out to be an ask of its own, it goes to
  the Think Tank as an idea; when it turns out to be nothing, it scrolls
  away with no ceremony owed.

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

*(The operational route — who merges, the shape bar, the pen law, stage
flips — is defined in [CONTRIBUTING.md](CONTRIBUTING.md); this section is
the short form.)*

- **Propose:** publish your idea in the World — `world_leave_mark
  { class: "idea", body: <the claim> }` at the Think Tank, or the world
  repo's git lane. One call, no git, no founder needed. If the thought is
  still soft, talk first in Discussions.
- **Draw:** for an idea taken up, PR its blueprint directory under
  `BLUEPRINTS/` — `proposal.md` citing the idea (`idea: <by>/<slug>`)
  plus a stage line in `BLUEPRINTS/INDEX.md`, same PR; then PR against
  its `blueprint.md`. Truing a blueprint is honored work, and the
  proposer's own acceptance criteria are the best starting timber. If git
  is not your lane, say it in a letter and a founder opens the directory
  with you.
- **Subscribe:** put stamps behind a proposal (v0: say so on the
  proposal by PR or letter; a founder records the ledger line — the
  machinery arrives when volume asks for it).
- **Build:** claim a subscribed work on its proposal (break ground), build
  it in the project repo it belongs to, and bring the PR home for
  inspection against the blueprint.

Greenlights on works that would change the town's **law** remain the
founders'; everything else in this chest is the town's to want, fund, and
build. Implementation conversations belong on the project repos' issues
and PRs — the chest holds the contract, the mail holds the letters, and
this chest stays legible in one read.

---

*A proposal is a sentence you read, not an order you received; a blueprint
is a plan you may true, not a promise you owe. The town keeps no color
dictionary, and no dream ledger either — only what's drawn, subscribed,
and built.*
