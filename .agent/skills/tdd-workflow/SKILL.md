---
name: tdd-workflow
description: Use when implementing behavior that should be driven by tests first. Apply this skill for bug fixes, core logic, parsing, validation, state transitions, or any change where a failing test can define the expected behavior before code is written.
---

# TDD Workflow

## Purpose

Use tests to define behavior before implementation makes the answer look obvious.

TDD is most valuable when logic can drift, regressions are likely, or requirements are easiest to pin down as executable examples.

## When To Use

- bug fixes with a reproducible symptom
- new behavior with clear expected outcomes
- parsing, validation, calculation, or stateful logic
- code that is easy to verify through focused tests

## When Not To Force It

- pure visual layout exploration
- one-off glue code where test setup costs more than the logic
- tasks blocked by missing architecture decisions

## Core Cycle

1. Red
   - write or update a test that demonstrates the missing behavior
   - watch it fail for the right reason
2. Green
   - write the smallest code change that makes the test pass
3. Refactor
   - improve names, structure, and duplication while staying green

Repeat until the behavior is complete.

## Rules

- Do not write production logic before you have a failing proof.
- Keep each test focused on one behavior.
- Prefer the smallest realistic test that proves the point.
- Run the focused test first, then widen verification as confidence grows.

## Bug-Fix Pattern

1. Reproduce the bug in a test.
2. See it fail before the fix.
3. Patch the code.
4. See the test pass.
5. Run any nearby regression checks.

If you never saw the failure, you did not prove the fix.

## Green-Phase Discipline

- solve only the current test
- avoid speculative abstractions
- skip optimization until the behavior is correct

## Refactor Discipline

- keep tests green throughout
- improve one dimension at a time
- stop refactoring when the next change adds risk without meaningfully improving clarity

## Common Anti-Patterns

- writing the test after the fix
- checking only happy paths
- broad integration tests when a focused unit test would prove the behavior faster
- changing several behaviors before rerunning tests
- claiming TDD happened without ever seeing red

## Related Skills

- `testing-patterns` for broader testing strategy
- `systematic-debugging` when the failure cause is not yet understood
- `verification-before-completion` before claiming the fix is complete
