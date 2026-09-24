## Recommendation

Choose **Resume-to-Interview Coach** — but position it as an **Evidence-Based Interview Readiness Copilot**, not a generic question generator.

It has the best winning profile for a 3-day vibe-coding hackathon: a clear user pain, an easy-to-understand before/after story, contained data model, credible AI value, and a reliable live demo. It also avoids the operational and trust risks of health, finance, and collaborative real-time products.

### Why it is strongest

| Criterion | Assessment |
|---|---|
| Problem clarity | Excellent: job seekers immediately understand the pain |
| AI necessity | Strong: resume/JD analysis and tailored feedback are natural AI tasks |
| Three-day feasibility | High: upload/paste → analysis → practice → feedback is one focused flow |
| Demo impact | High: judges can see personalised output change in real time |
| Technical risk | Moderate and controllable; no real-time sync or image-editing dependency |
| Differentiation potential | Good, if evidence-grounded rather than generic |
| Portfolio value | Excellent for an AI Generalist / Platform Architect narrative |

The playbook repeatedly prioritises one complete end-to-end journey, full CRUD for core records, one “wow” enhancement, scenario testing, and a short live demo. This idea fits that operating model unusually well.

## Winning MVP

**One-liner:**  
For job seekers preparing for a specific role, we build an evidence-based interview readiness copilot that maps their resume to a job description, identifies gaps, and runs personalised practice interviews with actionable feedback.

**Must-have flow:**

1. User pastes a resume and job description.
2. Product generates a transparent match map:
   - skills/evidence found in the resume
   - job requirements not evidenced
   - interview areas to prioritise
3. User starts a tailored mock interview.
4. User submits an answer.
5. Product returns feedback tied to the job requirement and resume evidence.
6. User saves the session and receives a readiness scorecard.

**One wow feature:**  
“Evidence Checker” — every interview question and feedback point shows the specific resume evidence or explicitly labels the point as a gap. This makes the AI feel trustworthy rather than hallucinated.

Do not let the AI invent experience, achievements, or missing skills. A visible “not found in supplied resume” label is both more honest and more impressive.

## Ranking of the supplied ideas

1. **Resume-to-Interview Coach** — best overall chance of a polished, credible, judge-friendly submission.
2. **AI Interior Makeover** — highest visual “wow,” but risky because image editing, upload reliability, generation latency, and consistent output can fail during a live demo.
3. **Campaign Planner** — commercially understandable and demoable, but crowded; it needs a sharp niche to avoid looking like a prompt wrapper.
4. **Task Management App** — feasible, but highly saturated unless transformed into a specific meeting-to-execution workflow.
5. **Personal Finance Manager** — strong user need but weaker trust profile; financial categorisation must be accurate and privacy handling becomes a concern.
6. **Collaborative Notetaker** — real-time collaboration increases implementation risk, while the core concept is already commoditised.
7. **Pet Care Companion** — safe to build but lower urgency and weaker AI differentiation.
8. **Personal Health Manager** — crowded, sensitive, and likely to be judged as another habit tracker without clinical-grade safeguards.

## Architecture recommendation

Use Bolt for the UI, Supabase for authentication and saved data, and OpenAI for structured analysis and feedback.

Core entities: `profiles`, `resumes`, `job_descriptions`, `readiness_analyses`, `mock_sessions`, `questions`, and `responses`.

Keep uploaded/pasted content private per user. Do not use real third-party candidate data, and use demo resumes/job descriptions that are synthetic or owned by the team.

## Practical submission advice

Your 2–3 minute walkthrough should show only one flawless scenario: a candidate targeting one role, receiving the evidence map, practising one question, and seeing a concrete improvement action. The pitch should lead with the problem: people practise generic questions while recruiters evaluate role-specific evidence.

The supplied playbook does not include a scoring rubric, so the “winning” assessment above is an informed inference from its stated expectations: a working product, focused workflow, AI wow feature, stable demo, live link, Loom walkthrough, and pitch deck.