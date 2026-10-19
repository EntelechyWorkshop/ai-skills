---
name: projectmanagerview
description: Project-management audit workflow for reviewing a project plan, proposed next step, branch, sprint, or agent recommendation from a sponsor/north-star lens. Use when the user says /projectmanagerview, projectmanagerview, PM view, project manager view, zoom out, sanity-check the plan, audit the next step, are we churning, are we solving the right problem, compare QC/worker feedback, or asks whether to proceed, defend, revise, pause, parallelize, or rebaseline a project plan.
---

# Project Manager Review

## Purpose

Take the project manager and integrator role. Treat the user as the decision-maker unless they identify another sponsor. Review whether the work advances the real project objective, manages risk, reduces uncertainty, and avoids repeated activity without progress.

Use this workflow with any project or AI assistant. Require no particular account, repository layout, software platform, external integration, or multi-agent capability. Adapt the depth of review to the importance of the decision.

This skill is not a “make the plan stricter” skill. Use judgment. Good PM work sets goals, guardrails, risks, decision points, and team coordination without turning every choice into a brittle hard gate.

## Strategic Compass

For a sustained goal or subgoal, locate or create the shortest authoritative
statement using this five-part frame:

```text
STRATEGIC OUTCOME
What capability must exist when this goal is complete?

THEORY OF CHANGE
Why should the current work create that capability?

CURRENT CONTRIBUTION
What is this task or phase supposed to teach or enable?

DRIFT RISKS
What tempting proxies could be mistaken for success?

NEXT CAPABILITY
What must the next person, team, or stage genuinely be able to do?
```

Answer these in outcome language, not as a long checklist of deliverables or
binary verdict fields. Add tactical detail beneath this frame only where it
improves execution, risk control, or evidence quality.

Treat this Strategic Compass as the stable intent layer. Execution plans,
settings, checklists, and sponsor questions are mutable inputs beneath it. A
Sponsor question is not automatically a scope change or a new acceptance
criterion; interpret it against the compass and ask whether it changes the
outcome, evidence, risk, or implementation.

When a project provides a current objective or strategy statement, read it before older completion reports or detailed work plans. Use the sources the user identifies as authoritative. Do not assume a document is authoritative merely because it has the newest timestamp or highest version number. Draft a concise working compass from the available context when none exists; do not create or overwrite project documents unless that is within the requested scope.

## Default Workflow

1. **Orient to the actual project state**
   - Identify the sponsor objective, current phase, desired outcome, proposed next step, recent evidence, and known blockers.
   - Read the available project brief, current status, phase plan, decision rules, decision history, and source index when relevant. Do not require specific filenames or a complete documentation set.
   - If documents or tools are unavailable, use the context supplied by the user and state material gaps. Ask for missing information only when it would change the decision.

   Reconstruct the Strategic Compass before evaluating activities. If the
   sources disagree, surface the conflict rather than silently choosing the
   easiest action or most recent narrative.

2. **Separate the goal from the activity**
   - State the intended outcome in plain language.
   - State the operational task being proposed.
   - Check whether completing the task would actually move the goal, or merely produce another document, output, or completed activity.
   - Name a plausible false-success case: the work passes mechanically while
     the required capability remains absent. If the current completion rule
     would accept that case, recommend a corrected rule before major execution and apply it only within the authority already granted.

3. **Audit proxy substitution**
   - Identify indirect measures being used as evidence of the intended outcome.
   - Ask whether document counts, completed checklists, activity levels, or passing tests could look successful while the required capability remains absent.
   - Treat such measures as diagnostic evidence unless the project objective explicitly makes them the outcome. Explain what evidence would connect the measure to actual success.

4. **Audit strategic fit**
   - Does the next step align with the sponsor objective?
   - Does it preserve or improve optionality?
   - Is it solving the highest-leverage blocker, or a convenient narrower one?
   - Is it “best/high-leverage enough,” not merely the smallest patch?

5. **Audit root-cause narrowing**
   - Identify which hypotheses the step tests, rules in, rules out, or leaves untouched.
   - Watch for false precision: more metrics, probes, or reports that do not reduce uncertainty.
   - Prefer broad-enough brackets early, then narrowing once evidence justifies it.
   - Do not force “one root cause” if the evidence points to interacting causes.

6. **Audit risk**
   - Name the top relevant risks, likelihood, impact, early warning signal, mitigation, and next action. Label estimates and unknowns; do not invent probabilities or assign owners without evidence.
   - Include risks from over-control, under-control, outdated authoritative documents, hidden downstream effects, resource limits, data quality, evaluation mismatch, and team/agent drift.
   - Explicitly note if a proposed plan would confuse operational success with project success.

7. **Audit scope and sequencing**
   - Decide what should be done now, later, in parallel, or not at all.
   - Identify critical-path dependencies.
   - Identify workstreams that can safely run in parallel without contaminating evidence.
   - Consider parallel work when it reduces risk or speeds learning; account for coordination costs and shared dependencies.

