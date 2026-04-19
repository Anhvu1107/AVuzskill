# Skill Catalog

Generated from the current unified skill library.

Total skills: 53

Use this file when the correct skill is unclear and you need exhaustive coverage.

## Operating System And Workflow

- `workspace-operating-system`: Central routing, sequencing, and quality-control layer for this unified skill bundle. Use when Codex is working anywhere in this repository and needs to decide which skills to load, how to combine them, what execution mode to use, or what quality bar to apply. Especially important for broad, ambiguous, multi-step, cross-domain, or high-value requests where the right workflow matters as much as the final answer.
- `behavioral-modes`: AI operational modes (brainstorm, implement, debug, review, teach, ship, orchestrate). Use to adapt behavior based on task type.
- `brainstorming`: Socratic questioning protocol + user communication. MANDATORY for complex requests, new features, or unclear requirements. Includes progress reporting and error handling.
- `intelligent-routing`: Automatic agent selection and intelligent task routing. Analyzes user requests and automatically selects the best specialist agent(s) without requiring explicit user mentions.
- `parallel-agents`: Multi-agent orchestration patterns. Use when multiple independent tasks can run with different domain expertise or when comprehensive analysis requires multiple perspectives.
- `plan-writing`: Structured task planning with clear breakdowns, dependencies, and verification criteria. Use when implementing features, refactoring, or any multi-step work.
- `skill-creator`: Create new skills, modify and improve existing skills, and measure skill performance. Use when users want to create a skill from scratch, edit, or optimize an existing skill, run evals to test a skill, benchmark skill performance with variance analysis, or optimize a skill's description for better triggering accuracy.
- `documentation-templates`: Documentation templates and structure guidelines. README, API docs, code comments, and AI-friendly documentation.
- `skillAVuz`: A unified Super-Agent framework combining Antigravity Kit (.agent) principles, Anthropic Claude skills (skills-main), and Core Engine Upgrades (RAG Memory & Sandbox).

## Architecture And Delivery

- `app-builder`: Main application building orchestrator. Creates full-stack applications from natural language requests. Determines project type, selects tech stack, coordinates agents.
- `architecture`: Architectural decision-making framework. Requirements analysis, trade-off evaluation, ADR documentation. Use when making architecture decisions or analyzing system design.
- `deployment-procedures`: Production deployment principles and decision-making. Safe deployment workflows, rollback strategies, and verification. Teaches thinking, not scripts.
- `clean-code`: Pragmatic coding standards - concise, direct, no over-engineering, no unnecessary comments
- `server-management`: Server management principles and decision-making. Process management, monitoring strategy, and scaling decisions. Teaches thinking, not commands.

## Frontend And Experience

- `frontend-design`: Design and implement distinctive, production-grade frontend interfaces with strong UX reasoning and a clear visual point of view. Use when Codex needs to create or improve web pages, landing pages, dashboards, components, app shells, or other frontend UI; choose typography, color, layout, spacing, backgrounds, or motion; turn vague visual goals into a coherent direction; or avoid generic AI-looking output while preserving accessibility, responsiveness, and usability.
- `web-design-guidelines`: Review UI code for Web Interface Guidelines compliance. Use when asked to "review my UI", "check accessibility", "audit design", "review UX", or "check my site against best practices".
- `tailwind-patterns`: Tailwind CSS v4 principles. CSS-first configuration, container queries, modern patterns, design token architecture.
- `react-best-practices`: React and Next.js performance optimization from Vercel Engineering. Use when building React components, optimizing performance, eliminating waterfalls, reducing bundle size, reviewing code for performance issues, or implementing server/client-side optimizations.
- `mobile-design`: Mobile-first design thinking and decision-making for iOS and Android apps. Touch interaction, performance patterns, platform conventions. Teaches principles, not fixed values. Use when building React Native, Flutter, or native mobile apps.
- `seo-fundamentals`: SEO fundamentals, E-E-A-T, Core Web Vitals, and Google algorithm principles.
- `theme-factory`: Toolkit for styling artifacts with a theme. These artifacts can be slides, docs, reportings, HTML landing pages, etc. There are 10 pre-set themes with colors/fonts that you can apply to any artifact that has been creating, or can generate a new theme on-the-fly.
- `web-artifacts-builder`: Suite of tools for creating elaborate, multi-component claude.ai HTML artifacts using modern frontend web technologies (React, Tailwind CSS, shadcn/ui). Use for complex artifacts requiring state management, routing, or shadcn/ui components - not for simple single-file HTML/JSX artifacts.

## Backend And Data

