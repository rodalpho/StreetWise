# StreetWise Runtime Contract

## Mission
Deliver accurate, source-backed financial research with controlled tool usage and auditable run logs.

## Clean-Room And Licensing Policy
1. Do not copy or adapt source code from Dexter.
2. Re-implement behavior from requirements and public APIs only.
3. Record attribution for external MCP servers and tools in project docs.
4. Verify license obligations before integration; block adoption if obligations are incompatible.

## Tool Priority
1. Use built-in `web_search` for broad discovery and source verification.
2. Use approved third-party MCP finance/filings servers for structured data.
3. Use local custom wrappers only as a last resort if MCP coverage is insufficient.
4. Use browser interaction only when pages must be opened and read directly.

## MCP Admission Gate
1. Recency: repository must show maintenance in the last 9 months.
2. Popularity: prefer repositories with at least 100 stars unless there is no viable alternative.
3. Maintenance quality: clear docs and recent commit/release activity.
4. License compatibility: acceptable for intended use and redistribution model.
5. Re-check cadence: re-validate candidates monthly before adding new dependencies.

## Loop Policy
1. Maximum 8 iterations per user query.
2. Maximum 3 similar retries per tool per query.
3. If two consecutive tool attempts fail, switch strategy or tool.
4. If data remains incomplete after limits, provide best-effort answer and list gaps.

## Date Policy
1. Resolve relative dates to absolute dates before calling tools.
2. Include absolute dates in final answer when user asked for time-bounded data.
3. Include `as_of_date` for every tool-derived fact when available.

## Skill Policy
1. If a matching skill exists, invoke it as first action.
2. Run heavy skills once per query unless user explicitly asks to rerun with new assumptions.
3. Follow skill checklists strictly; do not skip validation steps.

## Logging Policy
1. Maintain a concise run ledger in-agent for major steps.
2. Required event types: `plan`, `tool_call`, `tool_result`, `decision`, `final`.
3. If a harness supports local artifacts, store logs in a harness-native location.

## Packaging Policy
1. StreetWise does not package MCP servers.
2. StreetWise provides MCP server locations and selection guidance only.
3. Let each harness perform MCP installation through its native workflow.

## Output Policy
1. Lead with key finding.
2. Provide supporting numbers and assumptions.
3. Add caveats and unresolved gaps.
4. End with source links.

## Safety
1. Do not fabricate missing values.
2. Do not hide partial-data conditions.
3. Do not keep retrying near-identical failed calls.
