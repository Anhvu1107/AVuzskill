---
name: executing-plans
description: Use when there is already a written plan or clear task list and the next job is to execute it carefully. Apply this skill when implementation should follow an approved sequence, checkpoint, or plan document instead of improvising from scratch.
---

# Executing Plans

## Purpose

Turn an approved plan into finished work without drifting away from the agreed scope.

This skill is for execution, not for rediscovering the strategy from zero.

## Use This Skill When

- the user already approved a plan
- a repo contains a plan file that should now be implemented
- work must follow a staged sequence with explicit checkpoints
- the main risk is skipping, reordering, or overbuilding plan steps

## Execution Rules

1. Read the entire plan before changing anything.
2. Challenge unclear or dangerous steps up front.
3. Convert the plan into a live checklist if needed.
4. Execute one coherent step at a time.
5. Verify each step before calling it complete.
6. Escalate blockers instead of inventing silent plan changes.

## Before Starting

- confirm the plan still matches the current codebase
- identify which files, commands, and dependencies the plan implies
- decide whether the work should happen in a separate worktree

If the plan is stale, say exactly where reality diverges and propose the smallest correction.

## During Execution

- keep scope tight to the plan goal
- follow dependencies in order
- note safe parallelizable work, but only if the write surfaces do not collide
- prefer the minimum change that satisfies the current step

## Verification Standard

Every completed step should have a proving action:

- test command
- lint or build command
- browser or runtime check
- output inspection
- diff review against the requirement

Use `verification-before-completion` before summarizing the result.

## When To Pause

Pause and realign if:

- the plan requires information that does not exist
- the codebase no longer matches the assumptions in the plan
- a verification step fails repeatedly
- a new constraint changes the order or meaning of later steps

## Related Skills

- `plan-writing` to produce the plan first
- `using-git-worktrees` to isolate the execution branch
- `parallel-agents` for disjoint sub-tasks that can safely run in parallel
- `finishing-a-development-branch` when the plan is complete
