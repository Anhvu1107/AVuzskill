# Agent Skills Unified

This repository is a truly merged skill system that combines the local `.agent` toolkit and the `skills-main` repository into one operating system for future AI agents.

For day-to-day usage, start with `HUONG_DAN_SU_DUNG.md`.

## Mission

Make the workspace self-describing enough that an AI can enter cold, choose the right skill set, sequence work correctly, and finish with a consistent quality bar.

## Primary Entry Point

Start with `$workspace-operating-system`.

That skill is the routing and execution layer for the entire bundle. It tells an AI:

- how to classify the request
- which minimum set of skills to load
- when to stay narrow versus compose multiple skills
- what validation standard to apply before finishing

## Canonical Structure

- `.agent/skills/`
  - The one and only canonical skill library for the merged system
  - Contains the upgraded merged skills plus all unique skills brought in from both source projects
  - Now includes stronger workflow control for planning, isolated branch work, review handling, end-to-end delivery, and verification discipline
- `.agent/agents/`
  - Specialist agent prompts
- `.agent/workflows/`
  - Workflow entry points
- `.agent/rules/`, `.agent/scripts/`, `.agent/.shared/`
  - Runtime rules, validators, and shared assets
- `spec/`, `template/`, `.claude-plugin/`
  - Preserved from `skills-main` for ecosystem compatibility

## Security And Ownership Hardening

- The bundle now ships with one local-first default profile.
- `.agent/mcp_config.json` is intentionally empty, so no external MCP server is enabled by default.
- Stale ownership metadata and broken `./skills/...` marketplace paths were removed from `.claude-plugin/marketplace.json`.
- Restrictive office-document skills were removed from the public bundle so the repository stays clean to redistribute and review.
- Runtime side effects such as preview PID/log files are now ignored by git.
- Incoming community bundles are audited before merge; launcher files and external app shells are not imported into the canonical skill tree.

## Upgraded Core Layer

The repository now includes an explicit operating layer:

- `.agent/skills/workspace-operating-system`
  - central routing, execution, and quality-control skill
- `.agent/skills/workspace-operating-system/references/task-routing.md`
  - fast map from task shape to skill selection
- `.agent/skills/workspace-operating-system/references/composition-patterns.md`
  - recommended multi-skill bundles for common request types
- `.agent/skills/workspace-operating-system/references/quality-bar.md`
  - universal finish criteria for all serious work
- `.agent/skills/workspace-operating-system/references/skill-catalog.md`
  - full inventory of available skills

## What Was Actually Merged

- Both source projects were consolidated into one repo.
- Duplicate skill trees were collapsed into a single canonical location: `.agent/skills/`.
- High-value overlapping skills were manually unified and upgraded:
  - `.agent/skills/frontend-design`
  - `.agent/skills/mcp-builder`
  - `.agent/skills/webapp-testing`
- Additional workflow skills were rewritten into the bundle in local house style:
  - `.agent/skills/verification-before-completion`
  - `.agent/skills/using-git-worktrees`
  - `.agent/skills/executing-plans`
  - `.agent/skills/receiving-code-review`
  - `.agent/skills/closed-loop-delivery`
  - `.agent/skills/finishing-a-development-branch`
- Restrictive-license office skills were removed during hardening:
  - `.agent/skills/docx`
  - `.agent/skills/pdf`
  - `.agent/skills/pptx`
  - `.agent/skills/xlsx`

## Design Principles

- Prefer one strong entry skill over scattered implicit assumptions.
- Keep progressive disclosure: read only the references needed for the task.
- Favor execution, validation, and clarity over vague advice.
- Keep the merged repo structurally honest: one skill tree, not two mirrored trees.
- Prefer rewritten, repo-aligned workflows over wholesale imports from external bundles.
