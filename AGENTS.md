# Project Rules & Guidelines

## Supabase Connection & Tool Usage Policy

### 1. Never Use API Keys to Connect
- **Strictly Prohibited:** NEVER use API keys (anon keys, publishable keys, service-role keys, or access tokens) in terminal commands (e.g., `curl`, shell scripts, CLI commands, or custom test scripts) to connect to, query, or test Supabase.
- **No Reading Keys for Manual Requests:** Do not inspect, read, or parse `.env` to extract API keys or tokens for making manual HTTP/REST or direct client queries.
- **Zero Key Exposure:** Never hardcode, paste, or print API keys in source code, configuration files, terminal commands, or documentation.

### 2. Always Use the Supabase MCP Server
- **Mandatory Tooling:** ALL database operations, connectivity verifications, schema inspections, SQL executions, migrations, type generation, edge function deployments, and diagnostics MUST be performed exclusively via the **Supabase MCP server tools**.
- **MCP Tool Mapping:**
  - Connectivity tests / queries: `execute_sql` (using `project_id: "ivmfzbdzgzvcgzvwmolf"`)
  - Schema inspection: `list_tables`
  - Migrations and DDL: `apply_migration`
  - TypeScript type generation: `generate_typescript_types`
  - Edge functions: `list_edge_functions`, `deploy_edge_function`, `get_edge_function`
  - Security & diagnostics: `get_advisors`, `query_logs`
