# StreetWise

StreetWise is a lightweight install pack for financial-analysis agents.

## Quickstart
Tell your agent:

```text
1) Clone https://github.com/rodalpho/StreetWise into . and follow README.md.
2) Download the SEC filings MCP server repository into this project under ./mcp/:
   - git clone https://github.com/stefanoamorelli/sec-edgar-mcp ./mcp/sec-edgar-mcp
3) Review MCP repository files (README, install scripts, server entrypoints, dependency manifests) to confirm they are safe to run.
4) Read each MCP README/docs and identify required API keys/env vars.
5) Ask the user for required secrets before running MCP install/register commands:
   - SEC EDGAR: ask for contact name + email to set SEC_EDGAR_USER_AGENT as "Name (email@domain.com)".
   - Financial Datasets: ask for API key first. If user does not have one, direct them to:
     - Sign up: https://financialdatasets.ai/register
     - API key dashboard (after sign-in): https://financialdatasets.ai/
6) Configure Financial Datasets as a remote MCP server endpoint:
   - https://mcp.financialdatasets.ai/mcp
7) Install/register these MCP servers with this harness's native MCP flow, scoped to this project only (not global/user-wide):
   - Finance (remote): https://mcp.financialdatasets.ai/mcp
   - Filings: https://github.com/stefanoamorelli/sec-edgar-mcp
8) Use real user-provided values only. Never register MCPs with placeholder values like REPLACE_WITH_REAL_KEY.
9) Verify MCP tools are available, then run:
   "Compare AAPL and MSFT revenue growth over last 3 fiscal years with sources."
```
