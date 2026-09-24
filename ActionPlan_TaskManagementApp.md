# 48-Hour Hackathon Action Plan: AI Task Management App

**Goal:** Build a functional MVP of an AI-powered Task Management App (converting meeting notes to actionable tasks) in under 48 hours.
**Team Size:** 6-10 members.
**Stack:** Bolt (Frontend), Supabase (Backend), OpenAI API (AI Extraction).

## 🏆 Evaluation Criteria Focus
1. **Understanding the Problem:** Clearly define the user (e.g., project managers, busy professionals) and the pain point (manual, tedious extraction of action items from meetings).
2. **Functionality:** Ensure the core flow works end-to-end (paste notes -> AI extracts tasks -> tasks populate a board -> tasks can be moved/updated).
3. **Creativity:** Make the AI extraction feel magical and intuitive, avoiding generic to-do list templates.
4. **Presentation:** Polish the UI, ensure a smooth user experience, and prepare a compelling 3-minute video walkthrough (storytelling is key).

---

## 👥 Team Roles & Delegation
With 6-10 people, parallel work is essential. Divide into sub-teams:

1. **Product & Presentation (2 members):** 
   - Define PRD, manage scope (MoSCoW), oversee the demo script, create the pitch deck, and record the Loom video.
2. **Design & Vibe (1-2 members):** 
   - Define UI/UX, styling, color palette, and ensure the app looks premium and creative. Give instructions to the Bolt builders.
3. **Frontend / Bolt Builders (2-3 members):** 
   - Use Bolt.new to generate the UI, integrate design choices, and build the task board (Kanban style).
4. **Backend & AI Integrators (2-3 members):** 
   - Set up Supabase (DB schema, auth if needed), write the OpenAI API prompts for extracting tasks, and connect the backend to the Bolt frontend.

---

## 📅 Timeline & Milestones

### Phase 1: Ideation & Foundation (Hours 1 - 8)
*Objective: Lock in the idea, scope, and initial architecture.*

- **Hour 1-2: Kickoff & Scoping**
  - Define the target user and the core problem (Complete Steps 1 & 2 of the Playbook).
  - Review competitors and list features.
  - **MoSCoW Prioritization:** Lock in the *Must-Have* flow: User pastes meeting notes -> AI extracts tasks (Owner, Deadline, Title) -> Tasks appear on a Kanban board -> User can edit/move tasks.
- **Hour 3-4: Architecture & PRD**
  - Product team writes the PRD.
  - Backend team designs the Supabase DB schema (Tables: `Users`, `Meetings/Notes`, `Tasks`).
  - Design team creates low-fi wireframes and selects a color theme.
- **Hour 5-6: Prompt Engineering for Bolt & AI**
  - Product team drafts the single starting prompt for Bolt based on the PRD.
  - Backend team starts testing OpenAI prompts for extracting tasks from sample meeting transcripts.
- **Hour 7-8: Initial Build & Setup**
  - Frontend team feeds the starting prompt into Bolt.
  - Backend team initializes the Supabase project and gets API keys.
  - Setup GitHub repo for collaboration if needed.

### Phase 2: Core Building (Hours 9 - 24)
*Objective: Get the must-have flow working end-to-end.*

- **Hour 9-14: Frontend & Backend Development (Parallel)**
  - **Frontend:** Iterate on Bolt to refine the UI. Ensure the task board is interactive (drag and drop if possible, or simple status dropdowns).
  - **Backend:** Create Supabase tables. Build a serverless function (Edge Function or local API) to handle the OpenAI call and save extracted tasks to the DB.
- **Hour 15-18: Integration**
  - Connect the Bolt frontend to Supabase.
  - Hook up the "Generate Tasks" button to send text to the backend, call OpenAI, and return the tasks to the UI.
- **Hour 19-22: CRUD Operations**
  - Ensure users can manually Create, Read, Update, and Delete tasks on the board.
- **Hour 23-24: Mid-Hackathon Review**
  - Team regroups. Does the *Must-Have* flow work? 
  - Stop adding new features if the core flow is broken. Fix bugs.

### Phase 3: Polish, Automations, & Presentation (Hours 25 - 48)
*Objective: Make it look amazing and prepare the submission.*

- **Hour 25-32: UI Polish & "Wow" Factor**
  - Apply the Design team's styling to make the app look premium (crucial for the "Presentation" criteria).
  - Add micro-animations or loading states for the AI generation to make it feel magical.
- **Hour 33-38: Testing & Bug Fixing**
  - Run scenario tests (Step 11 of Playbook).
  - Product team tries to break the app. Developers fix the bugs.
