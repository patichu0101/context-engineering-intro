# 🛠 CRITICAL: CODE OPERATIONS RULE

All code editing and symbol queries MUST use Serena MCP tools.

## ✅ Primary Tools

- `serena:find_symbol(name_path="ClassName", include_body=true)`
- `serena:replace_symbol_body(name_path="function", body="...")`
- `serena:search_for_pattern(substring_pattern="TODO|FIXME")`
- `serena:get_symbols_overview(relative_path="src/")`

## 🔁 Fallback (only if Serena fails)

- `grep`, `sed`, or manual code navigation
- ONLY for exceptional cases (legacy shell scripts, broken metadata)

## 📍 Rule Coverage

These apply to:
- All agents and subagents
- All mono/multi-repo environments
