# Goal Loop: Deep Research

An iterative research workflow that runs until the done-condition is met, novelty dries up, or guardrails trip. Invoke with plain words ("goal-loop this", "deep dive until done") — no slash command needed. Use for a substantial research question with a defined finish line. This is an active, bounded research session, not a promise of continuous background work. It adds no tools or permissions.

## The loop

Each round runs five phases:

1. **Plan** — 2-4 non-overlapping research angles targeting the biggest open gaps. On round 2+, the previous round's red-team attacks and open gaps are the PRIMARY input. Each angle names which prior attack or gap it addresses.
2. **Research** — Research the angles in parallel only if delegation is available and authorized (up to 3 concurrent); otherwise work through them sequentially. Many distinct sources, multiple source types. Every substantive claim tagged `[observed]` (seen directly in a cited source) or `[inference]` (interpretation). Actively hunt counter-evidence. Never invent sources or quotes; keep quotes short with the source named. Self-reported marketing numbers tagged as such, never presented as independent measurements.
3. **Synthesize** — Append a dated `## Round N` section to the living dossier (never rewrite earlier sections). Maintain a confidence ledger: each load-bearing claim rated low | medium | medium-high | high with a one-line why.
4. **Red team** — A sharp colleague who wants the plan to succeed, not an adversary. Find common-sense holes, important missed points, outcome-relevant nuances. Never edge-case hunt or tear down for sport. Every attack carries a concrete fix. Steelman up to 3 attacks on load-bearing claims, rated fatal-to-thesis | weakens | fails-against-evidence.
5. **Review** — Judge cheaply and sharply: done? (quality, not just completeness), novelty? (genuinely new evidence?), North Star check (does this still serve the original goal — flag scope drift), recommendation: continue | checkin | complete | blocked.

## Guardrails

- **15 rounds max**; stop early when the goal is met
- **Novelty gate**: 2 consecutive rounds with no new evidence → stop
- **Checkpoints** — give a short progress update every 5 rounds, or sooner if effort feels disproportionate; do not wait for an answer unless a decision is needed
- **Spend profile**: research + synthesis ~80%+; red team / North Star are cheap pressure-testers; inversion = bug, stop
- **Pause triggers**: missing permission for spending or outreach, an access restriction, or a decision that changes the goal. Stop on a user request or the agreed effort limit; do not bypass permission denials.
- **Resilience**: for a failed read-only research call, retry once if useful, then use another source or record the gap. Never retry a permission denial or repeat an action with an uncertain external effect. If delegation is unavailable, continue sequentially; do not invent agent results.
- **Incomplete run → rollup**: preserve the dossier and report; nothing is lost
- Token metering is approximate — round cadence + effort notes is the checkpoint

## Reporting (TLDR-first, no exceptions)

Every run ends with a 5-point TLDR — pithy, no word cap — in chat AND at the top of the dossier:

1. What this run tried to accomplish
2. What it accomplished
3. The so-what — the single most important takeaway
4. Blockers
5. Next steps

Details underneath. Stop as soon as the question is answered and the evidence survives the pressure test; do not manufacture extra rounds. If runtime limits interrupt the work, save a checkpoint and state what remains.

## Bar

A product a VP would hand to their CEO, not a first draft. Each round's planner ingests prior red-team attacks. The loop pressure-tests, then re-researches.

## Starting a run

Inputs needed: `goal` (what we're trying to learn or decide), `dossierPath` (where the living dossier lives), `doneCondition` (the question is answered with cited evidence, important counter-evidence addressed, and remaining uncertainty stated; a confidence rating alone is not proof), optional `seedAngles` and `maxRounds`, plus an agreed time or effort budget. The earlier stopping limit takes precedence over the default 15-round ceiling.