- **Hour 39-42: Demo Script & Pitch Deck**
  - Product team finalizes the pitch deck using the provided template.
  - Write the 3-minute demo script focusing on the user's pain and the magic of the AI extraction.
- **Hour 43-46: Recording & Final Touches**
  - Record the 2-3 minute Loom walkthrough video. Make sure to follow the script and highlight the AI feature clearly.
- **Hour 47-48: Submission**
  - Gather the live link, Loom video, Pitch Deck, and team details.
  - Submit via the Project Submission Portal before the deadline.

---

## 💡 Pro-Tips for Success
- **Keep it Simple:** Don't get distracted by complex auth, email notifications, or advanced settings. Focus 100% on the core "Notes to Tasks" flow.
- **Fake it if necessary:** If drag-and-drop on the Kanban board is too hard in Bolt, use simple dropdowns for status (To Do, In Progress, Done). The AI extraction is the star of the show.
- **Commit frequently:** If using GitHub, make sure the "Code Owner" commits stable versions so you don't lose progress.
- **Vibe check:** Regularly ask: "Does this look and feel good?" The evaluation criteria heavily weights aesthetics and presentation.

---

# Architect Decision Record and Execution Kit

## 1. Principal-architect decision

**Build `CommitFlow` — an AI meeting-to-accountability workspace.**

Do **not** position it as a task-management app or an Asana clone. The product promise is:

> Turn a messy meeting into *reviewable, owned commitments* in under two minutes.

This is the right 48-hour decision because the chosen idea already has a single, visible before/after flow: unstructured notes become editable tasks with owners and due dates, then become trackable execution. AI is load-bearing, but the user remains the authority. That combination is both credible for an enterprise audience and materially safer than silently creating commitments from model output.

### Target user and problem statement

- **Primary user:** a delivery lead, engineering manager, or project coordinator running a cross-functional weekly meeting.
- **Context:** immediately after a meeting, when notes are scattered and accountability is still ambiguous.
- **Pain:** converting notes into reliable work is manual; owners and dates are easy to miss; normal task boards start *after* the hard extraction work.
- **Final problem statement:** Cross-functional teams lose commitments after meetings because action items, owners, and deadlines are buried in unstructured notes, while existing task boards require manual re-entry and do not show what the AI inferred.
- **Hackathon success metric:** from one supplied meeting note, a user reviews and publishes at least five tasks with zero dead ends, then updates one task to Done.

### The differentiator: reviewable extraction

Every AI-proposed action must show:

1. Task title and concise context.
2. Proposed owner and deadline, or an explicit `Needs review` state when absent/ambiguous.
3. A short source quote from the pasted note.
4. An editable form and a **Publish approved tasks** action.

This is the creative feature that prevents the app from looking like a template. It gives judges a clear trust story: *“The AI proposes; the team confirms; CommitFlow preserves the evidence.”*

## 2. Scope contract: protect the 48-hour outcome

| Priority | Ship it | Reason |
|---|---|---|
| Must | Paste meeting notes; extract structured task proposals; review/edit/reject proposals; publish approved tasks; task board with To do/In progress/Done; task edit and delete | This is the only complete value loop and directly proves functionality. |
| Must | Source quote + `Needs review` badge for ambiguous owner/date | This is the differentiator and makes AI output trustworthy. |
| Should | Filter by owner/status and overdue visual treatment | Improves the closing board view if the core loop is stable. |
| Should | Seed/demo meeting note button | Removes live-demo risk and makes judging reproducible. |
| Could | AI follow-up summary | Add only after the full scenario passes twice. |
| Won't in 48 hours | Authentication complexity, realtime collaboration, file/PDF upload, email/Slack/calendar integration, notifications, analytics, role management, drag-and-drop if unreliable | Each adds failure modes without improving the judged core flow. |

**Scope gate:** no Could/Should work begins until the Must flow is proven against the demo note twice. Use a status selector instead of fragile drag-and-drop if necessary.

## 3. Rubric-to-evidence plan

| Evaluation criterion (from supplied image) | What judges must see | Evidence to deliberately create |
|---|---|---|
| Understanding of the problem | A specific user, painful moment, and why a normal board is insufficient | First demo slide: messy post-meeting notes and the one-sentence problem statement. |
| How functional the app is | A real flow works end-to-end, including correction and persistence | Paste note → extract → edit one wrong proposal → publish → change status → reload and show persistence. |
| Creativity | A fresh interaction, not a generic template | Evidence quote, confidence/needs-review treatment, and explicit human approval before a commitment is created. |
| Presentation | Polished UI and a coherent walkthrough narrative | One visual system, realistic seeded team/project data, intentional empty/loading/error states, 2–3 minute rehearsed Loom. |

