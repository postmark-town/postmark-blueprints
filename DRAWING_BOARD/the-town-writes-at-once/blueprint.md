# Blueprint — The Town Writes At Once

*Drawn 2026-08-05 from a read of the office source; redrawn the same evening when
the commission changed from a drawing kit to a pull-request lane. **Not yet trued
by a second hand** — the acceptance criteria below are the proposer's first
timber and a builder's red pen is welcome on all of it.*

## Governing evidence

All receipts are `file:line` in `keeminlee/postmark-office` (branch
`fix/865-home-assets-door`) and `keeminlee/postmark-world`.

| Claim | Receipt |
|---|---|
| The world lock IS the town lock | `office/src/world.mjs:436` — `process.env.TOWN_LOCK` |
| Marks/notes/walks/stakes/gifts all take it | `world.mjs:436-443`, `votes.mjs`→`stake-exec.mjs`, `ops.mjs:44-50` |
| The ferry holds it for its whole run | `office/deploy/postmark-ferry.service:46` (`flock -w 300`) |
| Taken synchronously, on the event loop | `world.mjs:442` / `ops.mjs:50` `execFileSync`; `server.mjs:525`,`:544` call without `await` |
| Single process, no cluster | `server.mjs:114` `createServer`, `:598` `listen` |
| One mark = 2 network round-trips + 3 spawns | `leave-exec.mjs` — fetch (`world-branches.mjs:189`), `mark-lint` (`:133`), `marks-fold` (`:143`), push (`:170`) |
| Gates live in the WORLD repo, not the office | `postmark-world/tools/mark-lint.mjs`, `tools/marks-fold.mjs` |
| Placement is computed from geometry, never authored | `leave-exec.mjs:89-100` → `marks-fold.mjs` `placementParent`; `tools/containment-diff.mjs` derives the whole tree from the same function |
| Identity already binds handle → GitHub id | `WORLD/households.json` (derived from town pins via the one resolver) |
| The sweep does NOT yet check branch ↔ authorship | `tools/settlement-sweep.mjs:277-306` — household from branch name only; safe today solely because the office pen is the only writer |
| The site posts through the office | `postmark-world/spectator/viewer.mjs:3622`, `:3767`, `:3346` |
| Letters and body edits take **no** lock | `write.mjs:76` `enqueueLetter`; `edit.mjs:100` `editBody` |

**Measured 2026-08-05:** 56 credential households / 77 handles; **8** `draft/*`
branches actually on origin; 474 marks; postmark-world = 8.9 MB `.git` + 6.6 MB
working tree (`WORLD/` is only 0.5 MB of it).

**Tense note (2026-08-05, evening):** the two synchronous-door rows above
describe the audited state. Tier 0 (async write path, one lane in
`src/town-lock.mjs`) and tier 1 (leased worktree pool, `src/world-pool.mjs`,
`WORLD_POOL=0` rollback) are built and tested on branches
`tier0/async-write-path` and `tier1/worktree-pool` — 173/173. First observed
write, dev fixture: **~670 ms** = checkout 330 + commit 150 + lint 54 + fold 60 +
spawn/lock ~65. **Box numbers are still owed** and remain a precondition of the
proposal posting; every write now logs `[town-lock] total=` / `[timing]` phase
lines, so the first deployed day answers.

## Architecture — the fold belongs where the writer is

The office's world-write path is not the law. It is a **remote hand that runs the
law**, and the law — `mark-lint` plus `marks-fold` — lives in postmark-world,
which is the repo a household's fork already carries.

That single fact is what makes the lane safe. A pull request into your own
`draft/<household>` does not fork enforcement, does not create a second answer to
*"is this mark legal,"* and cannot be weaker than the door: CI runs the same two
tools, from the same repo, at the same version the Settlement will judge by. The
lane relocates a hand, not a rule.

**The scaling argument in one line:** the fold is O(every mark in the world) and
runs on every write. On the office that cost is centralised and grows with the
town. In the lane it is paid twice, both times off the box: on the writer's own
hardware at pre-flight, and on CI compute at the gate. **This is the only change
in the whole picture that alters the asymptote.**

**Where the O(n) goes instead:** Settlement, which is O(households) and already
rebases every draft branch. That is the correct home for aggregate cost —
batched, on a cadence, off every resident's critical path. *Put the O(n) work on
the cadence and keep the interactive path flat.*

## The lane, end to end

1. Fork `keeminlee/postmark-world` (public). Your GitHub account is your
   credential; `households.json` already knows it.
2. Author under `WORLD/marks/**` (and `NOTES/<your-handle>.md`) with anything
   that edits files. For the one geometric question — *where does my outermost
   mark sit?* — run `tools/place-mark.mjs`; nested sets are self-placing because
   you designed the containment.
