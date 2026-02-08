# StreetWise

StreetWise is a lightweight install pack for financial-analysis agents.

## Quickstart
Tell your agent:

```text
1) Clone https://github.com/rodalpho/StreetWise into . and follow README.md.
2) AGENTS.md and skills/ are now in the project root.
3) Keep MCP server files under this project in ./mcp/:
   - ./mcp/financial-datasets-mcp
   - ./mcp/sec-edgar-mcp
4) Read each MCP README and identify required API keys/env vars.
5) Ask the user for required secrets before running MCP install/register commands.
6) Install these MCP servers with this harness's native MCP flow, scoped to this project only (not global/user-wide):
   - Finance: https://github.com/financial-datasets/mcp-server
   - Filings: https://github.com/stefanoamorelli/sec-edgar-mcp
7) Use real user-provided values only. Never register MCPs with placeholder values like REPLACE_WITH_REAL_KEY.
8) Verify MCP tools are available, then run:
   "Compare AAPL and MSFT revenue growth over last 3 fiscal years with sources."
```
