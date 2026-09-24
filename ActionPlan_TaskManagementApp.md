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
