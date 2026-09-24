# Hackathon Project Selection Report by Codex Luna

## Summary

Based only on:

- `hackathon/3.Product_Ideas/Product Ideas for Accelerator.md`
- `hackathon/4.Vibe_Coding/Product Building - Playbook.md`

My recommendation is to build the **Task Management App**.

It has the strongest balance of:

- Clear and painful business problem
- Demonstrable AI value
- A realistic three-day MVP
- Simple end-to-end workflow
- Strong relevance to productivity, operations, and enterprise use
- Lower technical and safety risk than health or finance products

The winning positioning should be:

> **Turn messy meeting notes into verified, assigned, and trackable commitments—so teams do not lose important actions after meetings.**

## Ranking

| Rank | Project | Assessment |
|---:|---|---|
| 1 | **Task Management App** | Best overall chance; clear workflow, practical AI, strong demo |
| 2 | Resume-to-Interview Coach | Strong personal value and compelling personalization |
| 3 | Campaign Planner | Broad appeal, but crowded and potentially generic |
| 4 | Collaborative Notetaker | Useful, but real-time collaboration adds complexity |
| 5 | AI Interior Makeover | Strong visual “wow,” but dependent on image API quality |
| 6 | Personal Finance Manager | Useful, but requires trust, accuracy, and sensitive-data handling |
| 7 | Pet Care Companion | Friendly concept, but weaker urgency and judging impact |
| 8 | Personal Health Manager | High safety/privacy risk and difficult to differentiate in three days |

## Recommended Project: Task Management App

### Core MVP

The user should be able to:

1. Paste or upload meeting notes.
2. Ask the AI to extract action items.
3. Review and correct the extracted tasks.
4. Assign an owner and deadline.
5. Track tasks on a simple board.
6. Mark tasks as complete.

The complete demo flow should take approximately two minutes and work with prepared sample meeting notes.

### Why it has the strongest scope

The project follows the Playbook’s strongest principles:

- One focused end-to-end flow
- A clearly defined primary user
- A visible AI transformation
- CRUD functionality for the main entity
- A measurable success outcome
- A natural 3–5 minute demo

The AI is not merely generating text. It converts unstructured information into structured, editable work. That gives the product a stronger platform and workflow story than a basic chatbot or summary tool.

### Suggested differentiation

Avoid presenting it as another generic task board. Position it as:

> **An AI meeting-to-accountability system that turns decisions into owned commitments.**

The differentiating feature should be **reviewable extraction**:

- Highlight the source text for each extracted task.
- Show confidence or “needs review” status.
- Require the user to confirm owner and deadline before publishing the task.
- Preserve the original meeting notes for traceability.

This gives the project an important enterprise-quality characteristic: AI assists the user, but does not silently create authoritative commitments.

## Recommended Architecture

Use the stack already suggested in the source idea and playbook:

- Front end: Bolt
- Backend and database: Supabase
- AI: OpenAI API
- Core entities: meeting notes, action items, users or owners
- Main screens:
  - Meeting notes input
  - AI extraction review
  - Task board
  - Task detail/edit view

The architecture should remain intentionally small. Do not add real-time collaboration, calendar integrations, email notifications, authentication complexity, or external project-management integrations unless the core workflow is already stable.

## MoSCoW Scope

### Must have

- Enter meeting notes
- Extract action items with AI
- Review and edit extracted tasks
- Assign owner and deadline
- Save tasks
- Display task status
- Mark tasks complete

### Should have

- Source-text reference for each extracted task
- Simple filtering by owner, status, or due date

### Could have

- AI-generated follow-up message
- Overdue-task indicator
- Export to CSV

### Explicitly exclude

- Real-time multi-user editing
- Calendar synchronization
- Email and Slack integrations
- Complex permissions
- Advanced analytics
- Autonomous task creation without user confirmation

## Demo Strategy

Use a realistic meeting scenario such as:

> A project team discusses a launch, identifies blockers, assigns owners, and agrees on deadlines.

The demo sequence should be:

1. Show messy meeting notes.
2. Click “Extract action items.”
3. Show AI-generated tasks with owners and deadlines.
4. Correct one intentionally imperfect extraction.
5. Publish the approved tasks.
6. Move one task to completed.
7. Show the remaining work grouped by owner or status.

The key judging message is:

> “We do not just summarize meetings. We make commitments operational and reviewable.”

## Risks and Controls

- **AI extracts incorrect owners or deadlines:** make every AI result editable and require confirmation.
- **Demo API failure:** prepare fallback demo data and test the full flow repeatedly.
- **Generic task-board appearance:** emphasize meeting-to-task traceability as the main product identity.
- **Scope expansion:** freeze the must-have flow before building, as required by the Playbook.
- **Weak user proof:** use a concrete team scenario with measurable output, such as converting one meeting into five confirmed action items.

## Final Recommendation

Build the **Task Management App**, but narrow it to:

> **AI-assisted meeting notes to verified action items with ownership, deadlines, and status tracking.**

This is the strongest project for a three-day vibe-coding hackathon because it combines practical value, visible AI transformation, manageable architecture, and a reliable live demonstration.

The main success metric should be:

> **A user can convert one meeting note into at least five reviewable, assigned, and trackable action items without getting stuck.**

### Assumptions

- No official judging rubric was included in the two Markdown files.
- The ranking therefore prioritizes problem clarity, AI usefulness, three-day feasibility, demo reliability, differentiation, and platform architecture quality.
- Only the two requested Markdown files under `hackathon` were analyzed. The other project folders and files were not accessed.
