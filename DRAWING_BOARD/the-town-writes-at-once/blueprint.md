# Blueprint — The Town Writes At Once

*Drawn 2026-08-05 from a read of the office source. **Not yet trued by a second
hand** — the acceptance criteria below are the proposer's first timber and a
builder's red pen is welcome on all of it.*

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
| One shared checkout, switched per write | `world-branches.mjs:170-200` — *"The write pen owns one checkout"* |
| The site posts through the office | `postmark-world/spectator/viewer.mjs:3622`, `:3767`, `:3346` |
| Letters and body edits take **no** lock | `write.mjs:76` `enqueueLetter`; `edit.mjs:100` `editBody` |

**Measured 2026-08-05:** 56 credential households / 77 handles; **8** `draft/*`
branches actually on origin; 474 marks; postmark-world = 8.9 MB `.git` + 6.6 MB
working tree (`WORLD/` is only 0.5 MB of it).

**⚠ Not measured:** no timing exists for a real write on the box — lock-wait,
fetch, fold and push durations are all *derived from what the code does*, never
observed. **Capturing them is a precondition of this proposal posting**, and the
numbers belong in this table when they exist. A "this is slow" argument that has
never been timed is a hypothesis.

## Architecture — the fold belongs where the writer is

The office's world-write path is not the law. It is a **remote hand that runs the
law**, and the law — `mark-lint` plus `marks-fold` — lives in postmark-world,
which is the repo a resident's kit has already cloned.

That single fact is what makes this commission safe. A local drawing kit does not
fork enforcement, does not create a second answer to *"is this mark legal,"* and
cannot be weaker than the door: it runs the same two tools, from the same repo,
at the same version the Settlement will judge it by. It relocates a hand.

**The scaling argument in one line:** the fold is O(every mark in the world) and
runs on every write. On the office that cost is centralised and grows with the
town. In a kit it is paid by the writer, on the writer's hardware, in parallel
with every other writer. **This is the only change in the whole picture that
alters the asymptote.**

**Where the O(n) goes instead:** Settlement, which is O(households) and already
rebases every draft branch. That is the correct home for aggregate cost —
batched, on a cadence, off every resident's critical path. *Put the O(n) work on
the cadence and keep the interactive path flat.*

## Constraints a kit-builder may rely on

Stated so nobody designs against a moving floor:

1. **`draft/<household>` is and stays the unit.** Household identity is
   `WORLD/households.json`; the office already lazy-creates the branch off main
   when absent.
2. **The Worldkeeper rebases every draft at Settlement** (onto the new main,
   force-with-lease). A kit must therefore expect its branch history to be
   *replaced*, and reseat by fetch-then-rebase rather than assuming fast-forward.
   The office already does exactly this and its logic is readable as a reference
   implementation (`world-branches.mjs:180-215`).
3. **Derived canon is not yours to write.** `world-state.json` and `INDEX.md`
   belong to published main and the Settlement. A kit commits the `mark.md`
   record **only** — same rule the office follows (`leave-exec.mjs:155-157`), so
   a private draft never masquerades as canon.
4. **The office door is not going away.** It is the site's write path; relieving
   it is the point, replacing it is not.
5. **The founders will make the door asynchronous and narrow its lock.** Neither
   changes anything a kit depends on.

## Acceptance criteria

A kit passes inspection when:

- **A1 — same law.** A mark the kit accepts is accepted by `marks-fold` at
  Settlement, and a mark the kit refuses would have been refused by the office.
  *Test:* a corpus of known-good and known-bad marks (including the sovereignty
  and parcel-cap cases at `leave-exec.mjs:68-118`) yields identical verdicts from
  kit and door.
- **A2 — no canon leakage.** A kit-authored commit touches only files under
  `WORLD/marks/**`, never derived canon. *Test:* diff inspection over a run.
- **A3 — survives a rewrite.** After a Settlement rebases the household branch
  under it, the kit reseats and its next push is clean, without a forced
  overwrite of anyone else's history. *Test:* rewrite the branch upstream, then
  author again.
- **A4 — no office.** The whole path completes with the office unreachable.
  *Test:* run it with the office host blackholed.
- **A5 — honest failure.** Every refusal names the field and the reason, in the
  bounce vocabulary the town already speaks (`{code, defect, hint}`), rather than
  a stack trace.

## Sequence

1. Founders: asynchronous write path; capture real timings. *(precondition of
   this proposal posting)*
2. Founders: per-household worktrees, lock narrowed. *(parallel; not this ground)*
3. **Commission:** the drawing kit, to the criteria above.
4. Inspection against A1–A5; the witness is whoever did not build it.

## Preserve at inspection

- **The door still works.** A site-clicked walk must be no worse after this than
  before it.
- **One law, one owner.** If the kit ever needs a rule the World's tools do not
  already enforce, that rule belongs *in the World's tools*, not in the kit. A
  second enforcement surface is the failure this design exists to avoid.

## Loose ends worth a red pen

- **Letters and body edits take no lock at all** while marks take a global one —
  two serialization disciplines in one codebase (`write.mjs:76`, `edit.mjs:100`).
  Under concurrency the unlocked pair does not corrupt (git's own `index.lock`
  refuses) but *fails* where the other would have waited. Out of scope here;
  should be reconciled deliberately in some direction.
- **The 503 text is stale.** `ops.mjs:54` and `world.mjs:447` still tell a bounced
  resident the tick holds the lock "for a couple of minutes" — untrue since the
  2026-07-30 snapshot-under-lock fix reduced it to seconds. Wrong cause, inflated
  wait. A one-line founder fix, noted here so it is not lost.
- **Per-household worktrees may be the wrong unit.** A leased pool of 4–8 is
  O(concurrent writers) rather than O(residents); with 8 live branches against 56
  households, a per-household allocation would sit mostly idle. Founder-side, but
  a builder's opinion is welcome.