8. **Assess feedback**
   - Treat reviewer, contributor, and other-agent feedback as input to assess on its merits.
   - Classify each recommendation as:
     - `incorporate`
     - `modify`
     - `defer`
     - `reject`
   - Explain why, especially when rejecting control-heavy or over-constraining advice.

9. **Decide**
   - Give a PM verdict:
     - `proceed_as_planned`
     - `proceed_with_changes`
     - `pause_to_investigate`
     - `split_parallel_workstreams`
     - `rebaseline_plan`
     - `stop_or_reframe`
   - Include the next 1-3 concrete actions.
   - If execution is requested, enough context exists, and the action is authorized, proceed after the audit. Keep an assessment-only request read-only. Never use the project objective to override permissions or required approvals.

## Event-Driven Checks During Execution

Do not wait until closeout to discover strategic drift, and do not interrupt
work on a fixed timer merely to repeat status. Re-run the PM view when:

- a proposed solution or measure of success is about to be accepted;
- a pilot or rehearsal is complete and a larger commitment of time or resources is next;
- evidence changes the theory of change, scope, or risk materially;
- the work begins optimizing an observable proxy rather than the intended
  outcome;
- the goal is about to be declared complete or the next stage declared ready.

At each event, ask: what capability has actually been created, what is still
being inferred, and would the proposed next action remain the best choice if
no checklist field existed? Course-correct the work when needed; do not merely
write a warning beside work that is drifting off course.

## Output Shape

Keep the response readable and sponsor-facing. Prefer a concise narrative that
makes the judgment and reasoning clear. The following is an optional aid, not
a completion form:

```text
PM Verdict: ...

What We Are Solving For:
...

Project-State Read:
...

Next-Step Audit:
- What it would achieve:
- What it would not solve:
- Risk:
- Confidence:

Incorporate / Defend:
- Incorporate:
- Modify:
- Defer:
- Reject:

Risk Register:
- Risk:
  Signal:
  Mitigation:
  Decision impact:

Recommended Next Move:
1. ...
2. ...
3. ...
```

Do not overuse the template for small questions. A concise narrative is fine if it answers the PM question.

## PM Principles

- Use the agreed objective to evaluate outdated plans and assumptions. Flag conflicts with governing documents and recommend a controlled amendment; do not silently disregard binding constraints.
- A plan is good when it manages uncertainty and risk, not when it has the most gates.
- Avoid “smallest patch” bias when the user is asking for best/high-leverage architecture.
- Avoid “boil the ocean” bias when a focused effort can answer the decisive uncertainty.
- Distinguish what a solution claims to be, how it works, whether it is ready for use, and whether it produces the intended benefit.
- Separate evidence from interpretation, and interpretation from decision.
- Preserve uncertainty when uncertainty is useful; do not collapse it into fake certainty.
- If an evaluation method or reporting format cannot represent the proposed approach, examine that mismatch before concluding that the approach itself has failed.
- A machine-readable verdict may summarize judgment, but must not manufacture
  it. Do not convert an ambiguous strategic question into a large binary field
  list merely because fields are easier to validate.

## Optional Team Huddle

If additional agents are available, their use is authorized, and the decision warrants the overhead, use distinct review perspectives. Otherwise, review these perspectives yourself without implying that independent reviewers participated:

- Strategy PM: sponsor objective, phase fit, critical path.
- Risk Manager: risks, mitigations, early warning signals.
- Feasibility Lead: practical constraints, interfaces, and dependencies.
- Evidence Reviewer: whether the assessment measures the intended outcome.
- Delivery Lead: sequencing, coordination, handoffs, and implementation implications.

Synthesize disagreements. Do not average them into bland consensus.

## Usage-Pause Continuity

Treat interrupted or unavailable reviews as incomplete evidence, never as successful completion. Apply this section only when a review is actually in progress.

- Preserve the reviewer's exact assignment, evidence already gathered, unresolved questions, and agent identifier.
- When work can resume, continue the assignment with the same reviewer where possible. Otherwise, use an authorized replacement with the preserved brief and identify the handoff. Do not claim automatic resumption or background work unless the host actually supports and has scheduled it.
- A missing, null, interrupted, or usage-limited response is not evidence that no blockers exist.
- Continue independent critical-path work during the pause when safe, but do not close the decision that depended on the paused review.
- Apply this rule wherever a decision depends on the missing review. Explain the practical impact and the smallest action needed to resume.

## Reusable Skill Boundaries

Keep these reusable instructions independent of any person or project. Do not add personal names, contact details, credentials, account identifiers, private URLs, local paths, or project-specific examples to the skill or its metadata. Use project context only in the current assessment, and include only information relevant to its intended audience. Do not copy that context into reusable files or send it to external services without authorization.
