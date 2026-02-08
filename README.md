# StreetWise

StreetWise is an instructions pack for financial-analysis agents.

It provides:
1. Runtime policy in `AGENTS.md`
2. `CLAUDE.md` for Claude Code
3. Financial workflow skills in `skills/*/SKILL.md`
4. MCP server repository locations for finance and SEC filings

StreetWise does not bundle MCP servers. Install MCPs using each harness-native MCP flow.

## Agent Setup Steps
1. Copy `AGENTS.md` to the target project root as `AGENTS.md`.
2. For Claude Code, also copy `CLAUDE.md` to the target project root as `CLAUDE.md`.
3. Copy these skills into the target project's skills directory:
   - `skills/dcf/SKILL.md`
   - `skills/filings_deep_read/SKILL.md`
   - `skills/comp_set_analysis/SKILL.md`
4. Install these MCP servers:
   - Finance MCP: https://github.com/financial-datasets/mcp-server
   - Filings MCP: https://github.com/stefanoamorelli/sec-edgar-mcp
5. Configure required environment variables/tokens by following each MCP repository README.
6. Verify MCP tools are available.
7. Run smoke query: `Compare AAPL and MSFT revenue growth over last 3 fiscal years with sources.`

## Required Files
1. `AGENTS.md`
2. `CLAUDE.md`
3. `skills/dcf/SKILL.md`
4. `skills/filings_deep_read/SKILL.md`
5. `skills/comp_set_analysis/SKILL.md`
6. `MCP_shortlist.md` (reference)

## MCP Repositories
1. Required finance MCP: https://github.com/financial-datasets/mcp-server
2. Required filings MCP: https://github.com/stefanoamorelli/sec-edgar-mcp
3. Optional fallback finance MCP: https://github.com/massive-com/mcp_massive
