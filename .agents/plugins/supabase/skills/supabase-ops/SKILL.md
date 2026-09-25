---
name: supabase-ops
description: Operates Supabase workflows including schema inspection, executing SQL migrations, generating TypeScript types, deploying Edge Functions, and querying logs.
---

# Supabase Operations Workflow

Use this skill when performing database operations, schema modifications, edge function deployments, or diagnosing Supabase issues.

## 1. Inspecting Schemas & Tables
Before running any SQL query or adding tables, check current schema state:
- Use MCP tool `list_tables` with `schemas: ["public"]` and `verbose: true`.
- Review table names, column types, constraints, and RLS status.

## 2. Executing SQL & Applying Migrations
- Use MCP tool `execute_sql` for queries, inspection, or small updates.
- For migrations, use `apply_migration` with a descriptive migration name.
- Always include `ALTER TABLE <table_name> ENABLE ROW LEVEL SECURITY;` on new tables.
- Example SQL template:
  ```sql
  CREATE TABLE public.meetings (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    title TEXT NOT NULL,
    notes_text TEXT,
    created_at TIMESTAMPTZ DEFAULT now() NOT NULL
  );

  ALTER TABLE public.meetings ENABLE ROW LEVEL SECURITY;

  CREATE POLICY "Allow public read access"
    ON public.meetings FOR SELECT
    TO anon, authenticated
    USING (true);
  ```

## 3. Synchronizing TypeScript Types
After applying any database change:
1. Run MCP tool `generate_typescript_types`.
2. Save the output to `src/types/database.types.ts`.
3. Verify that client code referencing `Database` compiles cleanly.

## 4. Edge Functions
- To list active edge functions: `list_edge_functions`.
- To deploy an edge function: `deploy_edge_function` with the function name and files.
- To check function code: `get_edge_function`.

## 5. Diagnostics & Advisory
- Check database security and performance advisories: `get_advisors`.
- Query operational logs: `query_logs`.
