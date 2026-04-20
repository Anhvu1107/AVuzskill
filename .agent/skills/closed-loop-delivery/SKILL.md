---
name: closed-loop-delivery
description: Use when a coding task should be driven to a real done state with explicit acceptance criteria, implementation, verification, review response, and runtime confirmation where needed. Apply this skill for end-to-end delivery, not just code edits.
---

# Closed-Loop Delivery

## Purpose

Deliver against a definition of done, not against the size of the diff.

This skill keeps implementation, review, and verification connected until the actual user outcome is proven.

## Use This Skill When

- the user expects an end-to-end fix or feature, not partial progress
- runtime behavior matters, not just source edits
- review comments, test failures, or environment checks are part of completion
- repeated prompts like "now test it", "now verify it", and "now respond to review" should be avoided

## Define Done First

Before coding, write down:

- the task goal
- explicit acceptance criteria
- the environment to verify against
- the proof expected at the end

If acceptance criteria are missing, propose a concrete version and proceed unless the decision would materially change the result.

## Delivery Loop

1. Define the acceptance criteria.
2. Isolate the work if needed.
   - for meaningful code changes, prefer a branch or worktree
3. Implement the minimum change that can satisfy the criteria.
4. Run focused verification locally.
5. Resolve relevant review feedback or verification failures.
6. Run runtime or browser checks when behavior depends on the real app or service.
7. Repeat until the acceptance criteria are either proven or blocked.

## Human Gates

Pause for user confirmation before:

- production or high-risk deployment
- destructive data operations
- force-push, history rewrite, or irreversible cleanup
- direct push or merge to a protected branch
- actions requiring secrets, billing, or permission assumptions

## Evidence Standard

Completion should include:

- acceptance criteria checklist with pass or fail status
- commands or checks run
- runtime evidence when applicable
- branch or promotion status when code changed
- unresolved risk or blockers

If a criterion is not proven, mark it clearly instead of burying it in the prose.

## Stop Conditions

Stop and report a blocker if:

- acceptance criteria still fail after reasonable iteration
- the environment or credentials prevent verification
- review instructions conflict in a way that changes product direction

## Related Skills

- `executing-plans` when the work already follows an approved plan
- `receiving-code-review` when PR feedback is part of the loop
- `verification-before-completion` for the final evidence gate
- `webapp-testing` when browser automation is the cleanest proof
