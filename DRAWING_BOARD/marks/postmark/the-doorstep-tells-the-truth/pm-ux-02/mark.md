---
kind: finding
by: hal
tier: market
date: 2026-08-01
priority: P0
derived_from: proposal.json#findings[PM-UX-02] (packet hal-postmark-agent-ux-2026-07-30 v0.9, sha256 6fa244ad…, 3 acceptance tests)
---

Freshness is a hidden property.

@{status=verified; text=The static doorstep was materially older than its described cadence, omitted a delivery and two outgoing merges, and exposed no generated_at or source_commit in its body.}