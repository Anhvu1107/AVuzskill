# Agent Skills Unified Architecture

This repository runs as a single canonical `.agent` system.

## Current Shape

- `skills/`
  - canonical skill library for the bundle
- `agents/`
  - specialist prompts for focused roles
- `workflows/`
  - higher-level workflow entry points
- `rules/`
  - shared global behavior constraints
- `scripts/`
  - local validation and runtime helpers
- `.shared/`
  - shared assets used by selected skills and workflows

## Operating Model

- Start with `skills/workspace-operating-system/`.
- Route from task shape to the minimum effective skill stack.
- Use one primary skill unless the task clearly spans multiple domains.
- Treat verification, ownership, and local-first safety as part of correctness.

## Core Skill Families

- Operating workflow
  - `workspace-operating-system`, `closed-loop-delivery`, `executing-plans`, `parallel-agents`, `plan-writing`
- Product and architecture
  - `app-builder`, `architecture`, `api-patterns`, `database-design`, `mcp-builder`
- Frontend and UX
  - `frontend-design`, `web-design-guidelines`, `tailwind-patterns`, `nextjs-react-expert`, `mobile-design`
- Quality and verification
  - `verification-before-completion`, `testing-patterns`, `tdd-workflow`, `webapp-testing`, `systematic-debugging`, `receiving-code-review`
- Delivery and hardening
  - `using-git-worktrees`, `finishing-a-development-branch`, `deployment-procedures`, `vulnerability-scanner`

## Canonical Rule

Do not treat imported community bundles as parallel runtime trees.

External sources may inform this repository, but the canonical runtime system is only the content that lives inside this `.agent` directory.
