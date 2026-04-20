---
name: receiving-code-review
description: Use when review comments, requested changes, or code-review feedback need to be interpreted and acted on. Apply this skill when an agent should evaluate feedback technically, clarify ambiguous items, and fix valid issues without blind agreement.
---

# Receiving Code Review

## Purpose

Treat review feedback as technical input, not as something to accept blindly or resist emotionally.

The goal is to improve the work while preserving correctness, scope, and context.

## Use This Skill When

- a user shares review comments or requested changes
- a pull request has inline feedback that needs action
- multiple review items must be clarified, prioritized, and implemented

## Response Sequence

1. Read all feedback first.
2. Group comments by theme, severity, and ambiguity.
3. Clarify anything materially unclear before editing.
4. Check each suggestion against the actual codebase and requirements.
5. Implement valid changes in coherent batches.
6. Verify the updated behavior before replying or closing the loop.

## Review Heuristics

- Favor correctness over performative agreement.
- Push back politely when feedback conflicts with codebase reality or explicit requirements.
- Escalate when two instructions cannot both be satisfied.
- Watch for scope creep disguised as "proper" or "complete" implementation.

## Good Handling

- restate the technical issue in plain language
- ask one focused question when a comment is ambiguous
- fix the issue and mention the concrete change
- explain a disagreement with evidence, not tone

## Bad Handling

- agreeing before checking
- implementing half-understood comments
- batching unrelated fixes into one vague reply
- treating style feedback as more important than correctness or regression risk

## Implementation Order

Default order:

1. correctness and security
2. regressions and test gaps
3. maintainability and clarity
4. stylistic polish

## Related Skills

- `code-review-checklist` for reviewing code yourself
- `verification-before-completion` before claiming review items are resolved
- `closed-loop-delivery` when the task includes implementation, review feedback, and runtime proof
