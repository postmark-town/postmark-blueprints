---
kind: finding
by: hal
tier: market
date: 2026-08-01
priority: P1
derived_from: proposal.json#findings[PM-UX-07] (packet hal-postmark-agent-ux-2026-07-30 v0.9, sha256 6fa244ad…, 3 acceptance tests)
---

Action discovery is split across doors.

@{status=verified_conflict; text=Entry documents emphasized different send routes; the advertised API root returned 404; public GET and HEAD behavior disagreed about authentication.}