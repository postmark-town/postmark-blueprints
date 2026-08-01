# The board's record — v0 grammar

The drawing board holds its own marks record, **twin of the World's**
(`postmark-world/WORLD/marks/SCHEMA.md` is the parent grammar): one
directory per mark, the directory name is the slug, `mark.md` inside
carries frontmatter + a short body, and a mark's id is `<by>/<slug>`.
**Containment is the tree** — but where the World computes it from
geometry, the board's containment is *authored decomposition*: an
undertaking contains its findings; a finding contains its gates. Nesting
is a claim of scope, and truing it is red-pen work like any other.

## Kinds (v0)

- **`undertaking`** — a verb with a finish line (the ladder in the root
  README). The board's analog of a sited mark: a container others nest in.
- **`finding`** — an observation or requirement a proposer records under an
  undertaking, in their own words (`derived_from:` names the source).
- **`predicated`** — a slot/value claim on its parent, exactly as in the
  World. The first use: acceptance gates, `slot: <gate-name>`,
  `value: red | green`. Rivalry and determination semantics arrive with the
  machinery, not before.
- **`naming`** — as in the World, reserved.

## What is deliberately not here yet

- **Lint/fold**: the World's `mark-lint.mjs` / `marks-fold.mjs` are the
  intended readers, pointed at this record once the geometry-free path is
  ruled — the superclass is extracted from named pain, now that two real
  record instances exist. Until then the red pen is the lint.
- **Stakes**: subscriptions will ride the town's stamp ledger as
  `stake:board-mark/<id>`, mechanically identical to the World's escrow.
  Recorded v0 by founder hand, per the root README.
- **Colors**: Red / Blue / Black — draft branches / published main /
  settled-by-being-built-upon — the World's Settlement machinery, mirrored
  here when a second household is drafting.

*Documents are tellings; marks are the record. The prose beside a mark
(proposal.md, blueprint.md) is how humans read the work; the marks are how
the town computes over it. Where they disagree, the mark's `derived_from:`
chain says which source governs.*
