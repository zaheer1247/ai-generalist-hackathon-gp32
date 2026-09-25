# Supabase Setup & Integration Guide

This project is configured to work seamlessly with **Supabase** for database management, authentication, edge functions, and AI agent automation.

---

## 1. Project Configuration Summary

- **Project Ref:** `ivmfzbdzgzvcgzvwmolf`
- **API URL:** `https://ivmfzbdzgzvcgzvwmolf.supabase.co`
- **Publishable Key:** `sb_publishable_calLsS97UzlH2dQmWpRJDg_sO8nI7vV`
- **Status:** **Active & Connected**

---

## 2. Directory Structure & Configured Files

```text
├── .env                              # Active local environment variables (ignored by git)
├── .env.example                      # Template for team environment variables
├── .gitignore                        # Configured to protect secrets and build files
├── SUPABASE_SETUP.md                 # This guide
├── src/
│   ├── lib/
│   │   └── supabaseClient.ts         # Pre-configured, type-safe Supabase client singleton
│   └── types/
│       └── database.types.ts         # TypeScript types auto-generated from Supabase schema
└── .agents/
    └── plugins/
        └── supabase/
            ├── plugin.json           # Plugin registration
            ├── mcp_config.json       # MCP server configuration for Antigravity AI
            ├── rules/
            │   └── supabase.md       # Always-on guidelines (RLS, schema integrity)
            └── skills/
                └── supabase-ops/
                    └── SKILL.md      # Operational workflows (migrations, types, functions)
```

---

## 3. How to Use the Supabase Client

### A. Installing the Client Library
When you create your frontend or backend app (e.g. Next.js, Vite, React, or Node):
```bash
npm install @supabase/supabase-js
```

### B. Importing the Type-Safe Client
Import `supabase` directly from `src/lib/supabaseClient`:

```typescript
import { supabase } from './lib/supabaseClient';

// Example: Fetch users with full TypeScript autocomplete
async function fetchUsers() {
  const { data, error } = await supabase
    .from('users')
    .select('*');

  if (error) {
    console.error('Error fetching users:', error.message);
    return [];
  }
  return data;
}
```

---

## 4. AI-Powered Supabase Features (MCP Integration)

The Supabase MCP server is configured in `.agents/plugins/supabase/mcp_config.json`. You can ask the AI pair programmer in natural language to perform tasks directly on your Supabase project:

- **Run Database Queries:** *"Run a query to show recent entries in the users table."*
- **Create New Tables & Migrations:** *"Create the meetings, extraction_runs, and tasks tables with RLS enabled."*
- **Synchronize Types:** *"Update database.types.ts with the latest database schema."*
- **Deploy Edge Functions:** *"Deploy a Supabase edge function for AI task extraction."*
- **Inspect Security & Advisors:** *"Check for any security warnings or missing RLS policies."*

---

## 5. Security & Best Practices

1. **Keep Secrets Secret:** Never commit your `.env` or `SUPABASE_ACCESS_TOKEN` to GitHub. The `.gitignore` has been pre-configured to exclude `.env` files.
2. **Row Level Security (RLS):** Every new table created in the `public` schema must have Row Level Security enabled.
3. **Publishable vs Service Keys:** Only use the publishable/anon key on client applications. Management tokens and service role keys should remain exclusively on the server side or in Edge Functions.
