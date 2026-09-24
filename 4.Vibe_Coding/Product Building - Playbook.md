# Hackathon Workbook

# **Vibe Coding Hackathon Workbook**

**Objective:** Build a working MVP in 3 days using vibe coding tools

## **How to use this**

* Pick **one** product idea from the list [here](https://docs.google.com/document/d/1Q5gQ-NobVeHAqSG8OJV9LSFlkcRqJw-ph6lvFny9bT0/preview?tab=t.0#heading=h.kxomnbbk9rwv) and stick to it.  
* Follow **Phase 1 → Phase 2 → Phase 3** in order.  
* Use any stack: AI Studio / Bolt / Lovable / Replit / Emergent / etc.  
* Focus on **one strong end-to-end flow**, not 20 scattered features.

---

## **PHASE 1 \- IDEATION** 

From vague idea to sharp MVP scope

### **Step 1 \- Product and user basics**

**1.1 Product one-liner**

* Product name (working):  
   `__________________________`

* One-liner (For X, I am building Y so they can Z):

   `For ____________________, I am building ____________________ so they can ____________________.`

**1.2 Who is this for**

* Primary user role:  
   `__________________________`

* Where they use this (context):  
   `__________________________`

* Top 3 pains today:

  1. `__________________________`

  2. `__________________________`

  3. `__________________________`

**1.3 MVP success for this hackathon**

By the end of 3 days:

* A user should be able to:  
   `_________________________________________________________`

* Simple success metric for the demo (one line):  
   `_________________________________________________________`

---

### **Step 2 \- Deepen the problem with 5 Whys**

**2.1 Problem statement v0**

> Problem v0:  
>  `_________________________________________________________`

**2.2 5 Whys table**

| Why \# | Question | Your answer |
| ----- | ----- | ----- |
| 1 | Why is this a problem for your user? |  |
| 2 | Why does that happen right now? |  |
| 3 | Why haven’t existing tools solved this well? |  |
| 4 | Why is your user still stuck? |  |
| 5 | Why does solving this now matter for them? |  |

**2.3 Final problem statement**

> Final problem statement:  
>  `_________________________________________________________`

This is the line you reuse in prompts, PRD, and demo.

---

### **Step 3 \- Competitor scan and AI feature analysis**

Screenshots → AI analysis → features list.

**3.1 Collect references**

Pick **2–3 products** closest to what you want to build.

* Take screenshots of key pages:

  * Pricing pages

  * Feature pages

  * Sample UI / dashboards

| Product / tool | Links or pages you checked | What they do well  (2 points) | What frustrates users  (2 points) |
| ----- | ----- | ----- | ----- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

**3.2 AI feature extraction**

Paste screenshots or text into your LLM:

> “I am building a product similar to these tools: \[brief description of each\].  
>  Here are screenshots / notes from their feature and pricing pages.  
>  Extract all unique features into a table with columns:  
>  **Feature | What it does | Why users care | Which tool(s) have it**.  
>  Highlight any patterns and common ‘must have’ features.”

* Where you saved that table (doc / link / file):  
   `_________________________________________________________`

Optional: Mark potential differentiators now with a ⭐ in that table.

---

### **Step 4 \- MVP scope with MoSCoW (core vs differentiators)**

**4.1 Feature dump**

List everything from your head \+ AI feature table:

* `________________________________`

* `________________________________`

* `________________________________`

* `________________________________`

**4.2 MoSCoW prioritisation**

Use this table and mark differentiators with a ⭐ in the name if needed.

| Feature | M (Must) | S (Should) | C (Could) | W (Won't now) | Differentiator? (⭐ / \-) | Why you placed it here |
| ----- | :---: | :---: | :---: | :---: | ----- | ----- |
|  | ☐ | ☐ | ☐ | ☐ |  |  |
|  | ☐ | ☐ | ☐ | ☐ |  |  |
|  | ☐ | ☐ | ☐ | ☐ |  |  |

Guidance:

* **Must:** Without it, product fails its main promise.

* **Should:** Strongly expected, but can live without for v1.

* **Could:** Candy. Only if time remains.

* **Won’t:** Explicitly not in this 3-day build.

**4.3 Final MVP scope for the hackathon**

* Single **Must-have flow** you commit to ship:  
   `_________________________________________________________`

* Up to **2 Should-haves**:

  * `_____________________________`

  * `_____________________________`

* Features you **park deliberately** (for later):

  * `_____________________________`

  * `_____________________________`

---

### **PHASE 1 \- END CHECKLIST**

* Final problem statement is clear

* Primary user and context defined

* Competitor screenshots \+ feature table done

* Features prioritised with MoSCoW

* One must-have flow \+ up to 2 should-haves locked

---

## **PHASE 2 \- BUILDING**

Architecture, PRD, starting prompt, and first build

### **Step 5 \- Architecture: screens, flows, data, backend**

**5.1 Big picture architecture**

* Front-end (what the user sees and clicks):  
   `Screens: ______________________________________________`

* Back-end / automations (what runs behind the scenes):  
   `Workflows / services: _________________________________`

* Data store (where data lives):  
   `Sheets / DB / built-in storage: _______________________`

* External APIs / services (if any):  
   `Email / AI models / webhooks / others: ________________`

**5.2 Screens & actions table**

| Screen name | Who uses it | Key actions (buttons / flows) | Data needed / shown |
| ----- | ----- | ----- | ----- |
| e.g. Task Dashboard | Logged-in user | Create task, update status, mark done | Task title, due date, status, assignee |
|  |  |  |  |
|  |  |  |  |

---

### **Step 6 \- PRD with AI**

Ask Claude to create a proper PRD.

**6.1 PRD prompt**

Use this in your LLM:

> “You are a senior product manager.  
>  I want to build an MVP in a no-code / vibe coding tool.

> Problem statement:  
>  \[Paste from Step 2.3\]

> Target user and top 3 pains:  
>  \[Paste from Step 1.2\].

> Prioritised features using MoSCoW (mark differentiators with ⭐):  
>  \[Paste your table\].

> Architecture draft:

> * Front-end screens: \[list\]

> * Back-end workflows / automations: \[list\]

> * Data store: \[sheet / DB \+ important fields\]

> * External services / APIs: \[list\]

> Tasks:

> 1. Write a concise PRD with: Goal, Users, Scope (Must \+ chosen Shoulds), Out of Scope, Core user flows, Data model (main tables and fields), Non-functional constraints.

> 2. Write a step-by-step build plan for a vibe coding tool.”

**6.2 Capture your PRD**

* PRD location (doc / link / notes):  
   `_________________________________________________________`

* Two key flows to build first:

  1. `_____________________________`

  2. `_____________________________`

---

### **Step 7 \- Platform optimisation: convert PRD into a starting prompt**

Bolt.new best practices → single starting prompt

https://support.bolt.new/building/build-your-first-app.

**7.1 Collect platform guidelines**

* Chosen tool (Bolt / Lovable / Replit / etc.):  
   `_____________________________`

* Link or notes from its “best practices” / docs:  
   `_________________________________________________________`

**7.2 Starting prompt generator**

Use your LLM again:

> “Here is my PRD:  
>  \[Paste PRD\]

> Here are best practices / docs for \[tool name\]:  
>  \[Paste key points or link \+ summary\].

> Rewrite this PRD as **one single starting prompt** optimised for \[tool name\].

> * Use the tool’s recommended format.

> * Include entities, screens, data model, and must-have flow.

> * Keep it copy-paste ready for the builder.”

**7.3 Final starting prompt**

* Paste your tool-specific starting prompt here or link it:

   `_________________________________________________________`

---

### **Step 8 \- Day 1 & Day 2 build execution**

**Day 1 \- Outcome**

* Complete **Phase 1**

* Complete **Steps 5, 6, 7**

* Have a PRD \+ starting prompt ready

Day 1 checklist:

* Ideation done and frozen

* Architecture sketched

* PRD written

* Tool-specific starting prompt ready

**Day 2 \- Build the first version**

In your chosen tool:

1. Create a new project.

2. Paste the starting prompt and generate the first version.

3. Set up core data model (tables / collections / sheets).

4. Ensure the **must-have flow** is present.

5. If parts are missing, use **targeted prompts** to:

   * Add missing screens

   * Fix obvious UI gaps

   * Align flows with PRD

Day 2 checklist:

* Project created in tool

* First build generated from starting prompt

* Data model exists

* Must-have flow runs at least once end-to-end (even if rough)

---

### **OPTIONAL SECTION \- GITHUB FOR BACKUP & COLLAB**

(Use only if your team wants shared code)

**Goal:**  
Keep your code in one place and let everyone update it.

This is a **simple path**: one main branch, small commits, no complex Git.

**Step G1 \- One repo per team**

1. One teammate goes to github.com → **New repository**.

2. Name it: `aiap-<cohort>-<team-name>` or similar.

3. Visibility: **Private** is fine.

4. Click **Create repository**.

**Step G2 \- Add collaborators**

1. In the repo, go to **Settings → Collaborators**.

2. Add your teammates by GitHub username or email.

3. Give them **Write** access.

Now everyone can open the same repo.

**Step G3 \- Simple “back code and collaborate” workflow**

Use this pattern during the hackathon:

* One person is **Code Owner** for the repo.

* Others send code snippets or files to Code Owner (from Bolt / editor export).

* Code Owner:

  1. Pulls latest code from GitHub (if using Git) or edits in web UI.

  2. Pastes / uploads updated files.

  3. Clicks **Commit** with a clear message:

     * “Add itinerary screen”

     * “Fix activity edit flow”

Repeat this whenever a feature is stable.

**Team rules (keep it simple):**

* Only commit **working** code.  
* One person commits at a time.  
* If something breaks, Code Owner reverts last change or fixes and commits again.  
* Github Guide for additional information : [GitHub Guide 101](https://docs.google.com/document/d/1t_K2KtvTRHGBxWBADKji3iu_PzObm9Iv85szdii2HT0/edit?tab=t.0#heading=h.ehfa52b0g2sl)

---

### **PHASE 2 \- END CHECKLIST**

* Architecture clear and documented  
* PRD complete  
* Tool-optimised starting prompt created  
* First build live with must-have flow in place  
* Backup on github

---

## **PHASE 3 \- BACKEND, AUTOMATIONS, ITERATION & DEMO**

Database implementation, CRUD, testing, and enhancement.

### **Step 9 \- Database and CRUD**

**9.1 Data design**

* Primary entities (e.g. Tasks, Projects, Users):

  * `__________________________`

  * `__________________________`

For each, define:

* Table / collection name: `__________________________`

* Fields:  
   `_________________________________________________________`

**9.2 CRUD checklist**

For each core entity, check if you support:

| Entity | Create | Read / list | Update | Delete | Notes / gaps |
| ----- | ----- | ----- | ----- | ----- | ----- |
|  | ☐ | ☐ | ☐ | ☐ |  |
|  | ☐ | ☐ | ☐ | ☐ |  |

If any box is unchecked:

* Write a prompt to your tool / LLM:

   “Enable full CRUD for \[entity\] in my app.  
   Add screens / actions for \[missing operations\].  
   Keep UX consistent with existing screens.”

---

### **Step 10 \- Automations and AI enhancements**

This covers things like AI Task Breakdown, notifications, etc.

**10.1 Backend & automations table**

| Trigger (event) | Tool / service | What should happen |
| ----- | ----- | ----- |
| User signs up / first login | e.g. n8n / built-in | Create user record, send welcome email, log to sheet |
| User creates a main item |  | Save item, optionally run AI Task Breakdown |
| User completes a workflow |  | Send summary email / notification / log to history |

Fill this for your product:

| Trigger (event) | Tool / service | What should happen |
| ----- | ----- | ----- |
|  |  |  |
|  |  |  |
|  |  |  |

**10.2 Optional “wow” AI feature**

Pick **one** small enhancement (example: AI Task Breakdown):

* Feature name:  
   `_________________________________________________________`

* What it does in one line:  
   `_________________________________________________________`

* Prompt or config notes for it:  
   `_________________________________________________________`

---

### **Step 11 \- Testing and iteration loop**

test → see missing edit/delete → prompt → fix → retest.

**11.1 Scenario test script**

Define **one realistic scenario**:

> “User type \[X\] wants to \[goal\].  
>  They will go through: \[screen 1\] → \[screen 2\] → \[screen 3\] → done.”

Describe it:

`_________________________________________________________`

**11.2 Bug and gap log**

While testing, log issues:

| \# | What broke / missing (issue) | Where (screen / flow) | Prompt you used to fix it | Fixed? (Y/N) |
| ----- | ----- | ----- | ----- | ----- |
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |

Cycle:

1. Run the scenario end-to-end.  
2. Write down each issue.  
3. Use targeted prompts to the builder to fix.  
4. Retest.

**11.3 Stability checklist**

* Must-have flow works start to finish at least twice in a row  
* No obvious dead buttons or dead-end screens  
* CRUD works for main entities  
* Key automation(s) fire as expected

---

### **Step 12 \- Demo and reflection**

**12.1 Demo script (3–5 mins)**

Fill this and use it as your narration:

1. **User and problem:**  
    “Our product is for \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ who struggle with \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_.”

2. **What you built:**  
    “In 3 days, we built \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ so they can \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_.”

3. **Live walkthrough:**

   * Start from entry point.

   * Run the **must-have flow** end-to-end.

   * Show the **one wow AI/automation detail**.

4. **Close:**

   * “Next, we plan to \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_.”

**Demo checklist**

* Clear entry path (login or shared URL)  
* Must-have flow runs live without hidden setup  
* Wow feature works on demo data

**12.2 Reflection after the hackathon**

* What users / judges liked most:  
   `_________________________________________________________`

* One product / design choice that worked well:  
   `_________________________________________________________`

* Top 3 issues you noticed:

  * `__________________________`

  * `__________________________`

  * `__________________________`

* Next 7-day plan:

  * Improve stability and UX

  * Add 1–2 parked features

  * Test with 3–5 real users

  * Clean PRD and architecture for v2

## **Resources** 

* Pitch Deck Template: [AIAP : Pitch Deck Template](https://docs.google.com/presentation/d/12lrt7l83ZLkKuFas_X0uUOiI6rCpQPtyHdVkdw_6vjQ/edit?slide=id.g36ed19b842a_0_0#slide=id.g36ed19b842a_0_0)  
* Product Ideas: [Product Ideas for Accelerator](https://docs.google.com/document/d/1Q5gQ-NobVeHAqSG8OJV9LSFlkcRqJw-ph6lvFny9bT0/preview?tab=t.0#heading=h.kxomnbbk9rwv)  
* Loom for recording: [https://www.loom.com/](https://www.loom.com/)

**How to Submit Your Project**

### **Step 1: Open the Project Submission Portal**

Visit the portal below:

[AI Accelerator Hackathon Portal](https://hackathon-group-allocator.onrender.com/dashboard)

### **Step 2: Navigate to the Submission Page**

* Log in to the portal  
* Click on the **"Submit Project"** tab at the top of the page  
* Review the submission requirements listed on the page

### **Step 3: Keep These Ready Before Submitting**

Make sure you have the following:

✅ Live product link  
 ✅ 2–3 minute Loom walkthrough video  
 ✅ Pitch deck (using the provided template)  
 ✅ Team details

### **Step 4: Submit Your Project**

* Click on **"Open Submission Form"**  
* Fill in all the required details  
* Submit the form 

![][image1]

---

### **Important**

⚠️ Project submissions will be accepted **only through the Project Submission Portal**.

⚠️ Submissions shared in WhatsApp groups, emails, or any other channel will **not be considered valid**.

⚠️ Ensure all details are entered correctly before submitting, as the submitted information will be used for evaluation.

# Example

# **Sample Filled Workbook**

Example Idea: **Travel Itinerary Planner**

---

## **PHASE 1 \- IDEATION (Example)**

### **Step 1 \- Product and user basics**

**1.1 Product one-liner**

* Product name:  
   **TripThreads**

* One-liner:  
   **For busy young professionals, TripThreads is a simple travel planner so they can organize day-wise itineraries in one place without messy spreadsheets and notes.**

**1.2 Who is this for**

* Primary user role:  
   **25-35 year old working professional who travels 1-3 times a year.**

* Context:  
   **Plans short trips (3-7 days) with friends or partner, usually on weekends or holidays, using multiple apps and random links.**

* Top 3 pains today:

  1. Plans scattered across WhatsApp, screenshots, Notes, Maps.

  2. Hard to see a clear day-wise plan and time clashes.

  3. Last minute confusion on bookings, timings, and what is confirmed.

**1.3 MVP success for this hackathon**

By the end of 3 days:

* A user should be able to:  
   **Create a trip, add day-wise activities with time and location, and view the full itinerary in one simple timeline.**

* Simple success metric:  
   **User completes one 3-day trip plan with at least 3 activities per day, without getting stuck.**

---

### **Step 2 \- Deepen the problem with 5 Whys**

**2.1 Problem statement v0**

> People planning trips struggle to keep their itinerary organized.

**2.2 5 Whys table (filled)**

| Why \# | Question | Answer |
| ----- | ----- | ----- |
| 1 | Why is this a problem for your user? | They feel stressed and confused before and during the trip. |
| 2 | Why does that happen right now? | Information is split across chats, screenshots, booking emails, and random notes. |
| 3 | Why haven’t existing tools solved this well? | Most tools are either too complex or focused on bookings, not on simple day-wise plans. |
| 4 | Why is your user still stuck? | Setting up existing trip planners feels heavy, so they fall back to WhatsApp and Notes. |
| 5 | Why does solving this now matter for them? | They want stress-free trips and to feel in control without spending hours planning. |

**2.3 Final problem statement**

> Busy young professionals feel stressed before trips because their plans are scattered across multiple apps, and existing tools are too heavy for quick, simple day-wise itineraries.

---

### **Step 3 \- Competitor scan and AI feature analysis**

**3.1 Reference products**

| Product / tool | Links / pages checked | What they do well | What frustrates users |
| ----- | ----- | ----- | ----- |
| Google Travel | Search \+ “Trips” itinerary pages | Auto imports bookings, shows map and day split | Not easy to manually plan custom day blocks |
| TripIt | Itinerary from email confirmations | Auto-parses emails, central trip timeline | Focused on bookings, less on custom activities |
| Notion templates | Free trip planning templates | Flexible, can add anything | Too manual, takes effort to set up and maintain |

**3.2 AI feature extraction (summary)**

Example AI feature table output (compressed):

| Feature | What it does | Why users care | Tools |
| ----- | ----- | ----- | ----- |
| Trip overview | Shows trip dates and destination | Quick snapshot of the whole trip | All |
| Day-wise schedule | Activities listed per day | Helps avoid clashes and confusion | All |
| Booking details | Stores flights, hotels, references | One place to check confirmations | All |
| Map view | Activities on a map | Understand distance between plans | Some |
| Email import | Reads booking emails | Saves manual typing | TripIt |

Key pattern:

* Every tool has **trip overview** and **day-wise schedule**.

* Differentiators: email import, deep map integration.

* For MVP, focus on **clean day-wise planning**, not automation.

---

### **Step 4 \- MVP scope with MoSCoW**

**4.1 Feature dump**

Raw ideas:

* Create trip with title, location, dates.

* Add days automatically between start and end dates.

* Add activities with time, title, notes, and basic location text.

* Simple day-wise list view.

* Edit and delete activities.

* Mark activities as “must do” or “optional”.

* Basic AI: suggest 3 activities per day based on city and theme.

* Share read-only link of itinerary.

* Export to PDF.

* Map view with pins.

* Attach booking references (PNR, hotel confirmation).

**4.2 MoSCoW table (filled)**

| Feature | M | S | C | W | Differentiator? | Why here |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| Create trip (title, destination, dates) | ☑ | ☐ | ☐ | ☐ | \- | Without trip object, nothing else makes sense. |
| Auto-generate days between start/end dates | ☑ | ☐ | ☐ | ☐ | \- | Core to “itinerary” experience. |
| Add activities (time, title, notes) | ☑ | ☐ | ☐ | ☐ | \- | Heart of the planner. |
| View schedule day-wise | ☑ | ☐ | ☐ | ☐ | \- | Users need a clear daily plan. |
| Edit/delete activities | ☑ | ☐ | ☐ | ☐ | \- | Basic CRUD, otherwise app frustrates users. |
| Mark activities as must-do / optional | ☐ | ☑ | ☐ | ☐ | \- | Nice clarity, but not core. |
| AI suggestion: 3 activities per day | ☐ | ☑ | ☐ | ☐ | ⭐ | Differentiator, but secondary to base planner. |
| Share read-only link | ☐ | ☑ | ☐ | ☐ | \- | People travel with others, sharing is important. |
| Export to PDF | ☐ | ☐ | ☑ | ☐ | \- | Nice to have for offline use. |
| Map view | ☐ | ☐ | ☑ | ☐ | \- | Useful, but not needed for first demo. |
| Attach booking references | ☐ | ☐ | ☑ | ☐ | \- | Useful, can come after base flow. |
| Email import (auto from inbox) | ☐ | ☐ | ☐ | ☑ | \- | Heavy build, not needed for hackathon MVP. |

**4.3 Final MVP scope for the hackathon**

* **Must-have flow:**  
   User creates a trip, days auto-generate, user adds and edits activities per day, and sees a clean day-wise itinerary.

* **Should-haves (max 2):**

  * Mark activities as must-do or optional.

  * AI suggestion that proposes 3 activities per day for a given city and theme.

* **Parked features:**

  * Export to PDF.

  * Map view.

  * Attach booking references.

  * Email import.

---

## **PHASE 2 \- BUILDING (Example)**

### **Step 5 \- Architecture: screens, flows, data, backend**

**5.1 Big picture architecture**

* Front-end:

  * Trip list screen.

  * Trip detail screen (day-wise view).

  * Activity editor modal or page.

* Back-end / automations:

  * API to create/read/update/delete trips and activities.

  * AI endpoint to generate activity suggestions.

* Data store:

  * Supabase with tables: `users`, `trips`, `days`, `activities`.

* External services:

  * OpenAI API for activity suggestions.

**5.2 Screens & actions table**

| Screen name | Who uses it | Key actions | Data shown |
| ----- | ----- | ----- | ----- |
| Trip List | Logged-in user | Create new trip, open existing trip | Trip title, destination, dates |
| Trip Detail | Logged-in user | View days, add activity, edit, delete | Days with activities |
| Activity Editor | Logged-in user | Add/edit time, title, notes, must/optional flag | Activity fields for one day |
| AI Suggestions UI | Logged-in user | Ask AI for suggestions, accept into itinerary | Suggested activities list |

---

### **Step 6 \- PRD with AI (example output summary)**

**Goal:**  
 Help busy professionals create and manage simple day-wise itineraries for trips in under 10 minutes.

**Users:**  
 Primary: 25-35 year old working professionals, planning 3-7 day trips.

**Scope (M \+ selected S):**

* Create and manage trips with destination and dates.

* Auto-generate days for each trip.

* Add, edit, and delete activities per day.

* Mark activities as must-do or optional.

* View full itinerary in a clean day-wise layout.

* AI suggests 3 activities per day for a city and theme.

* Share read-only link of itinerary.

**Out of scope (for hackathon):**

* Map view with pins.

* Email import.

* Complex collaboration.

**Core flows:**

* Create trip → auto days → add activities.

* Edit activity.

* Delete activity.

* AI suggest → pick items → add to day.

**Data model (main entities):**

* `Trip`: id, user\_id, title, destination, start\_date, end\_date.

* `Day`: id, trip\_id, date, index.

* `Activity`: id, day\_id, start\_time, title, notes, priority, created\_at.

(For the learner, the PRD comes from the actual LLM, this is just a sample.)

---

### **Step 7 \- Platform optimisation: starting prompt for Bolt**

**Chosen tool:** Bolt \+ Supabase \+ OpenAI.

**Sample starting prompt (ready to paste into Bolt)**

> Build a responsive web app called “TripThreads” for planning travel itineraries.  
>  Users sign in and manage trips.  
>  A **Trip** has: title, destination (city name), start\_date, end\_date.  
>  When a new trip is created, auto-generate `Day` records for each date between start\_date and end\_date.

> Screens:

> 1. Trip List: show all trips for the logged-in user in cards with title, destination, dates, and a button to open trip.

> 2. Trip Detail: show the trip summary on top, and then a column for each day in order. Inside each day, show a list of activities.

> 3. Activity Editor: modal or panel to add/edit an activity with fields: start\_time (HH:MM), title, notes, priority (must-do or optional).

> A **Day** has: id, trip\_id, date, index.  
>  An **Activity** has: id, day\_id, start\_time, title, notes, priority.

> Core flows:

> * Create trip → auto-generate days.

> * Add/edit/delete activities under each day.

> * Mark priority as “must-do” or “optional”.

> Add an “Ask AI for ideas” button in Trip Detail.  
>  When clicked, open a panel where the user enters: city, trip theme (e.g. food, culture, adventure), and day index.  
>  Call OpenAI API and return 3 suggested activities with title and short description.  
>  Let the user select suggestions to add directly as new activities on that day.

> Use Supabase for auth and database.  
>  Focus on a clean, simple layout.

---

### **Step 8 \- Day 1 & Day 2 execution (example outcome)**

**End of Day 1 (for learner):**

* Ideation completed.

* Architecture sketched.

* PRD created in a doc.

* Starting prompt for Bolt ready.

**End of Day 2 (for learner):**

* Bolt project created.

* Supabase tables set up.

* Trip List and Trip Detail screens working.

* Can create a trip, see days, and manually add/edit/delete activities.

---

## **PHASE 3 \- BACKEND, AUTOMATIONS, DEMO (Example)**

### **Step 9 \- Database and CRUD**

**Primary entities:**

1. `trips`

   * id

   * user\_id

   * title

   * destination

   * start\_date

   * end\_date

2. `days`

   * id

   * trip\_id

   * date

   * index

3. `activities`

   * id

   * day\_id

   * start\_time

   * title

   * notes

   * priority

**CRUD coverage**

| Entity | Create | Read | Update | Delete | Notes |
| ----- | ----- | ----- | ----- | ----- | ----- |
| trips | ☑ | ☑ | ☑ | ☑ | Done via Trip List and editor |
| days | ☑ | ☑ | ☐ | ☐ | Auto-create, no edit needed now |
| activities | ☑ | ☑ | ☑ | ☑ | Edit/delete from Trip Detail |

Gap identified:

* No need to edit days in MVP, so left as is.

---

### **Step 10 \- Automations and AI enhancements**

**Backend & automations**

| Trigger (event) | Tool / service | What should happen |
| ----- | ----- | ----- |
| New trip created | Bolt \+ DB | Insert trip, auto-generate days between start and end dates |
| “Ask AI for ideas” button clicked | OpenAI | Send city, theme, and day index, get 3 suggestions, show to user |
| User confirms selected suggestions | Bolt \+ DB | Insert each chosen suggestion as a new activity for that day |

**Wow AI feature (example)**

* Name: **AI Day Planner**

* What it does: Suggests 3 activities tailored to city and theme for a chosen day.

* Prompt idea:

   “Suggest 3 short, practical activities in \[city\] for a \[theme\] trip. Each suggestion must fit into a half-day and be easy for young professionals. Return as JSON: title, short\_description.”

---

### **Step 11 \- Testing and iteration loop**

**Scenario test**

> A user is planning a 4-day trip to Goa with a “chill and food” theme. They should be able to create the trip, see 4 days generated, manually add breakfast and beach slots, and then ask AI for ideas for Day 2 and add them.

**Bug/gap log (sample)**

| \# | Issue | Where | Prompt used to fix | Fixed? |
| ----- | ----- | ----- | ----- | ----- |
| 1 | Activities not sorted by time | Trip Detail | “Sort activities in each day column by start\_time ascending.” | Y |
| 2 | Priority tag not visible in list | Trip Detail | “Show priority as a colored label next to title.” | Y |
| 3 | AI suggestions panel closes on error | AI Suggestions UI | “Handle errors gracefully and show error message instead.” | Y |

**Stability checklist**

* Must-have flow works twice in a row without breaking.

* Activities save correctly.

* AI suggestions add activities correctly or fail gracefully.

---

### **Step 12 \- Demo and reflection**

**Demo script**

1. **User and problem:**  
    “TripThreads is for busy young professionals who feel stressed planning trips because their plans are scattered across chats and notes.”

2. **What was built:**  
    “Built a simple web app where you can create a trip, generate days automatically, and plan a clean day-wise itinerary.”

3. **Live walkthrough:**

   * Show trip creation for “Goa, 4 days”.

   * Show days generated.

   * Add a few manual activities.

   * Hit “Ask AI for ideas” for Day 2, add suggestions to the itinerary.

   * Scroll the full plan.

4. **Close:**  
    “Next step is to add map view and better sharing, but even today you can plan a full trip in under 10 minutes.”

**Reflection (example)**

* What worked:

  * Users liked the clean day-wise view and AI ideas button.

* Issues:

  * Some confusion on how to edit trip dates.

* Next 7-day plan:

  * Add map view and simple sharing link.

  * Improve onboarding copy for first-time users.

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAocAAAFcCAYAAAC6BRSTAACAAElEQVR4Xuy9eZjlRnnvP3/PTJ/u0z1bz+qZsWe8jM3Yns3jfd93e7wbLzPYxhvGO8YrOxgwNtjGKwRsEnLDEgiX4EsgZDMhDwFyWfLk3svFhhCwwYawxP7dRL/zlvRKb32rStLpPu/po+764/NIKknvkV5VqT5dOkc9a+6cuUkVQw1nOBKZBFifmgy27X4zR4vZvWJOzuxIJBKZoczCmzeDnUqTwc6+KbTmTj/wHJsA1qemg219qnAEr1c4wtcthSBGSYxEIjMRrxxiZ9J0sLNvAihV0wU8z6aAdarJYHufKhyp6xWO7HVLlMNIJDKzqSWHrTluZ8nQOtx+KsHjayooVdMFPM/pANbBQQfb+1ThSF2vcGSvW6IcRiKRmc0s7DgQ7gC5cx8RyM4e9+sn2FkPKihKkWowh4PIoP2B1A0obFOBI3e9wBG+brEFMYpiJBKZSZTKYd4BziUZHEraAJXROoNn/36AHfWggtITqQ/mchCJgjg5HLnrBY7wdUuUw0gk0hza7bFk8eJlyaJFS5KhoWFnfTcE5ZA7PRohZBkcHbJxJNETRwPsmAcFlJpI/8BrMZU0URRR1qYCR+56gSN8EyHKYSQSGVzmz1+UzO14GEKySPdB3L4OpXJInS6JH4ngWId5Q61kXquAylgSWQ770TFiZzwIUK6WLF7uSEukP+D1mGqwzjYBlLWpwJG7XuDIXrfE0cNIJDKYDA+3HSlEcJ86eOWQOzgeNTRi2JHBBcRwhhBEHj3kThrjTRbseKcSlBLJVMmh/B7oVEJ/IOCxDQJ4DfsN1udBB4Wt3zhy1wsc4ZsIURAjkchggSLoo90edfarIiiH1Knyo2QWw1VjI8lfHbc+eeX8rcmG8Xm5IPLo4ec/9zmz76uvvprHOuXkU5KXXnopX251tsPPG+scOE3//ut/76zjDnbB2Dwz/d3vfu90vsxe6/ZMFmbbff3rXzfThfPmO9tJlixcZKbPPvusmdKxj89fYOYdyRhKBTiETw4PPeRIM92yaWtlLJKr9hCJdipbO3Zcnc+PDg+baXuoZUuZ2L5pTKVMYj3oB1i3Bx2UtqnAkbzJ4ghft8RRxEhkOrJmzW75/IknnmGg+cMPP8YqX7JkebJ06fLO/WQo2bhxPyNfVL5ly0HJpk4/f8wxJzmxjz325OTQQ48y86Oj85JTTtmWx9uwYT/rMyne+PiSZHh4xJSfcMLpTjxmfHyZJYE333x7snLlajN//fW3OpKI+5cRlEMjKkIOl7ZHkk8cunuSXLh/zvJO2fxMDp9+6inT4R952OGWHP72t79Jzjj99I4MtZInn3giOfLwI8z8tVdfk9x6y63J6EjbyOFzzz2Xy+Fpp5yavOPtb09+/7vfJbutWZt873vfM8J21rZtye9///vk5BNPTJYvWZo8//zzyUEHHJicctJJ5phJDj/5yU8mn3j6E0YOv/vd7xpZpFHNu++6K7nx+huSeZ3Po22/8fff6Hze15PR1nBn+6fN9iRedOwrl68wAnHowYeY46D5d3amH/uDP3AkQ+KTw+3brzLTkU6eaHrwQYd3zrdt5k85+czk8svfYOYP2v+QZMf2q5MFo2PmXCmXJIebNmxOXrPn+mTZ4qXJ6694oylfs/Oazn7XpaLYyf2KpcuS3dfubtbtustaR8IGGcxXP0F56wfY1gYdlLWpwBG8yeIIX7dEOYxEphv77LMpn99vvwPz0bZt285Pxsbmm/l58+Ynl112bbLzzmuNtB1zzInJUKcfpm1bHZc47riTzT1mwYJFVuwdO64x62menICmtN1BHR847LCj8+1WrFhlpuedd0ly5JHHm/nXv/56K5aEYkr5GxkZ7cQ7MnnooSccMVy4cLGzfxm15XDJyHDy/i1rgnL4yiuvJD/84Q+TX738siWH//Zv/2bKH37o4eS4Y441ZTx6OL5oPDlw/wOSPXbb3UBySOtofs8OJId0LL/61a+SvXbfI3nfvfeakcP777vPlN9x++1GDrnjfQ2MHNKI5Wv2WGdka3zBwmRe5wKOdmz8Jz/+SfLnX/xi8pOf/CRZv+deyV997Wtm5JCEgY6dposXLTLTvdevN9P9tmwx0oqCIfHJIV1Ynh9fOJ6sWLIs2W3X3YwYXXHFdUbyaJ7lkObXrN7FTOXIIcnhJRdfYeY37LMxOfbok9J1ndwvXrjIQMvzOuKJAtZUMJeaoMRpgu2tCaCwTRWO6E0WR/zqEkcQI5HphJRDGhHk+bPOuiC58MIdZn5BxyO2d/ppkkMSQJZD3pbkkIRt/vyFVmySQxpppPmLLrosLz/44COSrVsPypdZDkkgr7zyBjPfjRzSaONhhx2VPPbYxx05pF8w4/5lBOWQOsxcDoeKx8oP7b82efHszcnqsXbxvcMOG/fe23To11x5Zf4Y+bUXXpjH/Nd//dfk3e96d/L973/fLH/m059O/uLLXzbzL3eEcvWqVWakbuniJckzX3rGyNuLL7xgjuXpp5424kiiuf3S7aaMRg0vveTi5ID9tuad7p4dgeTHz1/96leTRx7+cPLtb387uemGG5I//uQnk7/727/Nt92074bkPe9+d0cUf2zkddOGjcnPf/5zc+wsDF/rSOPDDz1k5jdv2mRGLFEqJD45JC6/7A3JPuv3NQK3vCN5lKfLOmU0XTg2lpx//qWd8zjIyOGOTqVgObo4k0GC8nLhBdvN/D5775vstHyn5JJLrjByeOKJpyZnnnGuWTed5LDfj51R4rTA9tYEUNKmCkfuJosjfd0Q5TASiXQPjfBh2URYuHCJJYDvec/9HWEcMfO33/4Wax2V4/5lBOWQ4Hcbyh+k0OPlFR3oRyk0aih/scwdLMarA3agGqAM9BqSw/SdkBODRwwj1WDuNcD6owW2hUEGZa3fOHLXKxzxq0scQYxEIlMHjhCGwP2q8MohQZ0WdZBSEFkSDUP+V9lgnDKwk9QAO/xeI4VlaUcOUWL6R/qL8f6CxzAY4DXqJVi/tMC2MkigsPUTR+p6iSN+dbEFMYpiJBLpF2NjCxwRROj+hvtVUSqHhrnU4Va9BLv7Tg07Qy2wc+8lKCVTB0pbP8FjGQzwWvUSrGMaYHsZNFDa+oUjdL3GEb+6RDmMRCJTA33HEYWQoO9DTmTUkAjKIZF3VnOpwy1ksJDCYsSwmw4NO8Jegh25BigieqCITSfwXHsPXjcNsP71Gmw7gwgKXD9wpK5XONJXlyiHkUhkapk3b5H5ryj0upwFC8ad9d1QKoeE7KhMZygR63C/ENj59RLsuDWYzHcKuwNlajqC59x78PppgPWwl2D7GVRQ3vqBI3a9wJG+boiCGIlEpgeVcshgpzWRzgv37SXYYfcalI7egtI0k8HcTB68lr0G62IvwTY0yKC89QNH7iaLI3zdEgUxEok0n9py2Auw4+sl2GH3EpSN3oOCpAN+LaAOGEMfzE1vwWvbC7Au9hJsQ4MMils/cORusjiy1y1RDiORSPOJcljCdHqEjNLXDRhLF8xN78HrPFmwLvYSbEODDIpbP3DkbrI4stctUQ4jkUjz6YscYofXa7Cz7gUoFJMHJai/oPB1C8brL5jLyYHXuhdgndQA29WgggKniSN3vcARvm6IchiJRJrPrKVLViQziqVdgPuWEdoeY0ZmLlg3sI5gGW7XDfjZkwXjN5wlkUgkEgkya372n06IBcNDnelQsoAYDsDrs/+YUiDXFSzsxC9jUQXjgsXMCDNcYMp5OV1P/w86Rc4XLK1iOJu2h5NlI1WMCNKy5Z355WbK8xltF/qvM7SOpgY5X4OdBLxcrBsW2NumhMrTdb7PQPB4ugXzUeSL85fm0M17GLpuBpqna8nXswSsI0X9SZF1b0nnOLHOMVxfZf3Fuo1Y7aIT08y3ijK37fnaYVaO7RbasGnn1N47cS2yewGSv/zeQC/DZ3Bd+u80xzrrcrIX6PNL87uljcwl6N97pv/isxgVDo80W29ZwFFf2maolS/jSCgyd84cDziqKdZ1Ys6Z444o8qhiHF3sLTT6i2W9QjN2JDJIzKJ/g1cgO5GiXHZaVicU2KaMtCMcdjpGi07HSIwLLBEE3M7cTy4BLAwlGMFoS+HzY0kfg6KTgUJUFxQxwyjMT4CVnnlZVhs8Ng94TnXA/PnlsQCvjUVbLrvX2wfWH4T+lSTPcz3EuknIesx1e9GIp95DG8C2E8Jqw6J9hrfzt3PGEUam5RPFMKkkljDkEcZOOcphUBID0P8bN5AoDtG7WP20DKkQSjlEhiQeWax8lD7X9wicRAPw3KAj3aMpcJqxI5FBQsghjjC40ud0QqIcOyKER0ZSMWSEDPJ8tlwmhthJ1yXv+PMRpZGUNk2L9cXok0cyRjIZQUnheZSYDBSfOtgjemJ+tO0IWkjqqLxX+D7LWmeOLZv6jhtGIfF8Q2Auq3KN18sFRTC7/nKkMQPrkFWf2oUcSrC+2oLIf/zY9T1tA0U7oG2xDYWQ7RDB7dy2LsuHcxwxJFrdySELYlAUh2w5pLJCDv2SiCJYxrDEK4eFAKZyaJc5cihkEHGEUDDUicvzZWIY5bA3aAqcZuxIZJCYld7wi8dM+aMrlMX8kVYIEka7DDsxxBktEcjHcdYjZQIe7xmG8TEyLkPHXodh91FlCHsUSz5KzuYzcUHxqQOLlPtoWD4uLmclMxpAbiP3G3VjlVMcFx5/N+QC6M2nLHOvhY+6j5UZu74Uj5VlXSI5TOsf1smirmI9xnoukW0jl8OWkDurrfEyz7vtL2/TvnYsylD+QqTCx4+S5WNl+zGz9UiZGHIfKzsjhiWg9Bnm+h4r+8FHyvxYmX/oY40cZrJXhv0oGR8r4+PmdB0+To6PlfXQFDjN2JHIIJGNHHo6kRzumDJwHjq1ENz5YYfog0ZXCtxRmImMHmLnn5KOJMkyWyrcEcN83pKXDJYaAUoPEhY/ZNgZEZzsyOCqDCyfKDiq6EojkgqknC8Dc2shrgleNzliaAljTbAu5XWq7Y4cYj3FUUMzcoh1foRHDmUb6G7k0GqnXJa102I7bNt2O+fRQ2fEkPCKYjXOaKHBlkaUwRCOIPqYW8zTY2V71NAjiNm01mNljyjWGTnkx8rpyKF/xBCFMTJxNAVOM3YkMkhUymHe+bREpyOWsaMK4XSIEugYnVEY6GyxQ67CGTFqF7A4uGJoyyELYD4vpUQuAyg4EnfUTUoUlNEInhCwiSBFkMUQwX0mSiGybfdccmgdT9P1mCME8+vDlUK/HLIgmqmoE3UfLfvkkMD6ivU5F0Cu+4zVBtJlbEc+ZDu02ijRkuvc9l20f5rSI+V0vzIx7FYObUl0RxRZ/uqIoiODJdiPld0RRSmAtR4rEx4xrJLDoaHAY+XZfvAmHekOTYHTjB2JDBKz3M7CFkPTqbQ8nU62rg6ODBpEh5h1jubxsSWDPRBDQsqhEIByebDXlQkgg/KCYlNLCkmorG1YttqOgCGrxvzboABOBIyFnxEi/X6kFEQQR5oaOWTKBRFzHkJeN7yW9rUuyoKCOOzWK1O32n45JLDeoiTSdw7No+aRajmsK4kMtlMWRGzffjmsJ4gogSFcORSSOCTIykaJoTAogFVIQSx+yZxOpQAOl8ihJYgghXUEsdWJbcthuSDiTTrSHZoCpxk7EhkkSuWQBdErhy23UwrhimEmhzyfdYT5dwt7OWpI1JJDd1TJK4c8rQClpp4cDnvkkMrou3+ueCGrxsR8FWMArq+APwOPwYf9iFlIsJFGWw4xVz4w114cGQxd66KsTA59I4ghOcQ665XDrL7XkcNuwXZaTw6JfsihO3LII4ZGDrP5ECh/VRRiGB45NI+ZS+SQpDAXRBDCenJYjBymgpiJYUAOqRxv1JH6zO1cRyzrFU2Vw6Yed2TqyOTQlb+8sxnJOhhYZ21TgSWFsjMcSUcLQ98r7FoK26Ljpg4dO/t29svkNsoCCwOWpTiPkVFE2q7A+MglKP+1Mc8X5DJVZ6QQGWu7ZYLVQgZXd7a1SdfLbbzSGCofdY8PsX9l7Z47izHnCvNXBl6P/HG/53qWkT5m5nqC9SetV3kd6xyvrHM+sB774Pov28XizjHIP6SwTZURkkPv+hwphxKQRKJlS2JdYfSOHkpRFOvMr5aZoYlJIr3GhgUxf7WNB/N9REsO+TU3tixO9PGyK4eeEcSMKz6+Nbn5mUMHmvPfv6/TkQwSUQ5dmnrckalDjBxyBwHiF5DDbrBGC6ET7K8cFoKIUlBbDgOgrPgIy2ExX0hUuRyimKXyVy2HBSiHAVHEOJOQQz43nvopcoX5KwOvh/wuKF7POtfcK4dUp7qUQwLrsk8MibAcum2qjPpyiO3eFcO6cogi6CMoh0O2GFpy6HmlDUpgFfZjZRd35NAVwzojh7QexTCVw+KxciGHthQOteYa8br2UwcOdkfeOdYbv3iIOVaad9YPAFEOXZp63JGpo/7IISHKu5HEXAxpKjvB4eLRGnaaCHa4ZeDjY5RDFIEqUejVyCHhE0KUIwKlSoJSZokblmXlhRBWyaEtkV4Z5GVYx8eGx2vLYXF+vvOWP1bB3JXhFUMBXtPQda8cORQyuGy0Wg6xHvvgXzOH5BDbUx3qyaEERw6prN7IYR1BRPkrE0QSQFsQJz9yKN9v6MohbeuTw/6NHJJsbT17dfZYefA78gvu25AKomfdVBPl0KWpxx2ZOkAOPSOHtNwSiA4FO6QynEfLYrl41YefiUiiJYi8nFO8vqYQhAo5RFBIPMISwpagDCFOdQWRp460ISB8tiD65j2CiDE94DH6wHO0zl3kA3MWAq+BTw7xetoU196tJ1CPsrqU17HRcjn0CaCf7LuHom2Mj0xMDmX7HF+wKFm0aGmkAdz8pUOdskGH5HBkrOV0KlNNlEOXph53ZOowclj//ylLQBph/ULC03lZkijAlwVL3B+pFD9UKTpi90XXEquzzx4PojyaHyVk6+wfLdjg//t1SdcZeeksV/2fZFsUxY9TgOKl1a50GVHMJI62QXFDVgfA7crAz08pjhOP3z23mkKY5TXNZ1nepRC6103ivN6I6wSTlWM9kpiRw2y+EEGspyR6bp32Yf/BNOK0HdOmuF3lbQ7bYWddu53Mm7co0hDWH7FzsuH4tU75oHPpI1uTCz+wOWm1hp2OZSqJcujS1OOOTB2z8v+OwqAYSnkMdEZ+OUw7MOzgUApDcGfpl0N7JJHL0446LImOBIAcynKUCVcOUQZtMZRl1XKI0hSmSg5ZzFDkekMRN3wcZWLoo5BizAvKoZ1fVwgleM0QSw7bGR5BxDpk1ad2iRzKOuup35WMwI9QuD1x+xqWbc5ui9iJRwaXhQuXJPudviZpt+c1jvPes8mMHtJ5YMcylUQ5dGnqcUemjspX2RQjhyiDflAGuxVDHE3BURgUwzpYI0QMyYCcjmTi0HZFIqXiMTPRtnEkJ4A7muYKVFjGUA6z+Qw53yvwc12qRg+lFI7kj5QxLz7yPGPuPdiPjf1464OoE2WCiK+ykXXTJq27WLe5vmMbIGg/bD8hrPbXOWcUkMhgwpLVVDk8513p9w7pXObOHZzHy1EOXZp63JGpo6YcuhJYRjHK0QM5JGrJYXjE0HTkCEuAFAFRFhLDoBySsDBZmZEZj+AgcvSsDFfCbIqRQ8+6CeAKH5aFqBJDVxAxJwjn0cl7gCoxtK69nOflbB7rkVWn2jXlMKvHWLex7lfKIbQr/mPMfMcwa3uL2qOOhEQGj9HRBblkNV0Ox8YWJq3WiNO5TBVRDl3icUe6xTxWdmQQSB8ruxJYQOuLbbAT61YQCdl5Vgkil2PnjTiPDVEKeJu2KxOFJKZTW0bwsTKud2UnhCtQQD4qh0Im5TBEtl0FPtHDGKFjqCeFNpgDBHNZ59Gye+1ADn2PlQlRP7D+IP7HykIIzXxaf7F+VzISeqwspNBph53yKIeNIMqhHlEOXeJxR7ql8n8r53g6ohC9lEP30bLdCRedc7kcOgLYUzlEccEyV3hC1BpFJAHL5ayQtlTspMR1I3UISmG9/ZxjBfAc8fwR6xGynC/B/SWyi3XN2wLxfcNuRg6xXkrqjhZa9X8kPHJo2thw1t54mlE1cvjAA48k5513cYeLnHXveMf7DJs3H5CcfvrZzvozzjjHKZtqtm9/fXLiiacm9977QTP96Ef/yFpP5yOnyIoVq50yYvHi5cnSpSud8jpcccU1ThlSJYevvPKKU0bcffdbkn/+53+2yhYvXuZsxyxatMRMR0fnO+t8XHfd9U4ZsXz5SqcsymFziMcd6ZZZ9N4yRwSBhUYO6wmi1ZFh55aBHSGCj9/qCmIVlhAQLARQjiIRxhUTi0xmUHjKwEethSja64qyVLqkEKbLmbDJ+a7J9rVioChmsuo9Rv/5uOdc/k7DPJdm3i/ftcSwXczjNQ+BdciqT+1UDrE+phT11fdrZVnXsf5TG/HKISHaFYqhkcPRsBxed93N+fy6deud9VKstm07PznhhFOTRx75qFl++OGPJG96091WnCeeeNps98EPPprMnz9uuOeedyV77PGa5N3v/kAe6957H0je9a77khtuuM3EIaGjfeTnHnvsyWa7q6++3jmuMigWTd/2tnvzWHI9L9N09eq1yXvf+0GzTMfz8MNPJqtWrTHLDz74RLJhw36d8/2DjmSeljz++FMdIVptjumii16XXH75NfkxX3DBJcmTTz5tfc6b33xP8uEPp7miz9qy5YDkvvsesraRlMnhlVdenfzyl79MzjzzLEfIvvzlv8jnTzjhpE6e7+1I7IrkU5/6dPKd7/yT2e9HP3ouufPOu5Kf/ORfk/HxJZ1j2Zo899zzZp+jjjom+eY3/zH57Gf/NNl//wOTL37xS8lf/uXXkp/+9Kdm/c0339rJ0fs65X9ulp977rnkjjvuSl599dXkf/7P71rHEuWwOcTjjnSLZ+Qw63QyrI7Is05uU0bR+dF73IqXYBt4nqYj+A447HS7E0LTiTOWCBb/KUXKgBQ/hOSEp9b3C+UygKJThV8AM0ZTXImbeuSxOe8xtERWnl8qhemUcXPCYG5D4HXzI6851QEmqxuivmB9yutVu/7/VsY6ndZzUf8J0T74vYfYjiopkcPzz784nz/mmBOd9SQ1BxyQ/sCApO+AAw5JNm7cmmzevL8pk+K2bNnKToyTcmE87riTLTnk7Q488DAzZTmk+TvvfLvzuSSHNP/+9z9orauijhzuu+9mMx0fX2aOb6eddu4cYyrHJIcPPvh4Pn/ffenn03GTHNL8Rz7yifzYDz30qOTUU7eZXxnLz7n11juTXXbZzcyTRD755CfM/KMd2ZTbMSE5POKIo8yUJE+KmOTss881UymHtHzppTvy/c488+zkmWeeMXJIywsWjJspySFNP/OZzxg5pPkjjzymc0wLzSgjyeEvfvHL5Pnnn0/uv/+D+Wdef/2NznFEOWwO8bgj3TKr+G8HqRyWvfPQfqWNhEYtsCzF6bwAHDVB8pFDiW8U0ZRz50yPmOVjZveRM44QGeT30Hh52DMCFaAYvZLL8P04ITEoP1XgSByKlxGzvGyydBPLJ37u8dfF5IfzlecvzWGRWzf/iPx6AD4uLsOuK1yXCvgrDCSHOEpoEHXVN1oYQraLfORQjhRa7Y2Xi1FD095K5JDZb7+DjMideupZVjmNfvH8EUccl6xfvyEfYbzlljs7EnFcvp4lbvfd9+oIxR1m/q673pFcdNFluSQRCxYsNnJ2111vzx9lr1u3d3Ljjals3XPPOzux7zByeM01N5jRO3lMdSH5xDKCz4mmdFx33PG25LTTzu4I1gXJZZdd3RHAVWb9pZdekWzatH9HmA5ONnemNDq6dOlOZt1tt92d7L33xo4g3WqWDz74CHNe8nMuuOBSI500/8Y33mJEFCVYEpLDc845L/nHf/xWDgrZySefmjz77LNm/gtf+O+dnF7Y+aylnc9/rRkt/PznP2/WHX74kcm9976vI7GLzfIzz/wPMyU5fKAjfdu2nd25vvuYsquvvjZ5/PEnzPxNN92cHHLIoR3pf7NZ/tKXnunkaKdk8eKlyZ/+6eesY4ly2FuaGluTph73dCAbOWQKEcTRxKKD8iBioPz54I4QO8cQpnNFGfSAAhjC9yjZB8qGC4ws+mDZycjlxyNFdZCjbihj6Ugdilu1xJmyXCz9MVLx9O0bBo+9DpgvC8wt5J9HBEPg9Q2B9SVE2WPldMS7eKSMdToEt5HgY+UMq92KdlhHDvsNCSSWITgSN90JyaE2NEKIZcySJeHvLvqIcthbmhpbk6Ye93Sghhza0md1SNhJwbY+sDMMgd/L4n8xhp1wt3Jofc9QTnm+w7K2/Pd6KIK2FDoCI2DZScUne2w6Kh+hCqhc/K9hKjMC6P3fy7iclq0UyzSPj3u5rJgP4T4yXjnG5XIbPDZ5PHCcwfPpMDbqlHE+8nzhPORveYhRmO+wzDDip20v07/IS//PssvyznHz/JISFhOdemOmzjyPPgKdY5T/a7mMhYLxsTFHRCKDx1TJYS+Rcjg83DYd+SAwNNRyynqFZmySWiyLTByUHaTONjOZ7AcpIUEsyqxRCxTDLkcQUQSrSOXQ04ECKIIhrF8qCym0ygB3hMoFR7JwlAvlsRBHe74uOLpHQsbl6RS3KUb1DLmM0TILnG8fOXKY4vt8PL6JkI8Q8hTAnIcppB6vpXPtPfNl/zM5r0ft8MghY75j6KnTZZg2MhIeOeT25W13I/El2E1gusmh5mhdt2gei6ZQNDW2Jk097umAkcOwIBbLTgclOyVfJ1WB1RFW0I0c1pVERxAYlIdsvS0dKCJhquQQYUFCaaqDGXHzlOfr24XAFTLIFDKI+8nYofV1QSmWZTmcK8yfJ79h0mtH8871JOT3D0U51w2sLwjVsyo5ZDHsRg7z9jHil0OrnXraHYEiEhlMxsYWmFfMNF0O6VywY5lKNOVQM7amCGnG1qSpxz0dCMghgYKYdVAjGXLbQCeFHZvE6ggrYDmsI4gMduYOKAsjrihIWDpsUaxHt4LoAyXLR5UcuvD21ft1H9sGzyeIzFM2j/msoupaWtcbtuO6UTZymNexduCRcEa9UUP+lXJK3iZGasghI9pe2j6HHRGJDCY06rbfGWuNJDaLBbkcDloHrilwmrE186gZW5OmHvd0IJdDvyAGRI8FcUR0Th45dPYDuDN0O0yXbsSQwU69VA5ZGPCRc04mHzydAI4I1UTKFUqXZLICV0a3sfEcukLkCnNYF3nd3GuZXWe63qIsl0IC60uGVbfaNeSQ8NTngkIOrbYx4sohtq287WXz8g83E2N01LzmhH51GxlcNp+we7Lh6D2c8kFmyZIVycUPbkkuenCj06lMNZoCpxlbU4Q0Y2vS1OOeDlhyGBZE+xfL3FGZeRJElkOJ2B87OYQ7RrfjFIykX77nThc74iqwk2dB9MkASkMhGSwaKCM8mih/wOKOMJaOHMr1PB/YB0XMR93t6sJyyHF98fE4veeH5wTnhzlzCeeXCQoh46sDsgzAupTXqbZfDvPHySP2qGAVVpsYKeTQaY+etib/YHP3gx+XdWLTlNs73gOQea16jNE0257mU4bs+aGU0S5oVzAyt2B4yCVdNzcZ7tAKMNI5vlZnO14eksyB+Yy5NaDObcj5oUGn05ttc9OXDnVuznXQ7DyrYtOoYXt+yymfajQFTjN2Vb4ng2ZsTZp63NMBRw79gmj/alnO5x1RC4AYKIQhsMO0oM6WO98aYKeNnX4uB1g2UiKIvI4kxMDLKVWCKEceWYzy+TJQtjxUCppnexS+EPToGcu6As9Hnnu2jZMrL0Vu03yn5d5r4ly/tByvdRlYh2TdIjnEOsc4ddeDrPNOOxipKYdyv2wk390Hvh7SiY1t3qFVTFECQxg5zKYuJIm9F0NHDqUg8rwpL5fD4SGSQ48YSjmkaQZKYAhXDqnDs8WQbsQkWmu3LnZu0FVodp5lsU+6ZU9zzFg+CGgKnGbssnxPFs3YmjT1uKcD4iXYYYoOpgbZi3rdF2ZDp9ZyO0RDoBw7VvlFf573kb+UmKYOrjRSOUkESgKCUhh8wTKUpxKEAtkbUgnL5jMBK+bL/+0cksfkGFls56XesP3EcPcvy2EVeK0K3JehE7YAcr1wX2qNdcvIIZRhPfWJX6iOy7ZBcojthdoUtyt+aX0dUPYWdPKJbZxB4bNJBc8I4FAme2I0kMjXCVD4UPxqSeDcFB4F9MECKOcd5hRCKGWP5FAu+7DFb07BbDHvkT8jh2JZSiEzf0nbyNbZ79rHuUmXodl5hmJf/vGt5liHhvVEaTJoCpxm7FC+e4FmbE2aetzTgVny5o8dRQ51XAa34/HBnVgdQTT/1aGVdZghRAeKHW8Z2HH7JRHFgDp9Fgn8TythpJjk/41Dkq03787LRrDkaJYRonYmR1k5ClMV2uKJZRMhdF55TiSYQ08+eRmvRwpfO/wvJwEJ9MDC5xM/2h/LGBQ/p05DvaZl/MNJth3ZproSw5bbnlEOXQl08YmgDymHKIOIJX5yGdeVCKFPDnFU0IwMEnOEHIL4lckhjgbmQpjBspeLYUAO6YbrE0NmbmtuctOXDjHiNchc9cn9nWMfJDQFTjO2pghpxtakqcc9HfCPHA7bOI+1PJ1Q/sgqw5FALuP1Ytu62B1wuGNeRJ26gR8FFvNIKgrFvKHOyGG2jSM0ZZAYZY9PuSwXJLPOlaYCfLzKslYs1380626fjv6FqRe77Dh9ZOsodhse0QtxdsqxTKzD61SFrx5I0sfEXJ9SqI7xyKH5qgPWPwHW4TJk2/CNHMr2w9vZ7RHnC+z2HB45pPUohj68j4xbmRwKiUQhLINk0JLGACNEPoooYUksHiPzPMoiYuRwLoghLLuSGCaXRBOHHivbwhgSxG7R7Dw1Y2uiKXCasTXzrRlbk6Ye93TAGTnkKXYYriiiHAYQox9ORweYDo+m2bx3hCUDO+EynNFDIh8dAiEYliNL2UhiJg/dQsIi540MkgRJwQlJECFHyCrlsXejez4mEts5N3k+vF5uF8iDL591kNfOud6mDtjX2QLqDdYpgv7DCZZhPc0Rddmq72JZsqgjzuk8txtP2woi2mzLheRQtnMUvxC59JWNINJ2Q674+UDpC5KPHoYfKzuPj1n6hAASJHk8lXQ9csiPkGenWKOGgZHDXkoho9l5asbWRFPgNGNr5lsztiaax60ZezpgyaEEOxT/aCJ2SgFK5TBULjpUAjvbDNkhY0cdwhXETBSyclsmJi6HCMkNjZY5j0hLHpd6xUrKlCAXz0wknfXZvlWSifuZfbLH4XIbax95bDwvzwHPh2PzvFhvciXmJ4Itg+Frjev4D4iQEFr1aMT/GhqHrA5j/TYMe8o6pHKYPkJOJdLTrrxAW215GC7kENt9iLqPlUkOUQIRr/xhGaxPJdAvh/ljYxBBhGWvGzksE0Mph4YKOaQbbpRDfTQFTjO2Zr41Y2uiedyasacDQTkknE6FgM7H7ZxK8IqgLONtuCydOp1tAO6ksRMPIQWBHhdacmith9FFj4wUlMsk/1cNMw/CZMpkuYTXmRgeRkj6skezcnvc1xcH5+UxZPNGauV+vhi4Do8dz8e3bsTN2UQopBCuZXa98+suyrF+VMFyiPUQ8ddvX1sotkkfK3vaUBBqi6JtUlv1YNr1cCqH9agphUyrXA5R+nJwnVhfCKErhiyHdUDxq5JDVwyFIM4GMSQ8YkiQUPRaChnNDk4ztiaaAqcZWzPfmrE10TxuzdjTgaAcYqcSksNuRhEXcifWKmMo6xTTeexoq5CdNXbmBP5IJR8pygTRfJeMxYLW5aIRBsWk7IcsUg595LLkWbYEzCNlzvf2qkA5xPUCKzYKJR6Lh9D5pTlx8xDGn1cCr0sBij5c+wBYd7hu5XWpI8xY/0L4/ujxk2433qZ3EbptyE/LUCWGRRuuL4fy+4SFAHqkMJO/Kjm0BLFMDLP1oe8Vlj1OLhtBRAGcmBzOTaVPimBg1DDKYf/RFDjN2Jr51oytieZxa8aeDnjl0O1M/NB3l4rvIDLYcaWdl9VZjmTbtgROnBTsZMvAjjxIRxCMANDUwHKYLpNohH7AEhbCeiwdHSl+8JJJFW5jtkMq5IuoLYe53GXvBTTL5fuGY2cxnPLhoDjm55idO2+DOegGeU3wWjHyHYX2tRfzWf1w6owHfp8h1sMQWLcdsnZA7WO8nYpnug7bky2FBSXvLxTtmb9zWBf3nYXwQ5ShVArzaQZKIeLIoIfwj0/S9xemUxRDepk1v9C6eLG1JYmATw6rBDEXRS8sjXOjHPYZTYHTjK2Zb83Ymmget2bs6cCs4t1lPkqEsZL6r9xwXtPhJes8M5zvIbbEKKNvfQZ28D5IHrDMlA8Xo00ONDolR6iQTEroF64oNgVyVMx+9UrZiBlTNSo5GSYWW54Dnk8YOcJnj/rVy3fV6F9dsO5g3WKBk+VYT+VooETWc187WcQjh2Jd0UawrYVJ269sz0NGFmU75/ZvjRISQy4oeIhPCu3RwLkONAI4mdfVWK+o8axD4bOZY6Ykh4Xw2d8rRHBkMATfZKNQ9BfNfGvG1sy3ZmxNNI9bM/Z0YJbsGHDEwAd2Pl6Giyl2emV0I4e5JGLnLTtrLANQBhifHOIjR5SRXFYQa91w8F+umXUoSTVESuIXuO5i+Kn3YnA/xeeXnQ/mIphDnodrgExUELGOOHVJzOdy6KmXLkVdtuq4px0QuRxaeNpaAGy38o+9VA5dQXQg2QuAAlhbDomOtBXzBSiCKIVSDqUkhsQQ32VYhi2H5YLoe3SMyJtsFIr+oplvzdia+daMrYnmcWvGng54HyuHcB5TyWkA+7FX2sHZy/xrzKLTzR+xIWJfua3TmZeAMuDD9+/P8sfQPM2h5VT8WGDk40uERw6lDDrbTJCJC1w1fvGcPHi+mAukyLeda4vseuE17AasNz6skUNBXn95isC2xXzRPmw5TMuwbTltEctabhtO23H1Y+VUED2Pjz1CWCaHJIBeQSyBHhXT1PxfZJrm4mg/QjZiiEIYAGUQ4cfK+MjYJZNDH7PTDsdA89lNNgpFf9HMt2ZszXxrxtZE87g1Y08HZtHNHDsGH/mohK9DkvMepNS5cOdXdIJ5Z9kSOPtBZyyW64AyIPHJIf9fZ55PRUXISC4wYpQrl0YhfiUjh2a9p4zLKxlQOcRzKTvParK8Dtu55fzzNbGuG17LErhuYH3xgXJo1U+us6IO+7Z19stY1IldLJd8lzBE1l6xHZu27JFDeR9wv1uYfZ8wA4Ww13LIYsj4fq2M8lcFvtAa6bkcziluslEo+otmvjVja+ZbM7YmmsetGXs6YOSQwQ7DhyOJoiOyEOvtjo9GROQPWeRoIj5GK75HWCaJsvOlZezEy5BSkJcFhQKkgxkWI1hie/dx83ClHFaB4mVREdvZvgb5vllsWe7bVu4zceyRWCmEMrdGAkM4185GXn+sE1VwvbN/NOKpk9k03c+t23bdZ9IylkNuP05bw3nYBtut1YYzOeQ2L6dBhqrFMCSHQfLHya4QFlJoy2HdkUJHDKUcyvmMlvNY2Y8jhCyFhFlviyERhaK/aOZbM7ZmvjVja6J53JqxpwOWHNaVRO58HCH0AR1cIYf4S2fsNP2S6HTGLQGuE/t0A8mFmXZDhZCkMtMykuU8Bs2lSIoRlldTJYfWtgK5jNvl23cRO0TV+aS5KMQPHw3jsiOEhBR4AK9zt2Ddykf3sO5ly8U+bn224e2KNrGwE9snfUHENtheEZJD2dax/ecyKOZRAoO0upND69fHQ4UU2nLIj5K7k0PrF8lzwpD01ZFDRwqlGDJz3A4nCkV/0cy3ZmzNfGvG1kTzuDVjTwe8clhHEE0nkyHnHUTnVnSAKIhyHjtOVw7pVR9M3hkTPJ9/lt2pY2cfguXQKqsilxPPugwSHpYsKUp+aXIfSVfRC4EL0bvY6XnxOWMecikcKc9lCsugi7xueC3rIuuRQ6eeyUe/Zh+qk944bn0upNDXHtLYpXIol8V6bKOIadvDhRzWxZHAEGJbRwYBa2RwqHzkkOUQBTAEvqomNHLI4lclh3JU0GF2Ct5cmSgU/UUz35qxNfOtGVsTzePWjD0dCMohgR1LFY4YMlYnZ3eGqTTiKKKvQxWdMCEE0erMWwKIiZ12CJ8cmnIxdSkftTKQ+HQ6fWe0S4iQd8Sspij2TuBcJhPbOj8mW8dTJxdin/oU++C1mwhW/eH6JOoXCRzWQblvOsV6XNTlFFcOqU04I4fYplqi3WXbYHtE8natJIckfCyHKIIIvr8QxVDKYfEDlHpy6EghM8eVwjpyWIhhWA7xxiqJQtFfNPOtGVsz35qxNdE8bs3Y0wHzKpuiE5DzWUcipt0SFkQb7hBR5grcThU7Y+6kWTAWDgegdSAjWBYUuAD5iFdJObO43Tbx0+URMV8Oi5b5tXOI0XYn/oiBy8x+chn3KWFxJx6WEUupnF7mbabtdFmu8+zDx5VDx5odrzlusVwG5QvL5Dokz3eXkPjljNjL46MpS+aNpvOh/by0xdSGhJAZHxu1lg30/5bpv7Jk0Hxd5tO08xk2VCYp1vH287P5MubJaWd7moYY6zBK0+GU0Rq0O+22ipEqWgXDHtojbaes5dAqGCoYqmC4cw5Y1ivouLCsV/hikxwNOnTcWNYrNGNr5jcU2/7DZ/DQPEaN2CxWcr6pzMK//vF9Zg74LrQM912J5e9NxFGQ2jijMPUof4eijRnxyZdp3k/+QmQCZZWBdSR6zjY1cEfJXCg2j5rJETTczmwL4HqEY3cLHosPEmkss5A5zK6Ptc5aD9do2L1uKe519+KpSwzJIJbl9c2Q/tETGvnzwe2DhA7bTNGuXLA9Ou3WasP1RgIlOPIXelchL1uPjOe67y30vbPQhzUqOMce/StIX2TtA0cBU+akzM6mHVpD1FGko4B1wBtpGdQJYVmv0OyENGNroplvzdia+daMrYnmcWvGng44cihxOhUCOyHsjLL5ouPCzq0HkkgdvkF0xi23gy7DJ4pclgqFXIdi4cKCgjFRXipFiBH71EXGRhnzyVoZZbEnhee8nM/LrkG+vSe/KIF+fNfSvtZY1k09ohFALLNkkKc1ke2ikEP7Dy7ZvoLtEdusaM9m2qovh7YQMvI/nLhyWCWFUgyl/PEylptHxR7xs+XQFkQWwcMPPyY555yLzPyZZ56X7LP3hmRsdCxZudOq5MorbzCid+IJpyXnnXepI4cbNmxJ1qzZ1czv2HGVme68eo25cc6bt8C5mYaIQtFfNPOtGVsz35qxNdE8bs3Y04GgHPqFUD5+lsvdPXrGjhA7SS9Zp1v/EXQYIwzDrqTkoifmLWS587kFGFfSK8lC0aP5bkclURhxvbVtIDbKZFUcH93u48s1z1vXqOxaivUYN5136w2SyqH9fVn8ykQtQcy2k20jPHJog+3P305BElv15ZBwRg1LaeXz8scmxfcHGVsCi/ku/ieyI4kuu++2Ltlt13VGDk877Zxk3bq9jBxu23Z+sn37Vfl3DY899uRUDnPSx0SXXnKlkcKNG/fLpfF1r7vGuZGWEYWiv2jmWzO2Zr41Y2uiedyasacDQTmU4CiEg+yAuGPK5rEzqwt3kk5HymAH7OmMuRPvZjSISH8FnS3TvhSrK+R+Yv/OsdF3G6XAoPhYsiLXV2xLeAWuxn6VtEjgPLHrkH1+nfM12zFOPn3zNTCx3GvcDUX94XqV1jP6niDWuRBYr6vwyaG/vXkQbRPbsmnPrWo5dKVvCEYHi1FD+QjZksIc/2NkFL8yymSQ5E7OS3bsuDrZa8+9zfzll78hueSS1xs5pO8YkhyS7F1wwY5k06b9UimcXXDxxZeb75gtWbLULB966FHmpkn74Y20jCgU/UUz35qxNfOtGVsTzePWjD0dMHLIN3/sIHw4YliF6LSws0sJlRdgR9sVouPGTj+EJYc+jKAgLCRYbq+nH8U4AmPt64tTbIMyJSE5lNt596uIkW+TUeyfxna2LcF/Lvb5+I61PA8YK0Dda1mBU58YOkf6AQaWZ8h62219J1gO85FAX7vCMgG2W6sNt9x3EfI0iBHB9FGy/YjYJ4f242OeovAR9H+RQ/8bue4IYfF/j105lOTi5/lu4VDn2LGMwZtmt0Sh6C+a+daMrZlvzdiaaB63ZuzpwCynE8g6iiqwMwpiOjfG7QRtacTvKbodKXbClQzDPIlIjisDxESEIhWc4ntr/h/AFJLlJ93GER2rLDt2Oc2Qsfl4bGEq1vkIj9rJ7+6JdXIfZ188BzwfiON8pj8O5jX8n0dSur+WxblUjQjWkUO7/ro/JMH6ndfzEXrdDLchjxyWgG0VoXiynWP795JJnh8WQlsOeYSQ5lH8pBj65LCeFDI6cog3y4kShaK/aOZbM7ZmvjVja6J53JqxpwNeOZQdx0TAzsp57GUIfU9RdpoVHagAlyvJOn9bbvgRYrdCUQHFzChGyexyV5x8yzzvp5BD3tYXty5yP3nc3YDnFjgfb2zYD3Nak5AcFte5qAteWmHMuwjFMtbPbuu1bB+2HGZAu5JtDdtgCNO2W8X3AisxI4Yprgx6GHJHDn2jhqZ8Tip5uRBmy1W4QugTQ7kuxSeFuRwOFXKIN8nJEoWiv2jmWzO2Zr41Y2uiedyasacDjhxiZ+LQsh9J2fInvwjP8y5pRxiSw3K4Ew523Ni5e5BCULyIW1L/pdxV4Oic+V4gvDTZ2qdVE7ktfxZ/nzEUBz9LbotlEMeRw8B21nwFfO6hF0kjzmd68clhObIedEP+oupWxrBbX7tBto1UDt22kyLbnBDGlmibch7g7bDt1wUfJTP0QxPzn07EciqC/h+XhOjmRyeuFIahzsAPyWErl0e8SU6WKBT9RTPfmrE1860ZWxPN49aMPR2Y5b6aQgCdAnYy3YCjHl2Rj7T4R1xScFTGHalxRDKAEQVPOYpAgT0i5TxWdmQFRbM3cGw8Bud4POB2cnszNecuyj2fP1FS8RNlGJ+Pc7js8/GapNcpeC1r4tanol75fjRSiF5R95z6LOq1b0SQMP//eKhoO9ie6mC1X2rnZjo3XWfaeFZuzUvh84wMZuSjf9k8Q//ZxFqG9Sh3dbFHB4vRQMPsDDlCKJntgjdCzU5fM7ZmB6cZWxPNfDc1dryWLk3NSb+YRTd6fmRkiSJ2LgB2RHXBTjAId5rcgQqwk3bBdf7tUARSGWiZjhnLKwEpSctckelKDmHfKrqK3SWTjk3nEjyf8thFDj15r6CuHGLdcOuTO2+/i7AA62tIAENQO6F/cYdtpy7YVlkKZduVMmgLYbkU4i+OWf6KqWeUcE4KCl8d7NE/kEKWwdlCCmeXQzc9nyDSyCHeHHtFUzs4zdiaaOa7qbHjtXRpak76hfNYuQzZ+WCHVAU/ykqFr+WKoIV8fDbxR9AhWAYcmcsICoUlfvXAR5jm357VemxdBe9T7N+9wMnPLt83HBuPP7SdDzyHcjC3Qepcy8B15XqBdcZH+cihD1/9FsvcNijGBOUQ26mP0HcO+QclPG//f+PydxTmj5CHaMqAJGaUPjLm8myKj4arSW/6/LjYTGe7koiCGOXQRTO2Jpr5bmrseC1dmpqTfjFLjhjkj54qwE6oG2RnaZXRlHFksVwSfWV1kIJglfuEQoqHT0aklAS2I8GxvhfopWp9mLDAoYyVCRnuk2LH5nnfvljWHTJXmD8rx578erfzXcuWWwewbtSheN2MXS7rqluPBdAe5PYTlUMC2yti5FC097z9D6VCaKRQlONoIj4qljKIj5W9UkjMqYcrfz7oRs/g9wkzZvulkIly6KIZWxPNfDc1dryWLk3NSb+w5NASRU+n4kN2RthJlZJ1hjSfd4w07wPkUCI7Y+y8JwoJhVtWglxP8xLYdsFI+Q8ffFKE0pQKJFOIVbV4+vbHWP4Y/ti4v70Nnod9Dja4jZeK3OK2dN3omJxrCcsTRY4cYr20wPps1e1iO9k+6sqhbHfYNsO0rHZu5ocKMcwF0bon2N81RPFjUA5JBC05nFMPVwDDVIohM9svhkSUQxfN2Jpo5rupseO1dGlqTvpFUA67lcQQ2Jl1i68TdSkXSAI79jK8cpgh561ln7x4qJJD3D6P7QGlqiq23B7lrErSZGzeru6+htA54fnJ9bgPgttky/a1dK9vN2A9kszvyGFR/+Q6UR9FHca6bWj5f1Xsk0NsW91StOlCDt0RQoZkMJ3Hx8ilDIEczqknhSR53UqhLYbZqKApQ9wbHxLl0EUztiaa+W5q7HgtXZqak35RKod5p+LpaLoBO7mJgB3zRMCOP4RPDqtguXHKJcMlAie2cSRIxC8jGLsHTDp2N+cTyENpbj3r0+vS/bVksP4ghRz6SOss1mMHsw1TlKMcYpvqBh4VLNp1IYeHHnxIsnnjJvOdQdn27dfRhB8VI/Q5zuNjOe/hzDPONNCLqFH+fPjkLzR6iDe8EFEOU4aESPc6dr/QzHdTY8dr6dLUnPSLUjmUj5ews8EOqAqnU+wWp/MVDNUZXXQJicBkhKIMEh5LsrIyS4Q8UmSBIiUwsXF73LcihrWN2Jcez1r7+uLg+hC4H2By1XLzNxFC19JXB2R5HcrkkOqsnO8WkkPZdrA91SE0Kijl8NVXX03+4Rv/4GxTfI+wvhyaR8hD9eWQZY+OgRhuDTsiWC6FQgxn2yOHeKOrIsrhnGT9wrEkuXB/Ay33MnY/0cx3U2PHa+nS1Jz0i1m+EQOLIZjnjmeu2xnVQXaAvrJyWo4kyvXOF/7z7Xi+nkBSx2wt95CQrHQDyhSTC1wd5L5yGbfLsGLL7VDqsmkVvH83+0wWvM7VYH2S9Wgol8O07qX7WI+J5XyXSDmcCPyjEqc9UzvvtCNu9yyHxQihlMFyMbQkMIO298ohTTNQ+nxyyGVhKfSIoecGV5coh3OS/ZfMV5NDivnCWZudcg00893U2L28lv0k5mTqmMU3enx3WQF0LDBvyDoi7KAmAnaSQWp0vM6X/5mgAKAcVIMCUkUv5DDEZGKzqIXol8BNBrw2fH2wzAavvae+eOoWQXKIZd2AdV8yVkMOud3JduhrpwVpm063S+dZDlH8CjnEMlcIpfgZORTLISGsguXQkkBr3hZDvLF1S5TDFHofJs/3MjbJ4e17r3LKNdDMd1Nj9/Ja9pOYk6ljFr+glv7Pqekw5LwAOwjTyYhpPYqODF/CWyBewi3nA8iOFjvfiUKSYC33gkxC5g1LIQHEds6+MgbAZanApdvylMm3NfPpdu7Ujsnb2vuU45wPgtuY/Tw5wf0mAF9Lnu8VXNfmZXKIddKLr147dZ/aRtpWSA7d9uNHtkFuq9h+c+ak7ZCmtF0qh99I23XW9lHsXDo37QyUP5JFFD38byb4WhkfuRxCOd7AesWgyeHPz9qcj+CVodnB9Sr2zet3qnUuvWIi+a5LU2P36lr2m5iTqSMfOQxTjDK4oxDp1DuaCFCnyNNeIDtqudwVLcIdgWQ5RNlg0QiPPPG8xB6pKh5Zu+vqgiNmjBw5LNtuInDsUFx5bHi8PsL7+PNmrwvn1+C7ZnCNewH/aATrH9bV2nA76ZDKYdpmWJSQA7ZutdpY/ng2b4/2H3b5+qFiRJDlcN7oqBOfeN973+vIIa+j+f/4j/9w9uHHw4ccfIiz7pVXXrGkkUb/eB3drL/61a86+zDPPPOMVxB5/TXXXOOsY/bcc698Oy7bunV/5zMIOifslL71rW+ZdU8++aQTmzjssMOd+D/4wQ/MMsXavn17vv4LX/iCsz/Cj3f/84L9k//vgq3JWzfu7GxDnL3LkuS/OtvtsWDULFP9++XZm5PvnbKvtd3G8XnJv5y2IfnNuVuSw5YtcOLQI+X/vHBrctW6FXmZ7DyXt4eT/9XZ/wenbjCfgfvvs2gsefGsTcnL52xJLly7NC//9OF75ufy6cPXJZ86bJ33GvYSvHa9pKmxmypCMSdTxyzrxu+IoZ/K0QkARzpSXIFMKUZU5HwOdqhdgJ17CBIKLJsMUlaMHEJZLRwpyhDrU8mC7cv2rYL3HQqM7vnA45bHj2X5OhA6QOYQc1tFL64l1iOmm+8Fcl3mOu7Wey5PGc1GDn/3u9/lUvHyyy8nzz//vCUyRx5+RN7OuAzbq2mrQurko19a/sdvftOKiZ/xtb/8mlcOmaefejp54IEHrLKR4ZF8/u67706+993v5su/+c1vrMfCXE7zVXKINzDi8ccfz7fBdcy//Mu/mPW//vWvzfLb3vY2KzaVv/zyr6wyuf9k5HDlylVW3DI5pDr+H+dvNTL1d8evz8vf0ZFDKiNJ47KnDtk9Fy8emZPLq8dGTNld+65K/vGkffL9fnfefslbN6zOl7ftvNiJQ3Dn+Zkj1iXfPzWVza8cs5czCnjcykXJPVm8M7JYa+e18/UYVxtNoRi0Eea6NFWEYk6mDlsOEU8n0y1hOZSSiGVYPlQtiHPF42fcNrBPSAJ8o4m9IiQrZRKE60IYgfOUO0jxq5K6jNqxBXiO8nwsFEf3QvnG6491w1uXoF55vxeI283F+m3X65AcUuzNGzYYmaCRLBwF3GvPPXPZ4DJcZlDqUA6ZlTvtZLX/7ZcWo107r1qdj/ZxGQmVfHzcHimE8Je//KWROfnfS9auXZuvr3qEzGV4w/JBN/k8xhz/DZ/XL1++wnQ4vPypT33arOdOn/an0U1aR3nn/Scjh//+7/9u9sd9ELqHnb56PLl63QqvTEnJojry1CG7meOlMho9vG6vncy6Jw7c1ZRR7t+wl/tI99RV41bZf5y/nxOfoNh/c9x6q+zPjkpHAnl5r4Wj5rN5mT5Trqf6R8t0XvIYNNEUiiiH/SXmZOool0MBdjiWAM7J6HSOZeCPVrr7IQv9P9iC4t1wxf+JxXfF8a+b82War4H5LhmU8SNLGi2aDPQjBiybKOZRr1yuiM3bm38pVwLuRyxot018+q8ghJyXUPkgQNeQmN85bp7vGk8e5g1n5Z31C8fGsu0yRuizGLnsie1hTMzPHx1NnnziCSMX5597bjLaKUNYRpYsGreW5Tbt4YJifdspO+O0061tCRr9kyOXI53zJnCZocfJzz33XL5+OCuT8LrLLrvMLLdEGc0zvrIyePt3v/s9zrq99nqNFe/FF1904rfbo954mzZtNsvf/va3zfJHPvIRJz5x5JFHOTFZDrs5D+J/nb7RCBWW3781lb7RznV54ez0uIY781T2lWNfk/z2vP2cfWjdHx+2zltO1/iTh+1hlcnPPX3NUuc4cBtcj2V37LvaLFPdxu00IHkb6dRvmmqgGZuPXwMZm4SrKdBxY9lEIRmUUC6wrOmg4E2G2nJooFEIjxxaggjgdgz95SsfO1ePMIZGW+SoiztSYyQ0m1aS7S+FMwSORPlGobCcCI1k9YKmxu6Gstx6t2sFriVdayzz4dS/rF7NzUYOnXpo10ccEURkvZcjg+1O7LvvutuIxWOPPea0sXxZ7MMi4rTbjFxU5rojh7gtjwau3Gllvg3/qCRfnp0uSx5++GGz7re//W2CvygmfvjDH5r1H/vYx/ObEMeTNyZfWRlHHHFkcB86Fir/sz/7Myv2woWL8m2oo5D78KN1EjxanszI4de//nVn+zJYwLCcHgVTOT1a/pOO1FEZdQhU9sp59P1Tu3P49blbvHHoOlD59t2XJr85Nx015M/95KFpXF7+2MG7WftS2SW7LjPzPz5zkzf+c2dsyudDx6AJXsteohmbBAbLekWvxaFfxJxMHbPyXxn2CJRAH/idxDpgp5q+wsNTnuPvqPGRX44QAiMXprymVFYgpUVTspoaOwTm0QDXqorSODVw5a5YrvpFMdbhuhg5pJGQuYW8fe5zn0sWzJuXtiFqZxmy7fG22Cad9XPTZWr3tPyzn/3MejwsfzBiyWBWxss++bvl5lvMuhdffNEqZ1iYPv/5z+c3IZSqUFkVvE+7XXzfTZaPjc0LxsZO/4ILLrS2m4wcPv300872ZZBM/dVxr3HK//SIdeko3FDRYX6iI3NURt9TxO1D5bvPHzXrrt1zhbmeVLZ4pGXK9l40Zpav9zyO/s7J+yTPHL2nFX+/JfOd+BLaBuNog9eyl2jGjiLkEnMydczCv/wl3KlMRh5RDJGy0UUf3OnKDhg7ZRtf5+6SikC6DcmD3McRC4T2z+cDP6LJpsGRrJqgQElI4OR2vn2rYvj2M/tkseU2uF9VjBDO9jKfvIzgPoi5DnNNbKwT8lpjPXDB+lQQkkOWPJ7HOlwHkkN+rYx8tCs56IADrbbG5dgGWfby9XNZ/NKyb37zm/k2ZXK4YP6C4HcEq+SQbziacvjQQw85+916661mmX4EUxYbO30SSbndZOTwqafqy+GO3ZYZmZrfcjtFn2j5yoinDt7NW0585MB0Hf1xEYpD8y+ds8XMH7Niofle4crR9AcuxOePsL97GIK2uWDtEqdcE7yWvUQzdhQhl5iTqSMbOWQhxPnJiSGCHWC3yNEV7IixvB4oAqkMkFzI7RwxkXhlJhUTS2yydaVyKOPAfnUojT1JJh275HwcOUSsXIvcljFXXkt5PeUyXntfOdaZAv5FsRRBCdbfbhjJRg5N28mmRx95VPI3f/M3uYQQJHbcvrgM2x2O+KEc/vSnP7Xae0gO53b2m4gcyhuOphz69uMfl5x44knBbQjs9I8//nhru37JYehRLUHlr55vjwSi1DHPl8T5rwvTX0NjnP93QRGb49Ivpqm+YIzQ5yK0TXvI3V8TvJa9RDN2FCGXmJOpI3+sXEXe2XCHVQfaFsBOsAx/B2u/Y9GmeN9iCNPh58IA8xm5UNBU4AjIBJi0ZGX4hKrb2DKGL569bTh21b5TAV/XfF4C1ztUD7DuICSH6bysf6F6W12v5TLJIbYd2bZoPcsIl+Eyw204X9/5LCzD9s7Q9/J4G/7Sc7FMN1hbDm8Wcog3G0JbDvn7hWeddVYwDpfxY2YCO31+9c2PfvQjs/zss886xy3Ztu0s57MmIoch6bpmXfoL5l3Gikfm/Cj4q8e6j6BDcULraPl/HL2XtbzV88j43s3p+xZ9MQj6Y+KiXdP3HNKxym3eIl6fowley16iGTuKkEvMydRRWw4tuKPydFpesJMD3I7SB/7vV/w/sIUcYicfwvoltSinX0PjtiQPvJ0jIQCKiqRbgeuGpsaeCJhrax6um3MtAawH+bJn23yfuakcFvXPrY8ofH7sbbhN+OQP4fW7rl1r9uHl9kjbbbNie58cbty4MS9jCSS+K95P6MjhbCGGc9Ib7VTL4bnnnmf2I0l89NFHzTz9CEZuwwL5i1/8Ii/DTp8//8wzzzTL73znO80yjUTiZxL06h485onK4R+JH4XI8l9nj3kZ/g4ibkvQtr511+2ZSuZrFqbfLST2WTTPlJFsys87cKn7suzPHL5Hvt4X/9PZeoJeui23+ddtxQ9VNMFr2Us0Y0cRcok5mTpmUYKwE+kW7LQcRKdXB7cDxc4U8Xe0soxHdrCT9zHaKv47RS4DLA9CJFAoQiKSrxsqJKtKIieCpsBpxpbkOeT5ITvPmNcQ+XYe0ffFQngU0K1PBfSLYrcuyjqJ9bMA6zxCcviTn/zEyMV3vvMdt03NcUf9WGBISrCNXnvNtfn2PjkkpBQSy5Ytz9cdcMAB+Uhhvr3nhtJrOdy2bZsTowp5TgS9DkOuHx9fnK8755xzTZns9F944QXnmJYsWVqc9xy7UxkdHbM+j8u7lcMN42OZlNkjdqFHxPQ9QF858amOpPnWUdkr59uPpuk/n+C2tHzDa9L3JjL7jhdCGZJD+QMYOr7HDtzVzNP/bqdRRV5HOab3ZBLz57sSOhk0BU4zdhQhl5iTqcPIIYIdy0TwyqGcLyvzYHeuvo6Yy3Hb8H4siywC+XcMQQ7NepAOS0Z4WeyDmHWdbdqdmySKTC5FPI/7w3YoVIymwFXFlscvy0zOCDgn3M+bX18OxTzm0ULkDj87hb8nWGxLU7ueYP2xSb8XWLZPuox1uQ70DkApgMRXvvKV5N3vfFfyT//0T3kZvoiay1966aVk7/V7Jxv23ZD86lf2f/4gOeS2Tss8wkbQi5/vv//+/JUzBHXk8vExl+PNhOiVHH75y1+2jpkI/YcUhD5b7ofrCcql3Oa//bc/ST75yU9aZdh5yH8VeMMNNyS7776H+c4nLb/lLW91Pq9bOXz2+L2NcO06v3h0TP+KzidhREjQ5Hq5/PwZG60XVpfF4TL+A4B+jCLF75ED0ncu0ku2Q59Hy7ftvdK7jl4MzvmKcpgSRcgl5mTqmJU+EsqQ8zm9E0YCRz9q4+lACdn5YuddjU8wqdNvOduyRMgRSCzj75vhDxcKSIjckSw/6fY+pATJssrYKF8cwxMPkbHz7aSMleybwucTPq9iPW6LefR/x5S2ldeErxtey2rq7ZP/aMQH11msx0hgG/7/xAT92zwpLcymjZuc9kXgdgR9FUTOc3un5R07dpg2TqKJ++26q/2eO4LXYTnRKzkkDjjgQOtY6sohwYJ4+eVXOOsY6ujxfInPfvazzrbMxz72MWf7xYuXJKtX7+ycR7dyyEJGfOKQ3ZJfnbMlOWuXJc52xKbx9FHwzuLf1CELh9PvJD60/1ojhacF/ksJbfPX4l/1EYuyfZlb16eSJ3nvll3y9fxfViR/nf13lf8SP3Rhohy6RBFyiTmZOlI5DDGHRxPlfG9HGAnsGL1g54sdMW8D28rOGzv3ED459ElkUV6sl48icZ5EhSWLZSYsRRJc76cQONy/et8w6b5mlM+KURUPP7vecdiyHc6nfU18ZPsM+a5ZPZx6xmR1zPujEdgmn68A24SUw27ANlq036Jdm+3yNi7berqMN4luGJQbLopaFZqdft3YJFJ/7Pm+YRmTzffJK+1/pSeZbOypom6+J4Jm7ChCLjEnU8csnnHEkOGOxBFEXHY7ql6BHam3I67LXFcCWAR4fnjIJ4dV1JOQNHYhMShBPPpo7QPrcJSMxaoQuBByvStm9nogi52OjPJ29nHwOpQ6BOVPxim2q5dPe3vfPr6yAqwPvFynXuVymNUrZx+xjHW6imHzHS23HME26JK1XdGmzX55+3ZvCpOBPhPL+s2aNen/cJb/G7kKzU6/Tmx6ryFJ2t6LRp11ZUw23984IX2UjeXEZGNPFXXyPVE0Y0cRcok5mTpyOUQcSWSsjkV0PiXgexMniuxosaPuirIOfU4qcI6AZtIwWdKRrHJhqYcrUnKUzCeZuE4KGosZ7pNv6xmBS7fF83G3q6J3ObFJr9mQcx1919wq8633QALn2xbr7URoDRVyiO0pTNY2zT6inSJz9G6KmrGrwMe9S5em/+atDpqdfp3YPz/L/6OTKiaS7wXixyHmsW/gcycSexCok++Johk7ipBLzMnUEZTDEE5H0w1OZ8biWGDJ5OxuxFJul+5XdNbFfB2MHHrKJ0UmLD7J8sH78XKd/yRjvvsntuV5uS/KX4j8//jy/ATkTX42no+1nScnPunyllVg5NBT3g1YR7me1R3dy+tkVp/L6j5Dcmjmud1gW6oA263Vhufo3RQ1Y1fBUkivqjn++BOc9WVodvp1YvN397C8ionkmz7n9+el3xGkefpuIm5DTCT2IFAn3xNFM3YUIZeYk6mjazmsC3ZWDtwR4rwH7ETdjpc7cJ7ituH9fBLQGkpf9YGS0AsmLSsoUWKdjO2uK8pQxBDnM0Vs8z99PfuU7VvFpHNSgowtrzlfa1zngvWpqEu2HOL6ou5hfXbaACPWGTnE7Wfb7QvbGrbBEJo3Rc3Ymmh2+lWx37phdS6Hf37Untb/Tq5iIvmWInr7Pquc9cxEYg8CVfmeDJqxowi5xJy49Ou4VeQQOzS3I8RHZfg9KRu3w9YhF4qhHsoKCZMgjw3lk4XETI7A4Xq5HRIql3EwJq6fDM6j37L8YH6rqNgH60A3yEe/VWCddrHbA3VCPmnsVgR9UHws6xWasTXR7PQ1Y2vmWzO2Jpr51owdRcgl5sSlX8etIod1wM5OAx7BkfOl0HYdSFbcESCJrwzX8zbFPMlI2SgZbSfnGVwXwo1N+zDu9vWhnGBZNXYOi3Nx8MR2c+nms5o5JrY3Rs06gXUqZw48+u0Bsn1odkKaNxfN2Jpo5lsztma+NWNroplvzdhRhFxiTlz6ddxTJofdgh3ppCkRAfOS4NmZQBCebV1QQnyQCBX/ncIlFEeWFdvbEsWx0+18csZlKGII7mf2ySWrOFaUubDUIXjc9nKxDe7XBdm1M8eUzfP1pfVy3iwzWd0oG7VjQo9+EazLddDshDRvLpqxNdHMt2ZszXxrxtZEM9+asaMIucScuPTruGeuHDIeEWA5ZBzxKIO2l1jrpRziumIbd71cRpEqSL8r6dsH47r7utjH5QpcHewY/mMLyWEAb179pNdurv+aY9kEiHLoohlbE818a8bWzLdmbE00860ZO4qQS8yJS7+OuzFyiHCnix2x7JCxrC4ohzk+qaAyj5QQhaAUyNG9SmDfKrxy6I3BAoZTH+m60IhiV3iPhcXTLWdkDvO81sQrh5NA1ivqKLis12h2Qpo3F83YmmjmWzO2Zr41Y2uimW/N2FGEXGJOXPp13I2Vw7rIzhs7+hBdyaFcV7Y+24b+dZmUGyk9hJx3yjLZCY2ySTk0+/H+Ik4KxgjLGe9vtrFilMfJc8FTOB83jv2ZdfMZJP+sicsh1iVEs6PQjK15c9GMrYlmvjVja+ZbM7YmmvnWjB1FyCXmxKVfxz3t5bCMkAxwhcT1k4bkZ272y1TPunyK63FdACm1uWTJGFmZK2duLDw+I1mwjXe/khjOseRx3NjOPhNEyqG8pnh9sW7UQbOjqBN74cJF+by8YQwFXoXSbo852zILFixMxsbmO+Xd4ouNlN3w6RhHRuz/F8wxh4dHnO27oezYON+t1rCzrppwXKLOtZRQDkL7hHLDhParwrdfN7Fx26mk7Dgni2bssnYxWQbp+nRDzIlLv457RsthCFkhUTYmC8XGMi8oSChPHokycshlcj3uMwFygauKh+eBx+JhMqN7lUBsvNaTQbOjqIr9+OMfN9N3vvN9Zrpo0Xi+bmxsnrM9sXr1LmaKN5e7736HES/a75prrnf26waM7WOvvfZ2yhg6Rj43Zt26vcx0yZKlzvbdsGLFSqeM4XxffXV350/nO3/+QqdcUnYtH3vMPleCcnD00cc55cTy5TtZyzLf69fvk5x//sXOPnU47bRtThley/nzFzjbMGXn2G80j0UzdhQhl5gTl34dt5FD04FOQ6hiTQQaPcCyMkjK6KZhpmXQfzCh/8fL29LUkK4zZNuV0zLHiAwP8zytLwP3xTJeLvZJY8v9fbFwXRnFPpSTfJnOjc8vm6f1QTpSQ9jH0R/a7VGnrFdUxb711juTNWt2zc//vPNem+yyyxozf8ABBye33HKXkaprr70x34aki+SCJInLiHvueae1zeLFS5MTTjgl+ehH/8iMKB555DHJUUcda+TxPe/5QHLhhZfk21999RvN9B3veG9y7733J8uWLU8+/OGPmBhUvmrV6mTevPnJ6153ZTI6OmbK9tlnY3LMMcd3xOhjnfiL8lgkH4888lFzDLS8334HJKeeeqaRHlq+8srrzPTww49KDj74sHy/j3zkD5Odd16TfOhDjyVLly43udm27Rwzf/nlVxvRovXvetd9+T4nnnhqPk/wvtdee0NyyilnJps27Zfsu+9Gk+Mbb7zNCNspp5yRHHHE0eY4aR86r512WtU51yXJ3nvvm+flnnvekezYcUUee8uWrcmuu+5uykni99//oOTYY080o4BPPPF0R3qXJeee+1rzeXTdSRiPO+5Es+8++2zo5Dg97zR2eq3oWt9551tNDFqmfNOxvfa1lyYrV65K3vrWd5vyk08+LdmwYXO+/333PWSu0YMPPp5cf/2bTNnDDz+ZnHnmOSbfF1xwsSnbuvXA5Oabb092331Ps57Kjj/+xOStb3lXp2xd57runLz5zfd0jmOtOSeqV48++jEj8O997wdNLLpuDz30pFN3talqO5OhV7GLe38B5RjLekXoM/sB9pfdQMeNZb1issdGoHNI98CyXqEZm8nlMGJDyceyXsGJx4sRGukqyhn3QjL5yKEc4bOmtF11HGckcI4Y3bO2gf2c9SIGIvZLRyULMGeTodfxJHRzwbJeUSc2nduTTz5t5nnkkASMOuZbbrkj345HtnhEDnPy9rffm88//vhTRghp/h3veF9HWDZZ237gAw8bqCPjWCQKt956R/KmN91plq+99qY8BonI8LD9KJRHDkk6+VE3QaLDcnjyyWfk5evWpSOHV1xxrZmShN5//4fz9SQlNH344Y/kx0efTwJEgkvQehIZmpJwPvnkJ6xjesMbbjRTGjk86aTTzDxJJ03pnOSI3V57rc/naR3nl0dmP/CBD5tj4Mf+dLw0pWt6wAGH5MdI58sjhySnt912j5FIKuORQxIzHh0maJSX54844hjrWsqRw23bzuvEH80/i7cZH19i8rVixarkjW+8Jf8MOXJI15OmBx10qJmeccbZZkrHdMUV13SO9XGzfNFFO0yOaZ4E+brrbjLzN910m5Frmv/gBx/N4/aLOm1nomjG7ke/0zRiTlz6ddxRDj00tULicXuFTM6HwP0odlaOn9kLNHOiGVuzo6iKffvtb+nIx3guFz453LBhkxnR431YDleu3NnIDgvP2WdfYASM9tuyZX9LDqlO0WjSpZdeZnJJ8nbjjW+yjuXBB58wsnjbbXd35GNxRzaeMH/x0whhOnLpyuH27VcYEaWYxx57gonPcsjCe/rpZyWXXXaVI4ckKYcccnger5DDJ438vO1t7zFSQiOBJIavec0+HXFbk0vS+9//oJGwe+99II9B84sWLbbkcHx8qRk5pHWUKxqFJPmSdYqEE+Xw0Uf/ILn55jfn26xdu1uy557rTZy5c1tmBPLii19n4pCk0v4U/5JLXmdGGema0sgdjUySiErRL5NDuo5SDmlKo3+HHnpEvg3liOoKfQbFppFblkMaZbz++lvzbX1ySCPHdM5r1qw1eV62bCcjhgSNElLsO+54a5TDCYD3716ieR/UJObEpV/HHeXQQ1MrZFOPu6mxNTuKyca+8so3OGVM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X59eP8L2/eeff3/8c680abq+9s0tixadNn690pgffPCZ2VI7bP1BBv82cFQOe0ubfdJm7Db7u83YHJVDgUEdNIPa7n6IjRPEIMLlkLavvvpWcv/9j5j088+/YrYkArRdv35TsnHjOSb9yitvGjmk9K5dd5syJCbf+lb6Srorr7wuefPN98fF6FyzT/LxxhvpK+Rmzpyb3HTT7clHH33b7JN0ffHFD016796HzdZKDklTmv/QuFyuMmkrSHffnb5Gj6SPtlYUrYx98smXRg6PHv3c7D/33Mtm+/DDj5tX69nPRZx//kV52raTzv3220dM+swzz05efPFVkyZxtAJneeihx5J33vkw33///U/Ne5hJoHbs2GnyVq06Pf+c1OZXX307j7d58wUmvWlT2l8k348//pxzDoI+O8UmaJ/iU99SmsT9rrvuS44cScXro4++yOtdcMFW0w/PPPOS2f/61/cnq1ensvjOOx/l4mt5992PzJaE/MknnzdpEl17nP4j8MQTaf599z1k+prSdI0+/bQQWJJD+k8Fpe31mTVrnpHDBx7Y55xzkMG/DRyVw97SZp+0GbvN/m4zNkflUGBQB82gtrsfYuMEMYigHJIYPfLIEyY9dWoqaPa9xO+//0myYcNmk+ZySCtPVrRo1Yi2O3feYuSQ3itM+7RKRun585cY4SA5tJK3devl4+dPRcbGtHJoV/5ILKwcHj2attWubKEcfvFFKqgkYiSrNiYJHC9/1VXXmS3xrW+l7abP+sILB/NzHzhwyKRJ3kicKY1yeOmlV+ZpC8mbXRWjz0dbkkPbP3Se119PJZTLoV3dozZSn9r3Q1v4yqEts3z5arP/6affHRe9o7l02z4kSABPP/2s/LPdeOOu/FySHNK1o+3ixctyiVuwoGgLyeHevel/Iqgd9votWbI8KIcXXZSuJNP1p2tj+2IygH8bOCqHvaXNPmkzdpv93WZsjsqhwKAOmkFtdz/ExgliEKHJnLZ2dejhh1OBOnDg9WTlytPzci++eDC/xfnyy28k99+/L7nlljvH671gVhOtBNrVObotbGN985uHjEBcddVOk6Y8uu1KWysrFIe2FJO2VuDs+ZYuXZlLhl2xsrLBy9L5SWCpvSSgd96Z3l599NGnjZSQ1NI+rR7ylTm6dfzYY88kF1641dzytuWmT5+THDx42KRpFZSEkW4n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>