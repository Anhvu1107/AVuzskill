# Skill Catalog

Generated from the current unified skill library.

Total skills: 54

Use this file when the correct skill is unclear and you need exhaustive coverage.

## Operating System And Workflow

- `workspace-operating-system`: Central routing, sequencing, and quality-control layer for this unified skill bundle. Use when Codex is working anywhere in this repository and needs to decide which skills to load, how to combine them, what execution mode to use, or what quality bar to apply. Especially important for broad, ambiguous, multi-step, cross-domain, or high-value requests where the right workflow matters as much as the final answer.
- `behavioral-modes`: AI operational modes (brainstorm, implement, debug, review, teach, ship, orchestrate). Use to adapt behavior based on task type.
- `brainstorming`: Socratic questioning protocol + user communication. MANDATORY for complex requests, new features, or unclear requirements. Includes progress reporting and error handling.
- `closed-loop-delivery`: Use when a coding task should be driven to a real done state with explicit acceptance criteria, implementation, verification, review response, and runtime confirmation where needed. Apply this skill for end-to-end delivery, not just code edits.
- `executing-plans`: Use when there is already a written plan or clear task list and the next job is to execute it carefully. Apply this skill when implementation should follow an approved sequence, checkpoint, or plan document instead of improvising from scratch.
- `finishing-a-development-branch`: Use when a branch or worktree is functionally complete and the next step is to decide how to wrap it up. Apply this skill before pushing, opening a PR, merging, keeping, or discarding completed branch work.
- `intelligent-routing`: Automatic agent selection and intelligent task routing. Analyzes user requests and automatically selects the best specialist agent(s) without requiring explicit user mentions.
- `parallel-agents`: Use when a task contains multiple independent questions, investigations, or implementation slices that can run in parallel without blocking the next local step. Apply this skill to split work cleanly across subagents with explicit ownership, no duplicated effort, and controlled integration.
- `plan-writing`: Use when a task needs a clear execution plan before implementation starts. Apply this skill for multi-step features, meaningful refactors, risky bug fixes, or any work where sequence, scope, ownership, and verification should be made explicit first.
- `skill-creator`: Use when creating a new skill, rewriting an existing skill, or tightening a skill so future agents can trigger it correctly and follow it reliably. Apply this skill for skill design, metadata cleanup, workflow refactors, validation, and bundled-resource decisions inside this repository.
- `using-git-worktrees`: Use when work should happen in an isolated git workspace instead of the current checkout. Apply this skill for risky feature work, parallel branches, review fixes, or any task that benefits from a clean worktree with a known baseline.
- `verification-before-completion`: Use when an agent is about to say work is done, fixed, passing, ready to merge, or ready to ship. Apply this skill whenever a completion claim needs fresh evidence from commands, tests, runtime checks, or direct inspection instead of assumption.
- `documentation-templates`: Documentation templates and structure guidelines. README, API docs, code comments, and AI-friendly documentation.

## Architecture And Delivery

- `app-builder`: Use when a request is really about building or extending an application, not just changing one isolated file. Apply this skill for turning product asks into app shape, stack choices, delivery sequence, and the right supporting skills or templates.
- `architecture`: Use when the hard part of a request is choosing system shape, boundaries, tradeoffs, or scaling direction before implementation begins. Apply this skill for system design, architecture reviews, major refactors, platform choices, and ADR-worthy decisions.
- `deployment-procedures`: Production deployment principles and decision-making. Safe deployment workflows, rollback strategies, and verification. Teaches thinking, not scripts.
- `clean-code`: Pragmatic coding standards - concise, direct, no over-engineering, no unnecessary comments
- `server-management`: Server management principles and decision-making. Process management, monitoring strategy, and scaling decisions. Teaches thinking, not commands.

## Frontend And Experience

- `frontend-design`: Design and implement distinctive, production-grade frontend interfaces with strong UX reasoning and a clear visual point of view. Use when Codex needs to create or improve web pages, landing pages, dashboards, components, app shells, or other frontend UI; choose typography, color, layout, spacing, backgrounds, or motion; turn vague visual goals into a coherent direction; or avoid generic AI-looking output while preserving accessibility, responsiveness, and usability.
- `web-design-guidelines`: Review UI code for Web Interface Guidelines compliance. Use when asked to "review my UI", "check accessibility", "audit design", "review UX", or "check my site against best practices".
- `tailwind-patterns`: Tailwind CSS v4 principles. CSS-first configuration, container queries, modern patterns, design token architecture.
- `nextjs-react-expert`: Use when a React or Next.js task is bottlenecked by performance, rendering strategy, bundle size, client-server boundaries, or data-fetching behavior. Apply this skill for optimization, performance reviews, and modern Next.js execution choices.
- `mobile-design`: Mobile-first design thinking and decision-making for iOS and Android apps. Touch interaction, performance patterns, platform conventions. Teaches principles, not fixed values. Use when building React Native, Flutter, or native mobile apps.
- `seo-fundamentals`: SEO fundamentals, E-E-A-T, Core Web Vitals, and Google algorithm principles.
- `theme-factory`: Toolkit for styling artifacts with a theme. These artifacts can be slides, docs, reportings, HTML landing pages, etc. There are 10 pre-set themes with colors/fonts that you can apply to any artifact that has been creating, or can generate a new theme on-the-fly.
- `web-artifacts-builder`: Suite of tools for creating elaborate, multi-component HTML artifacts using modern frontend web technologies (React, Tailwind CSS, shadcn/ui). Use for complex artifacts requiring state management, routing, or shadcn/ui components - not for simple single-file HTML/JSX artifacts.

