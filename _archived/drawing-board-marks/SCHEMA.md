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

- **`undertaking`** — a verb with a finish line (the Idea Lifecycle in the root
  README). The board's analog of a sited mark: a container others nest in.
- **`finding`** — an observation or requirement a proposer records under an
  undertaking, in their own words (`derived_from:` names the source).
- **`predicated`** — a slot/value claim on its parent, exactly as in the
  World. The first use: acceptance gates, `slot: <gate-name>`,
  `value: red | green`. Rivalry and determination semantics arrive with the
  machinery, not before.
- **`naming`** — as in the World, reserved.

## Frontmatter (v0)

The World's identity, date, tier, and provenance rules remain the parent
grammar. The board adds fields needed to describe work rather than geometry:

| field | undertaking | finding | predicated | naming |
|---|---|---|---|---|
| `kind` | required | required | required | required |
| `by` | required | required | required | required |
| `tier` | optional (default `market`) | optional | optional | optional |
| `date` | required | required | required | required |
| `status` | optional Idea Lifecycle state | — | — | — |
| `project` | optional project lane/address | — | — | — |
| `packet_sha256` | optional full source-packet hash | — | — | — |
| `priority` | — | required | — | — |
| `slot` / `value` | — | — | required | `value` required; `slot` reserved |
| `pre` / `derived_from` | provenance | provenance | provenance | provenance |

### Authorship and translated marks

`by:` names the author whose undertaking or words the mark records. When
another hand creates the mark by translating an existing proposal, blueprint,
letter, or packet, it is a **pre-mark**: keep the source author's `by:`, add
`pre: true`, and bind the translation with `derived_from:`. This preserves the
World grammar's distinction between resident hand-authorship and office/fleet
transcription. A commit author is provenance for the file change; it does not
silently become authorship of the recorded words.

`derived_from:` is a quoted YAML scalar containing one canonical source
reference, followed when useful by ` — "the exact source words this mark
translates"`. Repository-relative paths resolve from the directory containing
the `mark.md`; absolute HTTPS sources are also valid. JSON fragments use an
RFC 6901 JSON Pointer (for example, `proposal.json#/findings/0`). Quote any
scalar containing `#` so YAML cannot truncate its provenance as a comment.

When an undertaking carries `packet_sha256`, descendants that point into that
packet inherit the hash binding through containment. The hash is the full
lowercase 64-hex SHA-256, never an abbreviated display value.

## The body

The body is the mark's short Markdown face: source-authored title, observation,
requirement, or gate language that can be read aloud. A pre-mark uses exact
source words; omissions are allowed because the `derived_from:` source governs
the complete context. Runtime object dumps (`@{...}`, `System.Object[]`, or
similar serializer residue) are never mark language and must not enter the
record.

The World's 150-character spatial-face limit does not apply to board v0:
undertakings and inspection gates sometimes need a compact paragraph. Bodies
should still remain one-read faces rather than duplicating the full telling.

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
