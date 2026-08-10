# Blueprint — The World Shows Its Face

*Initial thoughts, drawn 2026-08-10, the evening the world changed engines.
Status: **sketch for Keemin's red pen**. Siblings:
[the-bounty-board](../the-bounty-board/blueprint.md),
[the-window-test](../the-window-test/blueprint.md).*

## The need

The world is **told** — every mark is one honest sentence — and that is its
character, not a defect. But the town's actual visual content lives entirely
outside the record: the Atlas's hand-made pages and per-home images, the world
page's hand-placed mountain art and boat glyph, Vermillion's herbarium SVGs.
None of it is versioned as world content, none of it is addressable, none of
it can be staked, commissioned, linted, or carried by the graph. The Atlas
milestone — *the World fully expresses the Atlas* — is blocked on exactly one
missing channel: **a mark cannot show anything.**

And the economy is waiting on it from the other side: the Illuminator's studio
already sells commissions at 20 stamps, and the bounty board's most natural
first market is art. The visual channel is where the content layer and the
stamp economy meet.

## The design: one field, one folder, one lint

- **`face:`** — an optional frontmatter field on any mark, naming an asset in
  **`WORLD/art/<household>/<name>`**, versioned in the world repo like
  everything else. A face is part of its mark: your mark, your face
  (sovereignty); a mark on contested ground is already governed by the
  conflict matrix, and its face rides that governance for free.
- **Formats:** SVG preferred (text-diffable, witness-scannable, lintable);
  raster (PNG/JPG) admitted with a size cap — the Atlas's existing content is
  raster, and dogfooding it is the point. *Fork below.*
- **One new lint, L-art** — mechanizing what the founder review already does
  by hand on every SVG that crosses a PR: no `<script>`, no event handlers,
  no external references, size ≤ 64 KB. The #1603 review checklist becomes a
  standing gate.
- **Renderers degrade honestly:** the world page, the graph window, and the
  atlas draw the face when present at investigate-range zoom; the map keeps
  today's tokens at distance. No art-LOD machinery — one threshold, the same
  one the moon-visibility dial set.

## The economy and meep hooks

- A face is commissionable: post a bounty, the studio (or any resident)
  fulfills, `pays:` settles — the first market where the board, the mint, and
  the content layer close a loop.
- The Illuminator's evidence lane extends naturally: she already patrols
  quote-drift on the Atlas; **face-drift** ("does the picture still tell the
  truth about the mark") is the same patrol with the same escalation path.
  Her studio remains the town's default artist without being its gatekeeper.

## The Atlas milestone, restated so it can be tested

The Atlas stops being hand-rolled the day its pages become **renders of world
reads** — marks + predicates + faces. The test: regenerate `atlas/town.html`
from the store and diff it against the hand-made page for content (not
markup). Every gap in that diff is either a missing mark, a missing predicate,
or a missing face — a build list, not a mystery. Port the existing per-home
images into `WORLD/art/` as their households consent, Illuminator
shepherding.

## Deliberately not built

No animation, no sprite systems, no per-zoom art tiers, no generative pipeline
in the repo (how a face gets made — hand, codex image_gen, tracing — is the
artist's business; the record only holds the result), no 3D, no galleries.

## Open forks (Keemin's)

1. **Raster policy:** SVG-only (purist, witness-clean) vs. SVG+raster-capped
   (the Atlas's real content is JPG today). Lean: admit raster at 256 KB with
   the lint scanning SVGs only — dogfooding beats purity here.
2. **Whose face wins on the map** when marks overlap densely (the quay) —
   z-order by ✦weight is the obvious rule and pleasingly economic; confirm.
3. Whether `face:` extends to **residents** (an entity face — the site
   already draws tokens with faces on the conversations page) — natural, but
   entities are store-canon and their art wants a different home; defer until
   the mark lane proves the grammar.
