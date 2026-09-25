---
trigger: always_on
---

# Supabase Connection Rule: MCP Only

## Strict Connection Constraints
1. **Never Use API Keys to Connect:**
   - Under no circumstances should API keys (anon keys, publishable keys, service-role keys, or access tokens) be used in terminal commands (e.g. `curl`, CLI scripts, ad-hoc fetch scripts) to connect to or query Supabase.
   - Never inspect or read `.env` to extract API keys for manual HTTP/REST queries or ad-hoc connections.
   - Never print or pass API keys in shell commands, scripts, code comments, or documentation.

2. **Always Use the Supabase MCP Server:**
   - All interactions with the Supabase project—including checking connectivity, inspecting database schemas, running SQL queries, creating tables, executing migrations, generating TypeScript types, managing edge functions, and reading logs—MUST be conducted exclusively via the **Supabase MCP server tools** (`execute_sql`, `list_tables`, `apply_migration`, `generate_typescript_types`, `list_edge_functions`, `deploy_edge_function`, `get_advisors`, `query_logs`).
