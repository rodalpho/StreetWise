# StreetWise

StreetWise is a lightweight install pack for financial-analysis agents.

## Quickstart
Tell your agent:

```text
1) git clone https://github.com/rodalpho/StreetWise .
2) AGENTS.md and skills/ are now in the project root.
3) Keep MCP server files under this project in ./mcp/:
   - ./mcp/financial-datasets-mcp
   - ./mcp/sec-edgar-mcp
4) Install these MCP servers with this harness's native MCP flow, scoped to this project only (not global/user-wide):
   - Finance: https://github.com/financial-datasets/mcp-server
   - Filings: https://github.com/stefanoamorelli/sec-edgar-mcp
5) Configure any required env vars/tokens from each MCP README.
6) Verify MCP tools are available, then run:
   "Compare AAPL and MSFT revenue growth over last 3 fiscal years with sources."
```