## 4. Thin, reliable architecture

```text
Browser (Bolt React UI)
  ├─ Meeting input / review queue / task board
  └─ Supabase client: reads and writes approved records
          │
          ├─ Supabase Postgres: meetings, extraction_runs, task_proposals, tasks
          └─ Server-side AI endpoint / Supabase Edge Function
                    └─ OpenAI structured extraction
```

### Design rules

- Keep the OpenAI API key only in the server-side function/secret store—never in the browser or repository.
- Treat all generated fields as untrusted suggestions until the user publishes them.
- Use anonymised synthetic meeting notes for the demo; do not paste customer, employer, or personal meeting data into an AI service.
- Prefer one deployed app, one database, and one AI request. A fallback seeded extraction is acceptable for continuity, but label it as demo data; do not pretend a failed live AI call succeeded.

### Minimal data model

| Entity | Essential fields |
|---|---|
| `meetings` | `id`, `title`, `notes_text`, `created_at` |
| `extraction_runs` | `id`, `meeting_id`, `status`, `model_name`, `created_at`, `error_message` |
| `task_proposals` | `id`, `run_id`, `title`, `owner_name`, `due_date`, `source_quote`, `confidence`, `review_state` (`pending`, `approved`, `rejected`) |
| `tasks` | `id`, `meeting_id`, `proposal_id` (nullable for manual tasks), `title`, `owner_name`, `due_date`, `status`, `source_quote`, `created_at`, `updated_at` |

**Screens only:** (1) Meeting intake, (2) Review queue, (3) Task board, and (4) task edit drawer/modal. Avoid a separate dashboard unless it is just the board.

## 5. Build order and 48-hour control points

| Timebox | Deliverable / owner | Exit test — do not move on until true |
|---|---|---|
| 0–2 hours | Product decision, demo note, success metric, visual direction | Team agrees on this document and parks the Won't list. |
| 2–5 hours | Supabase schema + seeded data + deployment path | A manually inserted task appears in the UI and survives reload. |
| 5–9 hours | Bolt screens and navigation | Intake, review, board, and edit paths are clickable; no dead primary controls. |
| 9–14 hours | AI endpoint and structured extraction | Demo note produces valid proposal JSON; bad/empty input shows a useful error. |
| 14–18 hours | Review-to-publish transaction | Edit/reject/approve works; only approved proposals become tasks. |
| 18–22 hours | Board CRUD and persistence | Create, read, update status, edit, delete, and reload all work. **MVP freeze.** |
| 22–30 hours | Design polish, filters, loading/error states | Full must-have scenario succeeds twice in a row. |
| 30–36 hours | Test pass, fallback prep, accessibility/readability pass | Five test notes are checked; demo data and a short recovery path are ready. |
| 36–42 hours | Pitch deck + recording rehearsal | One presenter can demonstrate the value in 2–3 minutes without narration gaps. |
| 42–46 hours | Record Loom; final regression | Recorded path matches the working deployment. |
| 46–48 hours | Submission package and portal submission | Live URL, Loom URL, pitch deck, team details, and final form are checked. |

If you have fewer than four people, work in this order rather than attempting parallelism: database/persistence → UI shell → extraction → review/publish → polish → demo. A working narrow app beats a broad unfinished one.

## 6. What to do next — first 90 minutes

1. Name the product **CommitFlow** (or retain a team-approved name) and copy the target user, problem statement, success metric, and Won't list above into the team channel.
2. Select a Code Owner and a Demo Owner. The Code Owner alone merges stable changes; the Demo Owner owns the seeded note, deck, script, and recording checklist.
3. Create one realistic, sanitised demo note with six actions: two explicit owner/date pairs, one missing date, one ambiguous owner, one completed follow-up, and one non-action statement. This lets the review interface demonstrate judgment rather than blind automation.
4. Create the Supabase project, add the four tables above, and insert one meeting plus two sample tasks. Verify database-backed persistence before connecting AI.
5. Create the Bolt project using the starting prompt below. Build the four screens with static seeded data first.
6. Implement the extraction endpoint and validate its response against the JSON contract below using the demo note. Only then connect the **Extract actions** button.
7. At hour 18, run the acceptance test. If it fails, stop feature work and repair the narrow flow.

## 7. Copy-paste starter prompt for Bolt