- `api-patterns`: API design principles and decision-making. REST vs GraphQL vs tRPC selection, response formats, versioning, pagination.
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
- `testing-patterns`: Testing patterns and principles. Unit, integration, mocking strategies.
- `tdd-workflow`: Test-Driven Development workflow principles. RED-GREEN-REFACTOR cycle.
- `webapp-testing`: Toolkit and workflow for interacting with and testing web applications using Playwright. Use when Codex needs to verify local or remote web app behavior, discover routes and selectors, run end-to-end checks, inspect rendered DOM, capture screenshots, review console output, or debug frontend flows with browser automation.
- `lint-and-validate`: Automatic quality control, linting, and static analysis procedures. Use after every code modification to ensure syntax correctness and project standards. Triggers onKeywords: lint, format, check, validate, types, static analysis.
- `performance-profiling`: Performance profiling principles. Measurement, analysis, and optimization techniques.
- `systematic-debugging`: 4-phase systematic debugging methodology with root cause analysis and evidence-based verification. Use when debugging complex issues.
- `vulnerability-scanner`: Advanced vulnerability analysis principles. OWASP 2025, Supply Chain Security, attack surface mapping, risk prioritization.
- `red-team-tactics`: Red team tactics principles based on MITRE ATT&CK. Attack phases, detection evasion, reporting.

## Documents And Artifacts

- `docx`: "Use this skill whenever the user wants to create, read, edit, or manipulate Word documents (.docx files). Triggers include: any mention of 'Word doc', 'word document', '.docx', or requests to produce professional documents with formatting like tables of contents, headings, page numbers, or letterheads. Also use when extracting or reorganizing content from .docx files, inserting or replacing images in documents, performing find-and-replace in Word files, working with tracked changes or comments, or converting content into a polished Word document. If the user asks for a 'report', 'memo', 'letter', 'template', or similar deliverable as a Word or .docx file, use this skill. Do NOT use for PDFs, spreadsheets, Google Docs, or general coding tasks unrelated to document generation."
- `pptx`: "Use this skill any time a .pptx file is involved in any way — as input, output, or both. This includes: creating slide decks, pitch decks, or presentations; reading, parsing, or extracting text from any .pptx file (even if the extracted content will be used elsewhere, like in an email or summary); editing, modifying, or updating existing presentations; combining or splitting slide files; working with templates, layouts, speaker notes, or comments. Trigger whenever the user mentions \"deck,\" \"slides,\" \"presentation,\" or references a .pptx filename, regardless of what they plan to do with the content afterward. If a .pptx file needs to be opened, created, or touched, use this skill."
- `xlsx`: "Use this skill any time a spreadsheet file is the primary input or output. This means any task where the user wants to: open, read, edit, or fix an existing .xlsx, .xlsm, .csv, or .tsv file (e.g., adding columns, computing formulas, formatting, charting, cleaning messy data); create a new spreadsheet from scratch or from other data sources; or convert between tabular file formats. Trigger especially when the user references a spreadsheet file by name or path — even casually (like \"the xlsx in my downloads\") — and wants something done to it or produced from it. Also trigger for cleaning or restructuring messy tabular data files (malformed rows, misplaced headers, junk data) into proper spreadsheets. The deliverable must be a spreadsheet file. Do NOT trigger when the primary deliverable is a Word document, HTML report, standalone Python script, database pipeline, or Google Sheets API integration, even if tabular data is involved."
- `pdf`: Use this skill whenever the user wants to do anything with PDF files. This includes reading or extracting text/tables from PDFs, combining or merging multiple PDFs into one, splitting PDFs apart, rotating pages, adding watermarks, creating new PDFs, filling PDF forms, encrypting/decrypting PDFs, extracting images, and OCR on scanned PDFs to make them searchable. If the user mentions a .pdf file or asks to produce one, use this skill.
- `doc-coauthoring`: Guide users through a structured workflow for co-authoring documentation. Use when user wants to write documentation, proposals, technical specs, decision docs, or similar structured content. This workflow helps users efficiently transfer context, refine content through iteration, and verify the doc works for readers. Trigger when user mentions writing docs, creating proposals, drafting specs, or similar documentation tasks.
- `internal-comms`: A set of resources to help me write all kinds of internal communications, using the formats that my company likes to use. Claude should use this skill whenever asked to write some sort of internal communications (status reports, leadership updates, 3P updates, company newsletters, FAQs, incident reports, project updates, etc.).
- `slack-gif-creator`: Knowledge and utilities for creating animated GIFs optimized for Slack. Provides constraints, validation tools, and animation concepts. Use when users request animated GIFs for Slack like "make me a GIF of X doing Y for Slack."

## Creative And Brand

- `brand-guidelines`: Applies Anthropic's official brand colors and typography to any sort of artifact that may benefit from having Anthropic's look-and-feel. Use it when brand colors or style guidelines, visual formatting, or company design standards apply.
- `canvas-design`: Create beautiful visual art in .png and .pdf documents using design philosophy. You should use this skill when the user asks to create a poster, piece of art, design, or other static piece. Create original visual designs, never copying existing artists' work to avoid copyright violations.
- `algorithmic-art`: Creating algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Use this when users request creating art using code, generative art, algorithmic art, flow fields, or particle systems. Create original algorithmic art rather than copying existing artists' work to avoid copyright violations.

## Specialized Domains

- `game-development`: Game development orchestrator. Routes to platform-specific skills based on project needs.
- `geo-fundamentals`: Generative Engine Optimization for AI search engines (ChatGPT, Claude, Perplexity).
- `i18n-localization`: Internationalization and localization patterns. Detecting hardcoded strings, managing translations, locale files, RTL support.
