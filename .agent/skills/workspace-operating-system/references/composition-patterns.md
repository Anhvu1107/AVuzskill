# Composition Patterns

Use this file when one skill is not enough.

## Common Multi-Skill Stacks

### New Product Surface

- `brainstorming`
- `architecture`
- `frontend-design`
- `api-patterns`
- `database-design`
- `testing-patterns`

Use for new features, dashboards, landing pages with backend logic, or app shells.

### Full App Delivery

- `app-builder`
- `architecture`
- `frontend-design`
- `database-design`
- `deployment-procedures`
- `testing-patterns`

Use when the request is "build the app" rather than "improve one slice."

### UI Polish With Real Quality Control

- `frontend-design`
- `web-design-guidelines`
- `performance-profiling`
- `webapp-testing`

Use for redesigns, landing pages, or component-system polishing where both aesthetics and execution matter.

### Backend Feature Delivery

- `architecture`
- `api-patterns`
- `database-design`
- `testing-patterns`

Use for new endpoints, auth flows, or business logic that crosses API and schema boundaries.

### Bug Hunt

- `systematic-debugging`
- relevant domain skill
- `webapp-testing` or `testing-patterns`
- `lint-and-validate`

Use when behavior is failing and root cause is not yet obvious.

### Security Pass

- `vulnerability-scanner`
- `red-team-tactics`
- relevant domain skill
- `testing-patterns`

Use for authentication, exposed APIs, secrets handling, or risky integrations.

### Document And Messaging

- `doc-coauthoring`
- `internal-comms`
- `brand-guidelines`
- `canvas-design` when visual polish matters

Use for written deliverables, stakeholder-facing documents, briefs, and polished communication artifacts.

### Skill Bundle Maintenance

- `workspace-operating-system`
- `skill-creator`
- `plan-writing`
- `documentation-templates`

Use when adding, upgrading, or standardizing skills inside this repository.

## Composition Rules

- Name the primary skill first.
- Add only support skills that materially reduce risk or rework.
- Keep the sequence explicit: plan -> build -> verify, or reproduce -> fix -> verify.
- When two skills overlap, prefer the one closest to the actual deliverable.
