# Hackathon Project Selection — Architect's Assessment

I reviewed both files in `Hackathon/3.Product_Ideas/` and `Hackathon/4.Vibe_Coding/` (didn't touch anything outside those, per your instruction). Here's my read, framed around what actually wins a 3-day vibe-coding hackathon judged on a live demo: **feasibility inside the stack you're told to use (Bolt + Supabase + OpenAI API), a single unmistakable "wow" moment, low live-demo failure risk, and a business story judges immediately understand.**

## Scoring the 8 ideas

I scored each on 5 dimensions (1–5), equally weighted: **Build Feasibility in 3 days**, **AI Value clarity** (is the AI call doing something non-trivial or just window dressing?), **Demo/Wow factor**, **Differentiation** (how saturated is this category already), **Business viability**.

| Idea | Feasibility | AI Value | Demo Wow | Differentiation | Business | **Avg** |
|---|:-:|:-:|:-:|:-:|:-:|:-:|
| **Task Management App** | 5 | 5 | 4 | 3 | 4 | **4.2** |
| AI Interior Makeover | 3 | 5 | 5 | 3 | 3 | 3.8 |
| Campaign Planner | 4 | 4 | 3 | 2 | 4 | 3.4 |
| Resume-to-Interview Coach | 3 | 4 | 3 | 2 | 3 | 3.0 |
| Personal Finance Manager | 5 | 3 | 2 | 1 | 3 | 2.8 |
| Collaborative Notetaker | 2 | 3 | 3 | 2 | 3 | 2.6 |
| Personal Health Manager | 5 | 2 | 2 | 1 | 3 | 2.6 |
| Pet Care Companion | 4 | 2 | 2 | 2 | 2 | 2.4 |

## Recommendation: **Task Management App** (meeting notes → action items)

This is the strongest bet for winning, and it's not close. Reasoning as an architect, not just a scorer:

**1. It's the only idea where the AI call is load-bearing, not decorative.**
Health/Finance/Pet Care all bolt a "summarize this" LLM call onto a plain CRUD app — judges have seen that pattern in every cohort. The Task app's core value proposition *is* the AI: turning messy, unstructured meeting notes into structured, assignable, deadline-bound tasks. That's a textbook strong use case for an LLM (unstructured → structured extraction), and it's legible to any judge in under 10 seconds.

**2. Lowest technical risk for a live demo.**
Architecturally this is: one Supabase table (`tasks`: title, owner, due_date, status, source_note_id), one Bolt-generated board UI, and **one** OpenAI call using structured/JSON-mode output to extract `{task, owner, deadline}` triples from pasted text. No real-time sync (ruled out Collaborative Notetaker — Supabase realtime + conflict handling in 3 days is genuinely risky and multiplayer bugs mid-demo are the worst way to lose), no image-generation latency/quality variance (ruled out Interior Makeover as the safe pick, see below), no document-parsing edge cases (ruled out Resume Coach — PDF parsing across resume formats eats a day easily).

**3. The demo writes itself.**
Per the playbook's Step 12 demo script, you need one live walkthrough plus "the one wow AI/automation detail." Paste a real, messy meeting-notes paragraph on stage → click extract → watch a populated task board with owners and deadlines appear. That's a visible, instant, unambiguous "wow" — and it works with *any* input text you paste live, so there's no brittle demo-data dependency.

**4. Business story judges will nod at.**
Every team, every company, has this exact pain — it's not a niche (Pet Care) or an oversaturated commodity category (Finance/Health trackers, Campaign Planner competing conceptually with Jasper/Copy.ai). The roadmap answer to "what's next" is obvious and credible: Slack/Zoom/Calendar integration, which extends naturally without needing to be built for the demo.

### 3-day execution mapped to the playbook
- **Day 1 (Phase 1 + PRD/prompt):** Lock the single must-have flow — *paste notes → AI extracts tasks → board view*. Should-haves (max 2): manual edit of extracted tasks, status transitions (To Do/Doing/Done). Park: notifications, integrations, multi-user assignment beyond a name field.
- **Day 2 (Phase 2):** Bolt front end (board + paste-input modal) + Supabase schema, wired to the starting prompt generated per Step 7.
- **Day 3 (Phase 3):** One OpenAI structured-output call for extraction (the "wow" feature from Step 10.2), CRUD completeness pass (Step 9), stability testing loop (Step 11), then the demo script (Step 12).

## Runner-up, if your team is stronger on visual/frontend polish: **AI Interior Makeover**

It scores lower only because of image-generation risk: API latency, inconsistent output quality, and cost/rate limits are real failure modes in a live demo, and it's a *harder* build (image storage, before/after compare UI) than the Task app. But if your team can de-risk that (pre-warm the API, have a fallback screenshot ready, test the exact demo photos beforehand), it has the single highest raw "wow" ceiling of anything on the list — nothing beats a visible before/after image transformation for audience reaction. I'd only pick this over the Task app if you have someone confident wrangling an image API under time pressure.

## What I'd avoid
- **Collaborative Notetaker** — real-time multiplayer sync is the single riskiest thing to attempt in 3 days with Supabase; if it desyncs live, it's your worst possible demo moment.
- **Personal Health/Finance Manager, Pet Care Companion** — technically the safest builds, but they're the most common hackathon submissions in existence. Safe build, weak differentiation — you'll finish, but you won't stand out.

**Bottom line:** build the **Task Management App**. It's the only idea in the set where feasibility, AI value, demo impact, and business relevance all point the same direction at once.

Want this written up as a shareable one-pager (doc or artifact) for your team, or is the verdict here enough?