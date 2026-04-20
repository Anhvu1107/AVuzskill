---
name: parallel-agents
description: Use when a task contains multiple independent questions, investigations, or implementation slices that can run in parallel without blocking the next local step. Apply this skill to split work cleanly across subagents with explicit ownership, no duplicated effort, and controlled integration.
---

# Parallel Agents

## Purpose

Parallelism is a force multiplier only when the subtasks are truly independent.

This skill helps an agent decide what to do locally now, what to delegate, and how to integrate results without chaos.

## Use This Skill When

- there are distinct research questions that can be answered separately
- different codebase slices can be changed without touching the same files
- verification can run in parallel with active implementation
- the next local step is clear even while subagents work in the background

## Do Not Use This Skill When

- the very next step is blocked on the delegated answer
- two subtasks need the same file ownership
- the work is tightly coupled and likely to thrash between agents
- the task is small enough that delegation would add overhead

## Core Rule

Do the immediate blocking work locally.

Delegate only bounded sidecar tasks that materially advance the main goal without stalling the critical path.

## Decision Process

1. Identify the immediate local step.
   - What should happen right now if no delegation existed?
2. Identify sidecar tasks.
   - discovery, isolated implementation, verification, or review work
3. Check independence.
   - separate files, separate questions, separate failure domains
4. Assign ownership.
   - each subagent gets a clear output and a disjoint scope
5. Keep working locally.
   - do not wait by reflex
6. Integrate and verify.

## Good Delegation Targets

- "map where auth state is read in the frontend"
- "implement tests in this one file"
- "review these changed files for regression risk"
- "compare two isolated approaches and return tradeoffs"

## Bad Delegation Targets

- "figure out the whole task and tell me what to do"
- "implement the part I need before I can continue"
- "work on the same module another agent is editing"
- "repeat analysis I am already doing locally"

## Prompt Shape

Each delegated task should include:

- objective
- exact scope or file ownership
- constraints
- expected output
- reminder that other agents may also be editing elsewhere

## Integration Rules

- Review returned changes quickly before trusting them.
- Verify delegated claims the same way you would verify your own.
- Synthesize outputs into one coherent answer or patch set.
- Close subagents when their job is done.

## Recommended Patterns

### Parallel Discovery

- one subagent per independent question
- main agent synthesizes the answers

### Split Implementation

- one subagent per disjoint write surface
- main agent keeps ownership of integration and final verification

### Implementation Plus Verification

- main agent implements
- subagent verifies tests, UI, or risk areas in parallel

## Red Flags

- delegating the task you should be doing locally
- overlapping write ownership
- waiting immediately after spawning
- trusting subagent success reports without checking
- using subagents for simple work that would be faster inline

## Related Skills

- `closed-loop-delivery` for end-to-end execution against acceptance criteria
- `executing-plans` when the work follows an approved plan
- `verification-before-completion` before claiming delegated work is complete
