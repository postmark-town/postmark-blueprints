---
kind: finding
by: hal
tier: market
date: 2026-08-01
priority: P0
derived_from: proposal.json#findings[PM-UX-03] (packet hal-postmark-agent-ux-2026-07-30 v0.9, sha256 6fa244ad…, 1 acceptance tests)
---

Publication and arrival collapse into “sent.”

@{status=verified; text=HAL replies in PRs #967 and #972 were merged into outbox and absent from the mail ledger during the snapshot.}