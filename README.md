# Agent Skills Unified

This repository is a premium unified skill bundle that combines the local `.agent` toolkit and the `skills-main` repository into one operating system for future AI agents.

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

## Bundle Structure

- `skills/`
  - Canonical skill library for the unified system
  - Includes the merged high-value skills plus all unique skills from both source projects
- `.agent/`
  - Keeps local agent runtime assets available
  - `.agent/skills` points to the same unified `skills/` directory
- `spec/`, `template/`, `.claude-plugin/`
  - Preserved from `skills-main` for ecosystem compatibility

## Upgraded Core Layer

The repository now includes an explicit operating layer:

- `skills/workspace-operating-system`
  - central routing, execution, and quality-control skill
- `skills/workspace-operating-system/references/task-routing.md`
  - fast map from task shape to skill selection
- `skills/workspace-operating-system/references/composition-patterns.md`
  - recommended multi-skill bundles for common request types
- `skills/workspace-operating-system/references/quality-bar.md`
  - universal finish criteria for all serious work
- `skills/workspace-operating-system/references/skill-catalog.md`
  - full inventory of available skills

## Merged Skills

These duplicate skills were upgraded and unified manually:

- `skills/frontend-design`
- `skills/mcp-builder`
- `skills/webapp-testing`

They now have stronger instructions and UI metadata so they are easier for future agents to discover and invoke reliably.

## Design Principles

- Prefer one strong entry skill over scattered implicit assumptions.
- Keep progressive disclosure: read only the references needed for the task.
- Minimize duplicated content and preserve traceability to original sources.
- Favor execution, validation, and clarity over vague advice.

## Source Preservation

- Unique skills are linked from their original locations where possible.
- Runtime and reference-heavy directories are preserved through junctions to avoid unnecessary duplication.
- The unified repository is the intended single entry point going forward.