## Backend And Data

- `api-patterns`: Use when designing or reviewing an API contract, endpoint shape, transport style, versioning strategy, authentication model, or error format. Apply this skill for REST, GraphQL, and tRPC decisions, not just endpoint implementation details.
- `database-design`: Database design principles and decision-making. Schema design, indexing strategy, ORM selection, serverless databases.
- `mcp-builder`: Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools, resources, and prompts. Use when building or improving MCP servers in Python or TypeScript, planning tool coverage, designing schemas, choosing transports, writing actionable errors, or creating evaluations for an MCP integration.
- `nodejs-best-practices`: Node.js development principles and decision-making. Framework selection, async patterns, security, and architecture. Teaches thinking, not copying.
- `python-patterns`: Python development principles and decision-making. Framework selection, async patterns, type hints, project structure. Teaches thinking, not copying.
- `rust-pro`: Master Rust 1.75+ with modern async patterns, advanced type system
- `claude-api`: "Build, debug, and optimize Claude API / Anthropic SDK apps. Apps built with this skill should include prompt caching. Also handles migrating existing Claude API code between Claude model versions (4.5 → 4.6, 4.6 → 4.7, retired-model replacements). TRIGGER when: code imports `anthropic`/`@anthropic-ai/sdk`; user asks for the Claude API, Anthropic SDK, or Managed Agents; user adds/modifies/tunes a Claude feature (caching, thinking, compaction, tool use, batch, files, citations, memory) or model (Opus/Sonnet/Haiku) in a file; questions about prompt caching / cache hit rate in an Anthropic SDK project. SKIP: file imports `openai`/other-provider SDK, filename like `*-openai.py`/`*-generic.py`, provider-neutral code, general programming/ML."
- `powershell-windows`: PowerShell Windows patterns. Critical pitfalls, operator syntax, error handling.
- `bash-linux`: Bash/Linux terminal patterns. Critical commands, piping, error handling, scripting. Use when working on macOS or Linux systems.

## Quality And Verification

- `code-review-checklist`: Code review guidelines covering code quality, security, and best practices.
- `receiving-code-review`: Use when review comments, requested changes, or code-review feedback need to be interpreted and acted on. Apply this skill when an agent should evaluate feedback technically, clarify ambiguous items, and fix valid issues without blind agreement.
- `testing-patterns`: Testing patterns and principles. Unit, integration, mocking strategies.
- `tdd-workflow`: Use when implementing behavior that should be driven by tests first. Apply this skill for bug fixes, core logic, parsing, validation, state transitions, or any change where a failing test can define the expected behavior before code is written.
- `webapp-testing`: Toolkit and workflow for interacting with and testing web applications using Playwright. Use when Codex needs to verify local or remote web app behavior, discover routes and selectors, run end-to-end checks, inspect rendered DOM, capture screenshots, review console output, or debug frontend flows with browser automation.
- `lint-and-validate`: Automatic quality control, linting, and static analysis procedures. Use after every code modification to ensure syntax correctness and project standards. Triggers onKeywords: lint, format, check, validate, types, static analysis.
- `performance-profiling`: Performance profiling principles. Measurement, analysis, and optimization techniques.
- `systematic-debugging`: 4-phase systematic debugging methodology with root cause analysis and evidence-based verification. Use when debugging complex issues.
- `vulnerability-scanner`: Advanced vulnerability analysis principles. OWASP 2025, Supply Chain Security, attack surface mapping, risk prioritization.
- `red-team-tactics`: Authorized adversary-simulation and detection-engineering patterns for defensive security work. Use for ATT&CK-based coverage mapping, purple-team planning, tabletop exercises, and detection-gap analysis. Do not use this skill to provide exploit instructions, malware tactics, or unauthorized intrusion guidance.

## Documents And Artifacts

- `doc-coauthoring`: Guide users through a structured workflow for co-authoring documentation. Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content. This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers. Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.
- `internal-comms`: A set of resources to help write internal communications using consistent company-ready formats. Use this skill whenever asked to draft internal updates, leadership notes, 3P updates, newsletters, FAQs, incident reports, or project communications.
- `slack-gif-creator`: Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like "make me a GIF of X doing Y for Slack."

## Creative And Brand

- `brand-guidelines`: Applies a consistent brand palette and typography system to artifacts that need a polished visual identity. Use it when brand colors, style guidelines, visual formatting, or company design standards apply.
- `canvas-design`: Create beautiful visual art in .png and .pdf documents using design philosophy. You should use this skill when the user asks to create a poster, piece of art, design, or other static piece. Create original visual designs, never copying existing artists' work to avoid copyright violations.
- `algorithmic-art`: Creating algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Use this when users request creating art using code, generative art, algorithmic art, flow fields, or particle systems. Create original algorithmic art rather than copying existing artists' work to avoid copyright violations.

## Specialized Domains

- `game-development`: Game development orchestrator. Routes to platform-specific skills based on project needs.
- `geo-fundamentals`: Generative Engine Optimization for AI search engines (ChatGPT, Claude, Perplexity).
- `i18n-localization`: Internationalization and localization patterns. Detecting hardcoded strings, managing translations, locale files, RTL support.
