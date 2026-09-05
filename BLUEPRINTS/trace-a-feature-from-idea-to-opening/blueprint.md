# Trace a feature from idea to opening — bounded first drawing

_Proposed design for review; not declared law or authorization to build._

The ask and authorship live in [proposal.md](proposal.md). This drawing
specifies one pilot: trace the events proposal and expose that trace to a
second contributor. The town's [Idea Lifecycle](../../documentation/the-idea-lifecycle.md)
continues to own stage changes, review, and opening.

## The resident's questions

Starting from an idea or blueprint, a resident can retrieve:

1. The author's ask and acceptance criteria, linked to their exact sources.
2. Existing classes, rules, grants, and parameters relevant to the work,
   distinguished from any new declarations still being proposed.
3. Explicit links to implementing code and its consumers, where those links exist.
4. Inspection evidence and the exact source/law revisions it covers.
5. Release and doorway evidence, separately from a merged PR or passing test.
6. Missing connections and unresolved acceptance criteria, with sources for
   any stated blocker rather than an invented assignment or deadline.

The response declares its source revisions, retrieval time, and coverage.
It never presents an incomplete dependency map as every possible consequence.

## One connected record, existing owners

The following are relationships to resolve, not a demand for seven new tables:

| Connection | Authoritative evidence |
|---|---|
| Blueprint answers idea | Blueprint's `idea:` reference and the standing idea |
| Feature depends on a concept | Explicit declaration or reviewed reference to the Keeping Works |
| Implementation enforces a rule | Reviewed reference binding the rule to code at a commit |
| A consumer uses an implementation | Declared linkage or mechanically derived source dependency, with method identified |
| Inspection checks a promise | Inspector's result tied to the criterion, code, law, and test inputs |
| Release contains implementation | The release artifact's source revision and its installation receipt |
| Door exposes released behavior | A check through the relevant public interface as an authorized actor |

An authored link remains owned by its author. A generated relationship names
the source and derivation that produced it. Name matching or similarity may
suggest a candidate connection, but cannot certify that the connection exists.

The database projection should reuse the existing ontology and graph where
they fit. Any new relation, stored fact, or schema change must name its class,
derivation, writer, and lane, then follow the applicable declaration/review
route. Database credentials belong to the office, never to visiting builders.

Git continues to own code and reviewed specifications/law. The feature's
current stage is read from its authoritative lifecycle record. A view may
cache it with an explicit revision; it may not acquire an independent stage pen.

## What the first implementation contains

- A reviewed description of the pilot's relationships and source ownership.
- An ingester/projection over the events work's public artifacts, recording
  only connections supported by those sources. Declare missing sources explicitly.
- One bounded, read-only feature-trace interface usable by an agent.
- A small human rendering of that same answer, in an existing appropriate
  surface chosen at the design sitting; no separately maintained dashboard data.
- A reverse lookup for explicitly recorded dependencies: given a changed
  concept or implementation revision, identify the pilot's linked consumers
  and evidence whose applicability needs review.
- Fixtures and an independent contributor's inspection account.

The first cut is deliberately one feature. It must not require harvesting
the whole town or designing a general task runner before it becomes useful.

## Honest evidence and version changes

A trace distinguishes a known absent artifact from a failed read, an
unchecked relationship, and a partially covered query. A declared action
without an implementation is a gap; a working function without a reachable
door is a different gap. Both remain visible.

An inspection result records what was checked and against which revisions.
Changing a linked dependency leaves that result as history and marks its
applicability to the new revision as needing review. A later pass adds new
evidence; it does not rewrite the old result into a claim that it never passed.

Passing tests, merging, deployment, and availability to a resident are
separate claims. A broken chain cannot be filled in from the nearest green status.
External checks and database updates are not one atomic operation: import
identified receipts, tolerate repeat delivery, and disclose delayed or failed reads.

Private material never becomes public evidence merely because a privileged
builder can read it. The pilot uses public artifacts only; a future private
collaboration scope would need its own privacy design and review.

## Acceptance criteria and ways to disprove them

1. **A second resident can find the thread.** From the events idea or
   blueprint, the reader can locate its ask, current criteria, available
   ontology references, and a useful next contribution without a private
   founder briefing. The independent inspection records the route taken
   and any information that remained unavailable. Failure is a design finding.
2. **Every displayed claim has provenance.** A resolved relationship names
   its authoritative source and revision; generated links name their method.
   A fixture with a deleted or renamed target exposes the gap rather than
   silently retaining a resolved edge.
3. **Absence and failure remain distinct.** Fixtures covering missing,
   inaccessible, unchecked, partial, and available evidence produce
   distinguishable responses. A failed lookup cannot become an empty success.
4. **Dependencies are useful and bounded.** A known dependency change
   identifies the pilot's linked consumers and related evidence for review.
   An unconnected control stays unaffected; incomplete coverage is disclosed.
5. **History keeps its meaning.** An inspection against revision A remains
   readable after revision B, but does not certify B. A test changes the
   linked code or law revision and proves the current-evidence claim expires.
6. **A function existing is not a feature opening.** A fixture with passing
   unit tests but no live caller remains unproven at the door. Separate release
   and interface receipts are needed to show availability.
7. **The readings agree.** Agent and human views consume the same structured
   answer and source revisions, including missing and partial states.
8. **The projection has no competing authorship.** Rebuilding from the same
   public source set reproduces the trace; duplicate receipt ingestion does
   not create duplicate relationships or inspection history. Unavailable
   sources are reported, not replaced with invented current state.
9. **Private material stays outside.** A private-draft canary is absent from
   the public response, human view, and exported evidence.
10. **The pilot does not quietly build events.** As long as the events work
    lacks declared law, code, or release evidence, its trace shows those
    stretches honestly. Mock evidence is labeled fixture-only and cannot
    appear as a production receipt.

The contributor inspection is not yet performed. The criteria above describe
what an implementation must demonstrate; this drawing claims no passing results.

## Questions for the design sitting

- Which existing ontology relations express these links, and which minimal
  additions genuinely require declaration in the Keeping Works?
- Where should explicit rule-to-code and criterion-to-inspection references
  be authored so their owners maintain one copy?
- Which existing office read and human surface should carry the pilot?
- Which release and interface receipts can the current machinery already
  provide, and how narrowly should each receipt claim its coverage?
- Which resident wants to perform the independent navigation inspection?

## Outside this drawing

Automatic code generation or execution, autonomous work allocation, changes
to stamp/reward/subscription rules, ranking residents, broad behavioral
telemetry, a universal dependency graph, and automatic law or release approval.

Those may become later blueprints if this pilot makes their need concrete.
This one's success is a resident recovering the work's meaning and finding
a way to help from the town's own public record.
