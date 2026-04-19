---
name: workspace-operating-system
description: Central routing, sequencing, and quality-control layer for this unified skill bundle. Use when Codex is working anywhere in this repository and needs to decide which skills to load, how to combine them, what execution mode to use, or what quality bar to apply. Especially important for broad, ambiguous, multi-step, cross-domain, or high-value requests where the right workflow matters as much as the final answer.
---

# Workspace Operating System

## Purpose

Act as the default operating layer for this repository.

Before doing substantial work, classify the task, choose the minimum effective skill set, sequence execution, and enforce the quality bar.

## Mandatory Reading Order

Always read:

1. `references/task-routing.md`
2. `references/quality-bar.md`

Read only when needed:

- `references/composition-patterns.md` for cross-domain or multi-phase work
- `references/skill-catalog.md` when the right skill is unclear or you need exhaustive coverage

## Operating Rules

- Start narrow. Load the fewest skills that can reliably solve the task.
- Prefer one primary skill and only add supporting skills when there is clear value.
- Preserve existing product patterns before introducing a new visual, architectural, or workflow direction.
- Convert vague requests into a concrete execution path quickly; ask only when the missing detail changes the outcome materially.
- Move from discovery to action to validation. Do not stop at analysis for executable tasks.

## Execution Ladder

1. Classify the request.
   - Decide whether the task is primarily planning, building, debugging, reviewing, designing, testing, documenting, or shipping.
2. Choose the primary skill.
   - Use `references/task-routing.md` first.
3. Add support skills only if required.
   - Use `references/composition-patterns.md` when multiple skills must work together.
4. Execute.
   - Gather just enough context to avoid blind edits.
   - Implement or analyze with the chosen skill stack.
5. Verify.
   - Apply the universal finish criteria from `references/quality-bar.md`.
6. Close clearly.
   - State what changed, what was verified, and any residual risk.

## Routing Heuristics

- For broad product work, start with the task shape rather than the technology.
- For coding tasks, route by the real bottleneck:
  - architecture unclear -> `architecture`
  - implementation heavy -> domain skill such as `app-builder`, `api-patterns`, `frontend-design`, or `database-design`
  - failing behavior -> `systematic-debugging` plus the relevant domain skill
  - validation gap -> `testing-patterns`, `webapp-testing`, `lint-and-validate`, or `performance-profiling`
- For document and artifact work, prefer the dedicated document skills over ad hoc scripts.

## Composition Rules

- One-domain request: use one primary skill.
- Two-domain request: use one primary and one support skill.
- Three or more domains: read `references/composition-patterns.md` and actively sequence the work.
- If the task is unclear but high-impact, begin with planning or discovery before implementation.

## High-Value Defaults

- New feature: plan -> design/architecture -> build -> test -> polish
- Bug fix: reproduce -> debug -> patch -> verify -> summarize cause
- Review request: prioritize risks, regressions, and missing validation over style commentary
- UI request: clarify direction, preserve usability, and avoid generic output
- Infrastructure or deployment request: favor explicit validation and rollback awareness

## Relationship To Other Skills

- Use `intelligent-routing` for agent-selection patterns and auto-routing heuristics.
- Use `parallel-agents` for multi-agent decomposition when the environment supports it.
- Use `behavioral-modes` to adapt how you communicate and reason.
- Use `skill-creator` when modifying this bundle or adding new skills.

## Finish Condition

This skill is successful only when the agent can answer:

- Why this skill stack?
- Why this sequence?
- What was verified?
- What still remains uncertain?
