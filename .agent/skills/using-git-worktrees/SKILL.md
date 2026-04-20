---
name: using-git-worktrees
description: Use when work should happen in an isolated git workspace instead of the current checkout. Apply this skill for risky feature work, parallel branches, review fixes, or any task that benefits from a clean worktree with a known baseline.
---

# Using Git Worktrees

## Purpose

Use git worktrees to isolate risky or parallel work without disturbing the current checkout.

This is especially valuable when the main workspace is busy, dirty, or already serving another task.

## Use This Skill When

- starting a feature or refactor that should not touch the current checkout
- fixing review feedback on a dedicated branch
- comparing two implementation paths side by side
- delegating or testing work that benefits from a clean branch baseline

## Do Not Use This Skill When

- the task is a tiny one-file change that belongs in the current branch
- the repository is not git-backed
- the user explicitly wants the current workspace modified in place

## Setup Rules

1. Find the repository root and current branch.
2. Check whether the repo already uses a preferred worktree directory such as `.worktrees/` or `worktrees/`.
3. If a project-local directory is used, confirm it is ignored by git before creating the worktree.
4. Choose a descriptive branch name tied to the task.

## Safety Rules

- Never create a project-local worktree in a tracked directory.
- Never assume `main` or `master` is safe to edit directly without user approval.
- If the current repo already has unrelated local changes, avoid mixing them into the new task.
- If ignore rules are missing, add the ignore entry before treating the setup as clean.

## Execution Flow

1. Create the worktree on a new branch.
2. Enter the new path and run the minimum setup needed for the project.
3. Verify the baseline before editing.
   - at least confirm status, dependencies, and the most relevant test or start command
4. Do the task inside the worktree.
5. When the work is done, use `finishing-a-development-branch` to decide whether to merge, push, keep, or discard it.

## Baseline Checks

Aim for a quick proof that the new workspace is usable:

- `git status --short`
- dependency install or restore if needed
- focused test, build, or app boot check

If the baseline is already broken, say so clearly before building on top of it.

## Reporting Pattern

When the worktree is ready, report:

- the branch name
- the worktree path
- whether the baseline check passed
- any pre-existing failures or constraints

## Related Skills

- `executing-plans` when the task already has an approved plan
- `closed-loop-delivery` when the task needs end-to-end acceptance proof
- `finishing-a-development-branch` when the branch work is complete
