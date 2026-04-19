---
name: mcp-builder
description: Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools, resources, and prompts. Use when building or improving MCP servers in Python or TypeScript, planning tool coverage, designing schemas, choosing transports, writing actionable errors, or creating evaluations for an MCP integration.
---

# MCP Builder

## Purpose

Create MCP servers that are easy for agents to discover, understand, and use effectively in real tasks.

## Recommended Process

1. Research the target API or service.
2. Review the MCP specification and framework guidance.
3. Plan tool coverage and resource design.
4. Implement the server with clear schemas and actionable errors.
5. Test the server and build evaluations.

## Design Principles

- Prefer clear, action-oriented tool names.
- Balance broad API coverage with useful workflow tools.
- Keep tools focused on one job each.
- Return predictable structured data when possible.
- Add pagination and filtering so agents can manage context efficiently.
- Write errors that help the agent recover with a concrete next step.

## Core Areas

### Tools

- Validate inputs with strong schemas.
- Describe parameters clearly.
- Mark annotations such as read-only, destructive, idempotent, and open-world behavior when supported.

### Resources

- Use static resources for fixed docs or config.
- Use dynamic resources for generated views.
- Use templates when URI parameters help agents target the right data.

### Transport

- Prefer `stdio` for local servers.
- Prefer stateless HTTP for remote servers unless a stateful transport is clearly needed.

### Security

- Validate all external input.
- Limit resource scope.
- Keep secrets in environment variables.
- Avoid exposing internal implementation details in user-facing errors.

## Testing

- Run build or syntax verification before finishing.
- Test with MCP Inspector when possible.
- Cover unit logic, integration behavior, and schema contracts.

## Evaluations

After implementation, create read-only evaluations that require realistic multi-step reasoning and have stable answers.

## References

Load these as needed:

- `reference/mcp_best_practices.md`
- `reference/node_mcp_server.md`
- `reference/python_mcp_server.md`
- `reference/evaluation.md`

## Runtime Assets

Use bundled files in `scripts/` for evaluation support and related utilities when they fit the task.
