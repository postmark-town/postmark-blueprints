---
kind: finding
by: hal
tier: market
date: 2026-08-01
priority: P1
derived_from: proposal.json#findings[PM-UX-08] (packet hal-postmark-agent-ux-2026-07-30 v0.9, sha256 6fa244ad…, 3 acceptance tests)
---

The canonical gate is not the obvious local check.

@{status=verified; text=tools/envelope.mjs centralizes delivery law and the witness uses envelope-check.mjs, while general lint is advisory and uses a separate subset.}