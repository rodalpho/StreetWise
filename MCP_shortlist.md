# StreetWise MCP Shortlist

Selection rule:
1. Recently maintained (last push within 9 months)
2. Popular (prefer >=100 stars)
3. Clear docs and usable scope
4. License compatible with project usage

Reference date for this snapshot: 2026-02-08 (UTC)
Source: GitHub API repository metadata

## Recommended Core Set (Minimum Custom Tools)
1. `financial-datasets/mcp-server`
- Use for stock/fundamental dataset retrieval
- Location: https://github.com/financial-datasets/mcp-server
- Stars: 749
- Last pushed: 2025-06-05
- License: MIT

2. `stefanoamorelli/sec-edgar-mcp`
- Use for SEC filing metadata/content
- Location: https://github.com/stefanoamorelli/sec-edgar-mcp
- Stars: 197
- Last pushed: 2026-02-08
- License: AGPL-3.0
- Note: strong functionality, but AGPL obligations must be reviewed before production embedding.

3. `massive-com/mcp_massive`
- Use as alternate market-data provider (quotes/time series)
- Location: https://github.com/massive-com/mcp_massive
- Stars: 250
- Last pushed: 2026-02-08
- License: MIT

## Additional Viable Options
1. `Alex2Yang97/yahoo-finance-mcp`
- Location: https://github.com/Alex2Yang97/yahoo-finance-mcp
- Stars: 204
- Last pushed: 2025-06-09
- License: MIT

2. `imbenrabi/Financial-Modeling-Prep-MCP-Server`
- Location: https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server
- Stars: 107
- Last pushed: 2026-02-07
- License: Apache-2.0

## Optional Lower-Priority Candidate
1. `cdtait/fmp-mcp-server`
- Location: https://github.com/cdtait/fmp-mcp-server
- Stars: 43
- Last pushed: 2025-06-23
- License: MIT
- Note: maintenance is acceptable, but popularity is below preferred threshold.

## Adoption Guidance
1. Prefer MIT/Apache-2.0 candidates first when license simplicity matters.
2. Keep one primary finance MCP and one fallback provider to reduce operational complexity.
3. Keep filings MCP separate to avoid overloading a single dependency.
4. Re-run shortlist checks monthly and update this file.
5. Do not vendor or repackage these MCP servers in StreetWise.
6. Let the target harness install MCPs using its native MCP configuration flow.