3. Pre-flight with `tools/mark-lint.mjs` — the identical gate CI runs.
4. Open a PR against `draft/<your-household>`. CI runs lint + fold `--no-write`
   + placement-vs-derivation + the **authorship wall** (every touched path and
   every `by:` resolves to the PR author's household).
5. Green automerges. Your household sees the mark immediately (authenticated
   reads fold your own draft); the town sees it when Settlement publishes it
   under escrow law, at a crossing, as ever.

**The crossing-rebase fact, stated plainly:** Settlement force-rewrites every
draft branch twice a day. A PR that stays open across a crossing will need a
`fetch && rebase`. Automerge makes that rare — a green PR lives minutes — and
additive diffs in your own namespace rarely conflict regardless. Sender fixes
own; the doctrine page names the two crossing times.

## Constraints a lane-user (or kit-builder) may rely on

Stated so nobody designs against a moving floor:

1. **`draft/<household>` is and stays the unit.** Household identity is
   `WORLD/households.json`; the office already lazy-creates the branch off main
   when absent.
2. **The Worldkeeper rebases every draft at Settlement** (onto the new main,
   force-with-lease). Expect your branch history to be *replaced*; reseat by
   fetch-then-rebase rather than assuming fast-forward. The office does exactly
   this and its logic is readable as a reference (`world-branches.mjs`).
3. **Derived canon is not yours to write.** `world-state.json` and `INDEX.md`
   belong to published main and the Settlement. A lane commit touches `mark.md`
   records (and your own `NOTES/` file) **only** — same rule the office follows,
   so a private draft never masquerades as canon. The authorship wall enforces
   the path set.
4. **The office door is not going away.** It is the site's write path and every
   chat-only resident's hand; relieving it is the point, replacing it is not.
   Stakes, gifts, and walks stay at the door — money is the sealed ledger's, and
   walks append a shared ledger on main.
5. **The founders carry the walls.** CI workflow, authorship wall (CI **and**
   sweep — the final publisher must hold even against a misconfigured merge),
   placer, doctrine page. None of it moves under a lane-user.

## Acceptance criteria

The lane passes inspection when:

- **A1 — same law.** A change CI accepts is accepted by `marks-fold` at
  Settlement, and a change CI refuses would have been refused by the office
  door. *Test:* a corpus of known-good and known-bad marks (including the
  sovereignty and parcel-cap cases) yields identical verdicts from lane and door.
- **A2 — no canon leakage, no borrowed pen.** A merged PR touches only the
  author's own `WORLD/marks/**` paths and `NOTES/` file; a PR touching another
  household's path or carrying a foreign `by:` is refused — by CI, and by the
  sweep even if merged. *Test:* adversarial PRs for each case.
- **A3 — survives a rewrite.** After a Settlement rebases the household branch,
  a straddling PR reseats by fetch-then-rebase and its next push is clean,
  without forcing anyone else's history. *Test:* rewrite the branch upstream,
  then land the PR.
- **A4 — no office.** The whole path completes with the office unreachable.
  *Test:* author, PR, merge, and settle with the office host blackholed.
- **A5 — the gate teaches.** Every CI refusal names the field, the reason, and —
  for placement — the correct path, in the bounce vocabulary the town already
  speaks (`{code, defect, hint}` register), never a bare stack trace.

## Sequence

1. ~~Founders: asynchronous write path; capture real timings.~~ **Built
   2026-08-05** (tier 0; box timings still owed — the posting precondition).
2. ~~Founders: narrow the lock.~~ **Built 2026-08-05** (tier 1, leased pool of
   worktrees, O(concurrent writers); deploy pending).
3. Founders: the lane's walls — CI workflow, authorship wall in CI and sweep,
   `place-mark.mjs`, `WRITES.md`.
4. **Commission:** the first outside drawing through the lane, to the criteria
   above. Inspection's witness is whoever did not build the walls.
5. Open ground thereafter: the optional kit (severable sugar), red pens on the
   walls.

## Preserve at inspection

- **The door still works.** A site-clicked walk must be no worse after this than
  before it.
- **One law, one owner.** If the lane ever needs a rule the World's tools do not
  already enforce, that rule belongs *in the World's tools*, not in the
  workflow. A second enforcement surface is the failure this design exists to
  avoid.

## Loose ends worth a red pen

- **Letters and body edits take no lock at all** while marks take a global one —
  two serialization disciplines in one codebase (`write.mjs:76`, `edit.mjs:100`).
  Under concurrency the unlocked pair does not corrupt (git's own `index.lock`
  refuses) but *fails* where the other would have waited. Out of scope here;
  should be reconciled deliberately in some direction.
- **Concurrent `git fetch` against one object store is unmitigated** (tier 1,
  known, self-healing by design: fetch failure degrades to local refs and push
  goes push-pending). Untestable in fixtures — no origin. If push-pending noise
  appears on the box, the fix is a fetch lock or a coalesced parent-side fetch.
- ~~**The 503 text is stale.**~~ Fixed in tier 0 — one copy, in
  `src/town-lock.mjs`, saying what a lock wait means today.
- ~~**Per-household worktrees may be the wrong unit.**~~ Resolved as predicted:
  tier 1 shipped a leased pool (default 4), O(concurrent writers); with 8 live
  branches against 56 households, per-household allocation would have idled.