> Build a polished responsive web app named **CommitFlow**, an AI meeting-to-accountability workspace for delivery leads. It is not a generic task manager. Its core promise is: turn messy meeting notes into *reviewable, owned commitments*.
>
> Use a calm, premium B2B visual style: dark navy/slate base, a restrained lime or teal accent for approved actions, strong whitespace, clear hierarchy, accessible contrast, and compact cards. Use realistic seeded demo data. Add purposeful loading, empty, and error states; do not add decorative charts.
>
> Build four connected screens:
> 1. **Meeting intake:** title field, large pasted-notes textarea, a `Use demo meeting` button, and primary `Extract action items` button. Include a clear privacy note that users should not add sensitive meeting data.
> 2. **Review queue:** show AI-proposed task cards. Each card includes task title, proposed owner, due date, source quote, confidence or `Needs review` badge, and editable controls. Support Approve and Reject. Do not publish tasks automatically.
> 3. **Task board:** columns To do, In progress, Done. Show task title, owner, due date, and a compact source-evidence icon/link. Use status controls; drag and drop is optional and must not be required.
> 4. **Task edit drawer/modal:** edit title, owner, date, status; delete with confirmation.
>
> Data model: meetings(id, title, notes_text, created_at); extraction_runs(id, meeting_id, status, model_name, created_at, error_message); task_proposals(id, run_id, title, owner_name, due_date, source_quote, confidence, review_state); tasks(id, meeting_id, proposal_id, title, owner_name, due_date, status, source_quote, created_at, updated_at). Persist through Supabase. Keep OpenAI calls server-side; no API key in client code. The AI response is always a proposal and only approved proposals create tasks. Make all CRUD operations work and preserve state on reload.
>
> Primary demo journey: paste a meeting note → extract six proposals → edit one ambiguous proposal → approve selected proposals → publish them → see the board → move one item to Done → reload and show persisted state.

## 8. AI contract and test guardrails

The extraction endpoint should request JSON only. A usable response contract is:

```json
{
  "tasks": [
    {
      "title": "Prepare deployment checklist",
      "owner_name": "Aisha",
      "due_date": "2026-09-30",
      "source_quote": "Aisha will prepare the deployment checklist by Tuesday.",
      "confidence": 0.92,
      "needs_review": false
    }
  ]
}
```

Prompt rules: extract only explicit commitments; never invent a person or date; return `null` and set `needs_review: true` when an owner or deadline is unclear; quote the smallest supporting source span; return an empty list when there are no actions. Validate this schema server-side before persisting proposals.

### Acceptance test (run before recording)

| Scenario | Expected result |
|---|---|
| Valid demo notes | Six proposals display with source quotes; uncertain fields visibly require review. |
| Edit one AI error | Edited owner/date persists into the published task. |
| Reject a proposal | Rejected proposal never appears on board. |
| Publish approved proposals | Tasks appear in To do and survive refresh. |
| Update and delete | Status changes persist; delete removes only the selected task. |
| Empty notes / AI failure | User sees a clear retry/manual-entry path; app does not show invented tasks. |

## 9. Demo narrative (2–3 minutes)

1. **Problem, 15 seconds:** “After a delivery meeting, commitments disappear into notes. Re-entering them is slow, and AI summaries do not make anyone accountable.”
2. **Before, 15 seconds:** show the deliberately messy note and identify one ambiguous commitment.
3. **Magic with control, 45 seconds:** extract actions; point to the source quote and `Needs review` badge; correct one proposed owner/date.
4. **Outcome, 45 seconds:** publish approved tasks; show owners, deadlines, and the board; move one task to Done and reload to prove persistence.
5. **Why it matters, 20 seconds:** “CommitFlow does not just summarise meetings. It makes confirmed commitments operational, with evidence.”
6. **Next step, 10 seconds:** integrations and team permissions come later—only after the trusted review loop is proven.

## 10. Operational checklist

- [ ] Repository has a README with local/deploy instructions and no secrets committed.
- [ ] Environment variables are configured in the deployment platform, not hard-coded.
- [ ] One stable, deployed URL is opened in an incognito/private session before recording.
- [ ] Demo data is seeded and resettable; an API-error recovery path is rehearsed.
- [ ] Full journey passes twice on the deployed version.
- [ ] Pitch deck uses the provided template and supports the same story as the Loom.
- [ ] Submission contains the live URL, 2–3 minute Loom, pitch deck, and team details, through the required portal.

## Source basis

- `EvaluationCriteria.png`: problem understanding, end-to-end functionality, creativity, and presentation.
- `4.Vibe_Coding/Product Building - Playbook.md`: one strong end-to-end flow, MoSCoW, architecture/PRD/prompt sequence, CRUD/testing/demo requirements, and submission artefacts.
- `3.Product_Ideas/Product Ideas for Accelerator.md`: Task Management App = meeting notes → editable action items with owners/deadlines → task board, using Bolt, Supabase, and OpenAI.
