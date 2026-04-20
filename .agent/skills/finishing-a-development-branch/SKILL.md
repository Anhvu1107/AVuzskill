---
name: finishing-a-development-branch
description: Use when a branch or worktree is functionally complete and the next step is to decide how to wrap it up. Apply this skill before pushing, opening a PR, merging, keeping, or discarding completed branch work.
---

# Finishing A Development Branch

## Purpose

Separate "the work seems done" from "the branch is ready for the next decision."

This skill helps an agent close the loop cleanly instead of leaving a half-finished branch state behind.

## Use This Skill When

- implementation in a branch or worktree appears complete
- tests have been run and the next question is merge, push, keep, or discard
- the user asks what should happen with a finished branch

## Closeout Sequence

1. Verify the current state.
   - status, diff, and the most relevant validation
2. Summarize what is on the branch.
3. Identify the likely base branch.
4. Present clear next-step options.
5. Execute only the option the user chose.
6. Clean up the worktree or branch only when that choice requires it.

## Option Set

Offer concise, explicit choices such as:

- push and open or prepare a PR
- merge into `dev`, `test`, or the agreed integration branch
- merge locally only if that matches the repo workflow
- keep the branch as-is for later
- discard the branch after confirmation

## Safety Rules

- Never delete a branch or worktree without explicit confirmation.
- Never force-push or rewrite history unless the user asked for it.
- Never imply readiness if verification is incomplete.
- Never recommend direct merge or push to `main` or `master` unless the repo policy clearly allows it and the user approves.
- If the branch contains unrelated changes, call that out before recommending cleanup or merge.

## Recommended Report

Before asking for the final choice, include:

- branch name
- base branch guess
- short summary of changes
- verification status
- any cleanup risk or open issue

## Related Skills

- `using-git-worktrees` when the branch lives in a separate worktree
- `verification-before-completion` before stating the branch is ready
- `receiving-code-review` if the branch still has unresolved review feedback
