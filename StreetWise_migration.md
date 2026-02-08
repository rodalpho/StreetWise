# StreetWise Migration Plan: Codex-Native Replacement

## Objective
Replace Dexter's primary financial-research functionality inside Codex using:
- `AGENTS.md` for orchestration policy
- `SKILL.md` files for domain workflows
- existing MCP servers for executable data access (installed by each harness)
- no bundled MCP servers and no installer script

This plan assumes:
- No custom multi-model abstraction layer
- No dedicated eval harness as a required deliverable

## Primary Dexter Functionality to Replicate
1. Tool-driven financial research (prices, fundamentals, filings, estimates, news, insider data)
2. Web search and page reading when primary financial data is insufficient
3. Repeatable multi-step workflow execution (planning, tool calls, synthesis)
4. Guardrails against looping and redundant calls
5. Skill-triggered workflows (for example, DCF valuation)
6. Persistent run artifacts for debugging and auditability

## Workstreams
1. Codex orchestration contract in `AGENTS.md`
2. Skill migration to `skills/*/SKILL.md`
3. MCP-first tooling with strict admission gate and repository location list
4. Minimal regression validation in `tests/golden_queries.md`

## Minimal Custom Tooling Strategy
1. V1 target: zero custom data tools.
2. Use Codex built-in web search + approved MCP servers.
3. Let each agent harness install MCP servers natively.
4. Add local wrappers only when an identified coverage gap persists.

## Attribution And Compliance Checklist
1. Keep a list of external MCP dependencies and repository URLs.
2. Record license type and compatibility decision for each dependency.
3. Avoid copying upstream code; use clean-room implementations when needed.
4. Re-check popularity and maintenance monthly before upgrades.

## Definition of Done
1. Codex answers complex financial prompts using executable tools.
2. Looping and duplicate retries are controlled by executable guardrails.
3. DCF and filings workflows run via skills.
4. Responses are traceable to sources and run logs.
