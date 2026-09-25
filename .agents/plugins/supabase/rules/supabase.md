---
trigger: always_on
---

# Supabase Project Rules & Guidelines

## Active Project Details
- **Project Ref:** `ivmfzbdzgzvcgzvwmolf`
- **Project URL:** `https://ivmfzbdzgzvcgzvwmolf.supabase.co`
- **Config file:** `.agents/plugins/supabase/mcp_config.json`
- **Type Definitions:** `src/types/database.types.ts`
- **Client Helper:** `src/lib/supabaseClient.ts`

## Database & Schema Guidelines
1. **Inspect Before Altering:** Always inspect existing tables via `list_tables` before generating or running migrations.
2. **Row Level Security (RLS):** Every new table in the `public` schema MUST have RLS enabled (`ALTER TABLE ... ENABLE ROW LEVEL SECURITY;`) and explicit security policies (`CREATE POLICY ...`).
3. **Primary Keys & Timestamps:** Every table must have a primary key (e.g., `id uuid DEFAULT gen_random_uuid() PRIMARY KEY` or identity bigint) and `created_at timestamptz DEFAULT now()`.
4. **Foreign Key Integrity:** Use proper foreign key constraints with `ON DELETE CASCADE` or `ON DELETE SET NULL` when referencing parent records.
5. **Type Generation:** Whenever the schema changes, update TypeScript types in `src/types/database.types.ts` using the `generate_typescript_types` MCP tool.

## Client Integration
1. Use the typed Supabase client from `src/lib/supabaseClient.ts`.
2. **Zero API Key Hardcoding:** Never hardcode any API keys (anon keys, publishable keys, service-role keys, or access tokens) in source code, configuration files, or documentation. All secrets must stay strictly in git-ignored `.env` or managed via secure environment variables.
3. Keep server-side AI endpoints or sensitive logic in Supabase Edge Functions or backend routes.
