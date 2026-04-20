---
name: skill-creator
description: Use when creating a new skill, rewriting an existing skill, or tightening a skill so future agents can trigger it correctly and follow it reliably. Apply this skill for skill design, metadata cleanup, workflow refactors, validation, and bundled-resource decisions inside this repository.
---

# Skill Creator

## Purpose

Build skills that are easy to trigger, easy to follow, and honest about what they require.

The goal is not to produce more files. The goal is to produce a better operating guide for future agents.

## Start Here

For any new or updated skill, define:

- the exact situations that should trigger it
- the workflow or judgment it should teach
- the resources it needs beyond the core instructions
- how another agent would verify the skill is useful

## Workflow

1. Capture intent.
   - what job should the skill help an agent do?
2. Define the trigger language.
   - write the frontmatter description around when to use the skill, not a long process summary
3. Draft the core workflow.
   - keep SKILL.md focused on decisions, sequence, and quality bar
4. Split only when needed.
   - move heavy detail into `references/`, deterministic helpers into `scripts/`, reusable outputs into `assets/`
5. Add UI metadata.
   - create or refresh `agents/openai.yaml` for important skills
6. Validate.
   - confirm the wording is clear, the references exist, and the workflow matches the actual repo

## Writing Rules

- Keep the description focused on triggering conditions.
- Keep the body focused on what the agent should actually do.
- Prefer concise structure over narrative explanation.
- Remove stale ecosystem references that do not apply to this repo.
- Do not promise scripts, tools, or flows that are missing.

## Progressive Disclosure

Use this split:

- `SKILL.md` for the primary operating guide
- `references/` for optional depth
- `scripts/` for repeatable utilities
- `assets/` for templates or output resources

If a detail does not need to load on every trigger, move it out of the core file.

## Validation Checklist

- does the description make the skill discoverable?
- does the body tell the agent what to do next?
- are all referenced files real and relevant?
- is the skill aligned with Codex tools and this repo's structure?
- would another agent know when not to use it?

## Updating Existing Skills

When improving an inherited skill:

- remove stale brand or platform references
- rewrite around the actual environment and tools available now
- merge overlapping ideas instead of duplicating another skill
- keep the result stylistically consistent with the rest of the bundle

## Useful Local Assets

Use the existing local helpers only when they materially help the task:

- `scripts/quick_validate.py`
- `scripts/package_skill.py`
- `eval-viewer/`
- `references/schemas.md`

Do not force an evaluation loop when a smaller validation pass is enough.

## Related Skills

- `workspace-operating-system` for routing and quality expectations
- `plan-writing` for multi-step skill upgrade work
- `verification-before-completion` before claiming a skill is ready
