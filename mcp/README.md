# MCP Directory

Use this directory for project-local MCP server files.

Expected layout:
1. `mcp/sec-edgar-mcp`

Download commands:
1. `git clone https://github.com/stefanoamorelli/sec-edgar-mcp ./mcp/sec-edgar-mcp`

Repository sources:
1. Finance MCP (remote streamable HTTP): https://mcp.financialdatasets.ai/mcp
2. Filings MCP (local clone): https://github.com/stefanoamorelli/sec-edgar-mcp

Guidelines:
1. Keep MCP installs scoped to this project.
2. Do not rely on global/user-wide MCP installs for StreetWise.
3. Financial Datasets uses remote HTTP MCP with OAuth sign-in for StreetWise.
4. For remote MCP endpoints, review official docs and auth requirements before registration.
5. For local MCP repos, review files before install (README, install scripts, entrypoints, dependency manifests) to confirm safety.
6. Follow each MCP README/docs for environment variables and launch details.
7. Before MCP registration, ask the user for required keys/secrets.
8. Do not run MCP add/register commands with placeholder secrets.
