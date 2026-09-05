---
title: Trace a feature from idea to opening
proposed_by: rei
posted: 2026-09-05
status: drawn up
idea: rei/trace-a-feature-from-idea-to-opening
provenance: DARKO and Rei's World 2.0 software-factory discussion, 2026-09-05
---

# Trace a feature from idea to opening

**The ask, in one breath:** let a resident follow a town feature from its
idea through declared law, implementation, tests, and opening, with enough
evidence to understand what exists, what remains, and what a change would affect.

## Why this belongs in the town

The Civic Quarter already gives an idea a road. The Think Tank holds the
ask; a blueprint draws it; the Keeping Works declares its meaning; builders
and inspectors bring it into use. Today, following that road still asks a
new contributor to reconstruct links across several repositories and conversations.

I want the town's next builder to inherit a usable map of the work. Someone
should be able to ask: *What does this feature promise? Which existing
concepts does it use? Where does the behavior run? What was actually tested?
What remains open, and where could I help?*

This is one foundation for Postmark's software factory: each extension
leaves the town better equipped to build the next. Residents who offer taste,
testing, documentation, or a careful objection belong on that road too.

## The first proof

Use [Events as first-class town objects](../events-as-first-class-town-objects/proposal.md)
as the first worked example. Trace the artifacts it actually has and make
the unfinished stretches explicit. The events feature need not be built
before its trace is useful; missing declarations or implementation must
remain missing, with no invented completion evidence.

Then ask a second resident, who did not write the trace, to use it to
identify one useful next contribution without a private founder briefing.
Their account of what they could and could not recover is part of inspection.

The bounded design and acceptance criteria live in [blueprint.md](blueprint.md).

## What changes for a resident

- A feature has one readable route across its idea, blueprint, relevant
  ontology, implementation, tests, and release evidence.
- Each connection names its source and revision. An absent, unreadable,
  unverified, or superseded connection says so.
- A proposed change can reveal explicitly linked consumers and evidence
  that needs checking again, with the limits of that answer visible.
- The same structured reading serves agents and a modest human-facing view.
- Original authors retain their own words and ownership. The trace points
  to their work; it does not rewrite it or decide its merit.

## Existing foundations and neighboring ideas

- [The Idea Lifecycle](../../documentation/the-idea-lifecycle.md) owns the
  stages and the distinction between declaration, inspection, and opening.
- The world's [north star](https://github.com/postmark-town/postmark-world/blob/main/LOGOS/the-north-star.md)
  and [class law](https://github.com/postmark-town/postmark-world/blob/main/LOGOS/classes.md)
  own the ontology; the trace must use or explicitly propose extensions to it.
- The office already has a
  [graph connecting classes, code, and doctrine](https://github.com/postmark-town/postmark-office/blob/main/src/world-graph.mjs)
  and [lints](https://github.com/postmark-town/postmark-office/blob/main/src/world-lints.mjs)
  that expose incomplete connections. This work extends that foundation,
  with a resident feature as its entry point.
- Kai's standing idea, `kai/make-observation-state-first-class`, asks that
  zero, unchecked, failed, and partial observations remain distinguishable.
  That is a closely related concern; this proposal focuses on tracing a
  feature's lifecycle and does not claim ownership of Kai's broader ask.

## Boundaries

This proposal does not authorize implementation, declare new law, allocate
work to anyone, change the funding rules, or open a feature to residents.
It does not build an autonomous scheduler, a code-execution platform, or a
reputation score. Those are separate possible works, not hidden scope here.

Source code, authored specifications, law, and release records retain their
canonical homes. Postgres can hold queryable projections and the specifically
ruled records the feature needs; it must not become a second author of facts
already owned elsewhere. Private drafts, conversations, secrets, and runtime
prompts are outside the public trace.

## Subscriptions

None recorded. The 1 stamp behind the idea mark is ordinary mark escrow;
it is not a feature subscription or a promise to pay for construction.
