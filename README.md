# StreetWise

StreetWise is an instructions-only financial research pack for modern coding agents.

It ships:
1. `AGENTS.md` runtime policy
2. Reusable `SKILL.md` workflows
3. Curated MCP server locations (no bundled MCP servers, no installer script)

## MVP Scope
- Custom data tools in V1: `0`
- Primary data path:
  1. Codex built-in `web_search`
  2. Approved MCP finance and SEC filing servers
  3. Optional local wrappers only if MCP coverage is insufficient

## Layout
- `AGENTS.md`: Runtime policy and loop guardrails
- `MCP_shortlist.md`: Vetted MCP candidates (recent + popular + license notes + repo locations)
- `skills/`: Domain workflows (DCF, filings deep read, comp set analysis)
- `tests/golden_queries.md`: Smoke/regression prompts

## Notes
- Clean-room: do not copy Dexter source code directly; re-implement behavior only.
- Default plan is zero custom data tools:
  - Use Codex built-in web search.
  - Use existing finance MCP servers for structured market/fundamental data.
  - Use existing SEC EDGAR MCP servers for filings retrieval.
- Do not package MCP servers in this repo. Point the user's agent at MCP repo locations and let that harness install them.

## Integration Order
1. Pick one primary finance MCP from `MCP_shortlist.md`.
2. Pick one filings MCP from `MCP_shortlist.md`.
3. Have the user's harness install those MCPs using its native MCP flow.
4. Run `tests/golden_queries.md` as smoke checks.
5. Only then consider custom wrappers for unresolved gaps.

## Harness Usage
1. Codex:
- Keep `AGENTS.md` in the project root.
- Keep skills under `skills/`.
- Add MCP servers using Codex MCP commands/config, using repo locations from `MCP_shortlist.md`.

2. Claude Code:
- Keep `AGENTS.md` in the project root.
- Keep skills under `skills/` (or your Claude skill directory).
- Add MCP servers with Claude's MCP configuration flow, using repo locations from `MCP_shortlist.md`.

3. OpenCode:
- Keep `AGENTS.md` in the project root.
- Keep skills under `skills/`.
- Add MCP servers via OpenCode MCP config, using repo locations from `MCP_shortlist.md`.

4. GitHub Copilot (where MCP is supported):
- Keep policy/workflow docs in the repo.
- Configure MCP servers in Copilot-compatible MCP settings.
- Use the same MCP repo locations from `MCP_shortlist.md`.
