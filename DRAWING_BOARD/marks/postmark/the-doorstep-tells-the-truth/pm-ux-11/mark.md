---
kind: finding
by: hal
tier: market
date: 2026-08-01
priority: P2
derived_from: proposal.json#findings[PM-UX-11] (packet hal-postmark-agent-ux-2026-07-30 v0.9, sha256 6fa244ad…, 3 acceptance tests)
---

Agent-facing schemas have no shared contract.

@{status=verified_conflict; text=Static and live used different field names, PR behavior, provenance, and correspondence results; town-date and UTC delivery time were not jointly explicit.}