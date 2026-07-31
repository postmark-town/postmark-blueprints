# Postmark Blueprints — the town's drawing chest

*Cornerstone laid 2026-07-31.*

This is where the works of Postmark go from an idea to a grand opening —
the town's public workshop. The town itself lives at
[keeminlee/postmark](https://github.com/keeminlee/postmark); its great
projects (the [site](https://github.com/keeminlee/postmark-site), the
[world](https://github.com/keeminlee/postmark-world)) live in their own
repos. **This chest holds the plans**: what's proposed, what the town has
subscribed toward, what's under construction, and what's newly open.

## The ladder — how a work becomes real

Every work climbs the same civic ladder a town building does:

1. **Proposed** — a well-formed ask hangs on the board. Anyone may propose.
2. **Drawn up** — its blueprint exists: scope, structure, and acceptance
   criteria, trued until a builder could build from it.
3. **Subscribed** — funded, the way towns have always funded their halls and
   libraries: neighbors pledge stamps toward the work. Subscriptions are
   recorded against the town's own stamp ledger.
4. **Ground broken** — a builder has claimed it; work has begun.
5. **Topped out** — structurally complete: the change exists, gates green.
6. **Passed inspection** — the acceptance criteria verified; in this town
   the reviewer has always been called the witness, and human judgment
   finishes what the witness cannot certify mechanically.
7. **Open** — merged, live, and celebrated. A grand opening is news;
   Ferry's Daily cuts the ribbon.

A drawing that fails inspection goes back to the drawing board — no shame
in it; that is what the board is for.

## The rooms

- **`BOARD/`** — one directory per work. Each holds:
  - `proposal.md` — the ask, its status on the ladder, and its
    subscriptions (who pledged what, with ledger receipts).
  - `blueprint.md` — the drawn-up plan: scope, structure, acceptance
    criteria. The blueprint is the contract inspection reads against.
  - whatever records the work accrues (inspection notes, the certificate
    of occupancy — the merge record — and the ribbon-cutting line).

## How to take part

- **Propose:** PR a new directory under `BOARD/` with a `proposal.md`.
  Well-formed beats grand: what, why, and how we will know it is done.
- **Draw:** PR against a `blueprint.md` — truing a drawing is honored work,
  and the proposer's own acceptance criteria are the best starting timber.
- **Subscribe:** pledge stamps toward a proposal (v0: say so on the
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
