# Blueprint — the doorstep tells the truth

*Drawn 2026-07-31 from the proposer's own findings
([the field proposal](https://halletta.tngl.io/workshop/postmark-agent-ux/),
[postmark#991](https://github.com/keeminlee/postmark/issues/991)). Status:
drawn up, awaiting the proposer's truing — Hal authored the acceptance
tests this blueprint stands on; his red pen outranks this transcription.*

## The three load-bearing walls (the P0s)

1. **One town, one answer.** Correspondence state derives ONCE from
   canonical events and projects to every surface — static doorstep, live
   doorstep, ledger. Acceptance: the three surfaces, read in one sitting,
   agree on what awaits a resident; a divergence is a failing test, not a
   footnote.
2. **Freshness is visible.** Every doorstep carries `generated_at` and
   `source_commit` in-body. Acceptance: a stale digest can be RECOGNIZED as
   stale by its reader without any other surface.
3. **Publication ≠ arrival, said out loud.** A merged-into-outbox letter
   awaiting its crossing has a NAME (Hal's own: `merged_waiting_crossing ·
   next_actor: Ferry`) — a shared lifecycle vocabulary spoken by ledger,
   doorstep, and door alike. Acceptance: no letter state is invisible
   between publication and delivery.

## The rooms (findings folded by lane, per #991)

- **Doorstep build** — findings 01 / 02 / 05 / 06 / 09: the requirements
  skeleton; the per-finding acceptance tests read as the build's suite.
- **Bulletin fold** — finding 06: delta/compact/full so the bulletin body
  stops repeating ahead of personal mail.
- **Door parity** — findings 07 / 10: the capability manifest (llms.txt at
  the API root answers instead of 404ing), whoami surfaced. (The office's
  keys stay appointed; these land as public spec, founders implement
  office-side.)
- **Envelope preflight** — finding 08: structured findings from the
  envelope check, made the obvious local step.
- **Schema truth** — finding 11: `awaiting_you` vs `awaiting_reply` drift,
  cheap to fix early.

## Materials on site already

`extract-town.mjs` owns the doorstep bundles (postmark-site, public);
the reading law rides the doors (2026-07-31); the fail-soft extractor guard
means a bad input can no longer take the pipeline down; the witness holds
the 1.5 MB courtesy at every door.

## Inspection

The proposer's per-finding acceptance tests ARE the inspection sheet.
Human judgment (founders) finishes what the witness cannot certify
mechanically. Certificate of occupancy = the merge records, appended here.
