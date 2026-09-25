# Task: build an interactive frontend mockup — PlanPulse

Produce ONE self-contained HTML file (inline CSS + JS, no build step, no npm).
It is a clickable prototype of a team task-management app, used to validate UX
before real development. Open it in a browser and everything below must work.

## Product
A Kanban board that computes DELIVERY RISK, not just status, and re-plans the
week in one click. The differentiator is a Risk Radar panel beside the board.

## Visual direction — dark "mission control"
--bg #0B0F17 · --surface #141A24 · --surface-2 #1C2431 · --border #263141
--text #E8EDF5 · --muted #94A3B8 · --faint #64748B
--accent #4F8CFF  ← primary buttons ONLY, never for status
Risk scale: #3FBF8F 0-24 · #7DD3A0 25-44 · #F0B429 45-64 · #F97316 65-84 · #EF4444 85-100
Inter for UI, JetBrains Mono with tabular-nums for all numerals.
10px radius. Elevation via lighter surface colour, not shadows. Information-dense
and calm. Every colour as a CSS custom property on :root.

## Screens (tab switcher at the top to jump between them)
1. Sign in — centred card, tagline, and a "View the demo board" button.
2. Dashboard — project cards with a small health number and a left border in the
   health colour.
3. Intake — left: textarea + "Use sample notes"; right: a 4-step labelled
   progress sequence (~800ms each), then editable AI-drafted task cards, then
   "Accept all".
4. Board + Risk Radar — the main screen. See below.
5. Settings — members table with an editable weekly-capacity number input that
   recomputes the board live.

## The board
Four columns: Todo, In progress, Blocked, Done. HTML5 drag-and-drop between
them; on drop, reset that task's status clock and recompute all scores.
Task card: 3px left border in its risk colour, title, then a metadata row
(assignee initials avatar, estimate, due date, days-in-status if ≥4, risk score
right-aligned). If risk ≥45 add a one-line plain-English reason. If ≥85 add a
slow border pulse. Clicking a card opens a modal with full edit (title, status,
priority, assignee, estimate, due) plus a breakdown of the four risk factors as
small bars.

## The Risk Radar (fixed 344px panel, right side)
- Semicircular SVG health dial, ~150px, stroke-width 10, rounded caps, animating
  strokeDashoffset over 1.2s, with a 34px tabular numeral counting up inside it.
- Three stat chips: blocked / overloaded / days left.
- "Biggest risks": top five tasks worst-first, each a clickable row with a score
  badge, title and reason. Clicking scrolls to that card and flashes it.
- Load bars, one per member: assigned hours vs capacity, over-capacity in orange,
  with a tick mark at the 100% position.
- Full-width primary "Replan the week" button at the bottom.

## The risk engine — compute in JS, never fake it
Per unfinished task, each factor clamped to 0..1:
  S staleness      = daysInStatus / 7        (0 for Todo — it hasn't started)
  B blocked depth  = transitiveDownstreamCount / totalTasks
  L owner overload = max(0, assignedHours / capacity - 1)
  D deadline       = max(0, 1 - daysUntilDue / (estimateHours / 6))
  risk = round(30*S + 25*B + 25*L + 20*D)
Project health = 100 - (0.6 * worstTaskRisk + 0.4 * estimateWeightedAverageRisk)
A project is as healthy as its worst problem, tempered by overall load.

## The replan — the demo's climax
Clicking Replan:
1. Button → "Analysing N tasks…" for ~1.4s.
2. A diff modal opens: the before and after health numbers side by side with an
   arrow, then changes grouped into "Reassigned" and "Rescheduled". Each row is
   a sentence plus an italic reason drawn from the data
   ("Priya is at 167% of capacity; Sneha has 12h free").
3. Compute the plan in code, not by hand-waving: move work off anyone over
   capacity to whoever has the most room (never move in-progress work), then push
   out any due date that cannot fit the remaining hours.
4. On Apply: run a FLIP animation (measure rects → mutate → animate transform,
   420ms cubic-bezier(.2,.8,.2,1)) so cards fly to new positions, the dial sweeps
   and the number counts up.
5. An 8-second toast with a working Undo that reverses the whole thing.

## Seed data — tune it so health starts in the low 40s and replans into the 70s
Five members with capacities 30/30/20/30/15 hours. Fourteen tasks: 3 done,
4 in progress, 2 blocked, 5 todo. One person carries ~50h against a 30h capacity.
One in-progress task has sat 9 days and is past due with three tasks behind it.
Eight dependency edges forming two blocked chains. Real launch-project titles —
no lorem ipsum, no "Task 1".

## Requirements
- Responsive: below 820px the radar stacks under the board and columns scroll
  horizontally. 16px side gutter at every width.
- Every number that changes animates rather than jumping.
- Respect prefers-reduced-motion.
- Keyboard focus visible everywhere; risk is never signalled by colour alone —
  every coloured element also carries its number.
- No external dependencies except Google Fonts.