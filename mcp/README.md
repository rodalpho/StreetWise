# MCP Directory

Use this directory for project-local MCP server files.

Expected layout:
1. `mcp/financial-datasets-mcp`
2. `mcp/sec-edgar-mcp`

Repository sources:
1. Finance MCP: https://github.com/financial-datasets/mcp-server
2. Filings MCP: https://github.com/stefanoamorelli/sec-edgar-mcp

Guidelines:
1. Keep MCP installs scoped to this project.
2. Do not rely on global/user-wide MCP installs for StreetWise.
3. Review MCP files before install (README, install scripts, entrypoints, dependency manifests) to confirm safety.
4. Follow each MCP repository README for environment variables and launch details.
5. Before MCP registration, ask the user for required keys/secrets.
6. Do not run MCP add/register commands with placeholder secrets.
