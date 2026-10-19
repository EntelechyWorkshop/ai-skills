# Goal Loop

Use when asked to work toward a concrete result in repeated, checked steps ("use Goal Loop" or "take this as a goal and run with it"). This is an active work session with an agreed stopping limit, distinct from Muse's longer-running background goals. It does not create new tools, permissions, or background execution capabilities.

## Setting the goal

A goal needs three things before work starts:

1. **Objective** — one paragraph, concrete. Name the outcome, not the activity. ("Refactor the auth module to JWT" beats "work on auth.")
2. **Finish line** — how you will know it's done, stated as verifiable criteria. Tests passing, a file existing with defined contents, a number hitting a threshold. If you can't say how you'd check it, the goal isn't ready.
3. **Constraints** — boundaries the agent must respect: files or systems it may not touch, approaches that are off the table, a max cycle or effort budget.

Long specifications live in a project file; the goal itself points at the file and keeps the finish line inline.

## The loop

Each cycle runs four steps:

1. **Plan** — the smallest next chunk of work that moves toward the finish line. One chunk per cycle; don't plan the whole project up front.
2. **Act** — do the chunk. Make the change, run the command, write the file.
3. **Verify** — check the chunk against the finish line. Run the tests, read the output, confirm the behavior. Evidence, not vibes.
4. **Review** — end-of-cycle check: did we hit the finish line? If yes, stop and report. If no, is the next chunk clear? If yes, continue. If the agent is stuck, confused, or needs a judgment call, pause for the user instead of guessing.

## Pause, resume, clear

- **Pause** when blocked on missing information, a decision only the user can make, or a constraint violation. State exactly what is needed to resume.
- **Resume** picks up where the loop left off — re-read the goal and the last verified state, don't start over.
- **Stop or clear** ends work immediately. Save a brief checkpoint when possible; do not keep working toward the goal after a stop request.

## Guardrails

- **Finish line is load-bearing.** Never declare done without running the verification. "Looks right" is not done.
- **One chunk per cycle.** Big-bang plans rot; small verified steps compound.
- **Effort budget.** Set a max number of cycles (or time/token budget) up front. When it's near, wind down gracefully: report what was accomplished, what's left, and what it would take to finish.
- **No silent scope growth.** If the work reveals the goal was wrong, pause and re-contract the goal with the user — don't quietly redefine "done."
- **Authorization.** Stay within the user’s authorized scope. Before deleting data, publishing, spending money, or contacting someone, obtain any approval not already explicitly given. Never bypass an access restriction or permission denial.

- **Runtime limits.** If the session or tools cannot continue, save the verified state and next step. Do not claim that work will continue in the background unless that capability is actually available and authorized.

## Reporting

Brief status at each natural checkpoint: what was just verified, what's next. When the loop ends — done, paused, or cleared — close with the same five lines every time:

1. What I was trying to accomplish
2. What it actually accomplished
3. Blockers, if any
4. What remains, if anything
5. Proposed next steps
