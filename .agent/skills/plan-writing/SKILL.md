---
name: plan-writing
description: Use when a task needs a clear execution plan before implementation starts. Apply this skill for multi-step features, meaningful refactors, risky bug fixes, or any work where sequence, scope, ownership, and verification should be made explicit first.
---

# Plan Writing

## Purpose

Write plans that are short enough to execute and precise enough to verify.

A good plan reduces ambiguity, reveals risk, and makes later execution boring in the best possible way.

## Use This Skill When

- the task spans multiple files or systems
- order matters
- the user asked for a plan
- a bug fix needs a reproducible path, patch, and proof
- parallel work might help but needs safe boundaries

## Principles

- Plan outcomes, not vague activity.
- Keep the number of steps small.
- Give every step a proof of completion.
- Name dependencies and collisions early.
- Do not pad the plan with obvious filler.

## Strong Plan Shape

1. Goal
   - one short paragraph on the user outcome
2. Constraints
   - technical, product, safety, or branch constraints
3. Steps
   - each step should say what changes and how to verify it
4. Done state
   - how the user will know the work is actually complete

## Step Quality Bar

Each step should answer:

- what changes
- where it changes
- what could block it
- how to prove it worked

If a step cannot be verified, it is probably too vague.

## Planning Heuristics

- Prefer 3 to 7 strong steps over 20 tiny ones.
- Break out parallel work only when ownership is disjoint.
- Put discovery before irreversible edits.
- Put verification near the step it proves, not only at the end.
- Keep one explicit final verification step for the whole task.

## Good Verification Language

- "Run the focused unit test for X"
- "Open the page and confirm Y state"
- "Verify the endpoint returns Z"
- "Confirm the branch is clean except for intended files"

## Weak Verification Language

- "make sure it works"
- "check everything"
- "verify manually"
- "test if needed"

## Handoff

If the plan will be executed later, note which supporting skill should own the next phase:

- `executing-plans`
- `using-git-worktrees`
- `parallel-agents`
- `closed-loop-delivery`

## Related Skills

- `executing-plans` to carry the plan through implementation
- `verification-before-completion` to enforce evidence at the end
