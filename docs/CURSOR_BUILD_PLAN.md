# Gigi OS — Cursor Build Plan

> **Build exactly what matters. Nothing more.**

Version: `0.1`  
Status: Build Instruction  
Owner: Germain Caplain  
Purpose: Give Cursor a precise development plan for the first Gigi OS prototype.

---

# 1. Purpose

This document tells Cursor how to build the first version of Gigi OS.

Cursor must not improvise the product.

Cursor must follow the documentation.

The goal is to build:

```text
V0.2 — Static UI Prototype
```

The prototype must show the core experience of Gigi OS:

```text
Open Gigi. See one mission. Understand why. Execute.
```

---

# 2. Cursor Role

Cursor is the Lead Developer.

Cursor must:

```text
read the documentation
respect the MVP scope
build modular code
avoid overengineering
create a beautiful static prototype
use mock data
keep the product mission-first
```

Cursor must not:

```text
add AI too early
add Supabase too early
add authentication
add payments
add Gmail
add Calendar
add GitHub API
add n8n
create a generic todo app
invent new features outside the docs
```

---

# 3. Required Documentation to Read First

Cursor must read these files before coding:

```text
README.md
docs/MASTER_PRD.md
docs/DECISION_ENGINE.md
docs/MISSION_SYSTEM.md
docs/PROJECT_MODEL.md
docs/MEMORY_SYSTEM.md
docs/UX_FLOWS.md
docs/DESIGN_SYSTEM.md
docs/ARCHITECTURE.md
docs/ROADMAP.md
docs/MVP_SPEC.md
```

If any file is missing, Cursor should create it as a placeholder but must not invent the product direction.

---

# 4. Current Target Version

Current target:

```text
V0.2 — Static UI Prototype
```

The objective is visual and experiential.

Cursor must build a first interface that makes Gigi OS feel real.

---

# 5. V0.2 Goal

The V0.2 goal is:

> **Create a premium static web prototype with four screens and mock data.**

The prototype must answer:

```text
What is my mission today?
Why is this mission recommended?
What projects exist?
What progress has been made?
```

---

# 6. Required Stack

Use:

```text
Next.js
TypeScript
Tailwind CSS
App Router
```

Do not use:

```text
Supabase
OpenAI API
Stripe
n8n
Gmail API
Calendar API
GitHub API
Redux
complex state management
```

---

# 7. Required Screens

Cursor must create these screens:

```text
/
Mission screen

/projects
Projects screen

/brain
Brain screen

/history
History screen
```

Optional if easy:

```text
/mission
Mission Mode preview
```

But do not create a large routing system yet.

---

# 8. Required Layout

Create a global app shell.

Desktop layout:

```text
left sidebar
main content area
dark premium background
```

Mobile layout:

```text
responsive stacked layout
navigation remains usable
mission remains first
```

Navigation items:

```text
Mission
Projects
Brain
History
```

Mission must be first.

---

# 9. Design Requirements

Follow `docs/DESIGN_SYSTEM.md`.

The interface must feel:

```text
premium
dark
calm
focused
cinematic
minimal
intelligent
```

Use:

```text
deep black background
glass cards
soft borders
subtle blur
warm white text
electric blue accent
copper accent for primary actions
generous spacing
```

Avoid:

```text
bright colorful UI
childish gamification
overloaded dashboard
generic SaaS template feeling
too many buttons
too many charts
```

---

# 10. Required Components

Create these components:

```text
components/ui/AppShell.tsx
components/ui/GlassCard.tsx
components/ui/PrimaryButton.tsx
components/ui/SecondaryButton.tsx
components/ui/StatusBadge.tsx
components/ui/ProgressBar.tsx
components/ui/ConfidenceIndicator.tsx
components/ui/SectionHeader.tsx
```

Mission components:

```text
components/mission/MissionCard.tsx
components/mission/MissionModePreview.tsx
components/mission/MissionActions.tsx
components/mission/MissionSteps.tsx
```

Project components:

```text
components/projects/ProjectCard.tsx
components/projects/ProjectList.tsx
```

Brain components:

```text
components/brain/ScoreBreakdown.tsx
components/brain/DecisionReason.tsx
components/brain/AlternativesList.tsx
```

History components:

```text
components/history/HistoryTimeline.tsx
components/history/HistoryEventCard.tsx
```

---

# 11. Required Modules

Create these module folders:

```text
modules/projects/
modules/missions/
modules/decision-engine/
modules/memory/
modules/history/
```

For V0.2, modules can use mock data only.

---

# 12. Required Data Files

Create:

```text
data/mockProjects.ts
data/mockMissions.ts
data/mockHistory.ts
```

Mock projects must include:

```text
Buildy Clear
Buildy Crafts
Linko
1Millimètre
Le Dernier Souvenir
Gigi OS
```

---

# 13. Initial Mock Project Data

Use these base project states:

```text
Buildy Clear
Status: active
Progress: 94
Priority: critical
Next action: Finish the sales page and checkout flow.
Business potential: 9
Strategic value: 7
Urgency: 9
Estimated effort: 3
Clarity: 9

Buildy Crafts
Status: active
Progress: 72
Priority: high
Next action: Continue stabilizing the app and expanding missing trade categories.
Business potential: 10
Strategic value: 10
Urgency: 6
Estimated effort: 8
Clarity: 7

Linko
Status: paused
Progress: 22
Priority: medium
Next action: Finalize positioning and validate name availability.
Business potential: 9
Strategic value: 9
Urgency: 4
Estimated effort: 9
Clarity: 5

1Millimètre
Status: paused
Progress: 28
Priority: low
Next action: Improve core gameplay feeling and visual polish.
Business potential: 6
Strategic value: 5
Urgency: 3
Estimated effort: 6
Clarity: 6

Le Dernier Souvenir
Status: future
Progress: 5
Priority: low
Next action: Write the story bible and define the visual identity.
Business potential: 7
Strategic value: 6
Urgency: 2
Estimated effort: 7
Clarity: 4

Gigi OS
Status: active
Progress: 10
Priority: high
Next action: Complete the core product documentation.
Business potential: 8
Strategic value: 10
Urgency: 7
Estimated effort: 8
Clarity: 8
```

---

# 14. Required Mission Recommendation

The main recommended mission for the first prototype should be:

```text
Finish the Buildy Clear sales page.
```

Reason:

```text
Buildy Clear is the closest project to short-term revenue. It is near launch, the next action is clear, and completing the sales page unlocks the next step: publishing traffic videos.
```

Estimated duration:

```text
45 minutes
```

Expected impact:

```text
High
```

Confidence:

```text
87%
```

---

# 15. Mission Screen Requirements

The Mission screen must be the strongest screen.

It must show:

```text
Today's Mission
mission title
related project
estimated duration
expected impact
confidence
reason
Start Mission button
Postpone action
Reject action
Explain decision action
```

The page must not feel like a dashboard.

It must feel like:

```text
a focused command screen
```

---

# 16. Projects Screen Requirements

The Projects screen must show project cards.

Each card must include:

```text
project name
status
progress
priority
next action
blocker if any
business potential
```

Active projects should be visually stronger.

Paused and future projects should be quieter.

---

# 17. Brain Screen Requirements

The Brain screen must explain the recommendation.

It must show:

```text
selected mission
selected project
final score
score breakdown
reasoning
alternatives considered
why alternatives were not selected
```

Use mock score values.

Example score breakdown:

```text
Business impact: 9
Alignment: 9
Completion proximity: 10
Urgency: 8
Clarity: 9
Effort efficiency: 8
Risk of delay: 6
Final score: 87%
```

Alternatives:

```text
Buildy Crafts — strategic but longer-term
Gigi OS — important, but documentation can continue after revenue work
Linko — promising, but paused
1Millimètre — experimental
Le Dernier Souvenir — future creative project
```

---

# 18. History Screen Requirements

The History screen must show a calm timeline.

Mock events:

```text
Today
Created docs/MVP_SPEC.md
Created docs/ROADMAP.md

Yesterday
Created docs/ARCHITECTURE.md
Created docs/DESIGN_SYSTEM.md
Created docs/UX_FLOWS.md

Earlier
Created docs/MEMORY_SYSTEM.md
Created docs/PROJECT_MODEL.md
Created docs/MISSION_SYSTEM.md
Created docs/DECISION_ENGINE.md
```

The History screen should feel like progress, not developer logs.

---

# 19. Static Prototype Rules

For V0.2:

Buttons can be static.

No real persistence is required.

No backend is required.

No user account is required.

No API calls are allowed.

The goal is to validate:

```text
visual direction
screen hierarchy
mission-first experience
clarity of recommendation
overall product feeling
```

---

# 20. Decision Engine V0.2

Cursor should create a simple mock Decision Engine structure even if static.

Files:

```text
modules/decision-engine/decisionTypes.ts
modules/decision-engine/decisionWeights.ts
modules/decision-engine/calculateMissionScore.ts
modules/decision-engine/selectMission.ts
modules/decision-engine/explainDecision.ts
```

For V0.2, the functions may return mock values.

But the structure must be ready for V0.3.

---

# 21. Project Module V0.2

Create:

```text
modules/projects/projectTypes.ts
modules/projects/projectFixtures.ts
modules/projects/calculateProjectHealth.ts
```

Project health can be basic.

Example:

```text
if progress >= 90 => ready_to_launch
if nextAction is missing => unclear
if status is paused => paused
otherwise healthy
```

---

# 22. Mission Module V0.2

Create:

```text
modules/missions/missionTypes.ts
modules/missions/missionFixtures.ts
modules/missions/createMissionFromNextAction.ts
```

V0.2 can be simple.

---

# 23. Memory and History V0.2

Create:

```text
modules/memory/memoryTypes.ts
modules/history/historyTypes.ts
```

Use mock history only.

---

# 24. Code Quality Rules

Cursor must follow these rules:

```text
Use TypeScript.
Keep components small.
Keep business logic out of React components.
Use explicit types.
Avoid unnecessary dependencies.
Avoid overengineering.
Use readable names.
Use clean file structure.
```

---

# 25. UI Quality Rules

Cursor must ensure:

```text
Mission screen looks premium.
Spacing is generous.
Cards are not crowded.
Typography is readable.
Primary action is obvious.
Navigation is calm.
Responsive behavior is acceptable.
Dark theme is clean.
```

---

# 26. What Cursor Must Not Build Yet

Cursor must not build:

```text
authentication
Supabase
OpenAI API
Stripe
Gmail integration
Calendar integration
GitHub integration
n8n integration
voice mode
agent system
settings complexity
notifications
admin panel
team accounts
billing
```

---

# 27. First Cursor Prompt

Use this prompt in Cursor when ready:

```text
You are the lead developer of Gigi OS.

Before coding, read all documentation in /docs and README.md.

Your first mission is to build V0.2 — Static UI Prototype.

Build a premium dark Next.js + TypeScript + Tailwind interface with four screens:
- Mission
- Projects
- Brain
- History

Use mock data only.
Do not add Supabase.
Do not add authentication.
Do not add AI calls.
Do not add external integrations.
Do not add payments.

The product must be mission-first, not dashboard-first.

The Mission screen should be the home screen and must clearly show one recommended mission:
"Finish the Buildy Clear sales page."

Follow:
- docs/MVP_SPEC.md
- docs/DESIGN_SYSTEM.md
- docs/UX_FLOWS.md
- docs/ARCHITECTURE.md
- docs/DECISION_ENGINE.md

Create a modular structure:
- app/
- components/
- modules/
- data/
- lib/

Implement mock projects:
Buildy Clear, Buildy Crafts, Linko, 1Millimètre, Le Dernier Souvenir, Gigi OS.

Create a simple decision engine structure, but no real AI.

At the end, provide:
1. Summary of files created.
2. How to run the project.
3. What is implemented.
4. What is intentionally not implemented.
5. Next recommended step for V0.3.
```

---

# 28. V0.2 Acceptance Checklist

Before considering V0.2 complete, verify:

```text
[ ] The app runs locally.
[ ] The home screen is Mission.
[ ] One mission is clearly recommended.
[ ] The design feels premium and dark.
[ ] Projects screen shows all mock projects.
[ ] Brain screen explains the recommendation.
[ ] History screen shows mock progress.
[ ] No Supabase was added.
[ ] No AI API was added.
[ ] No authentication was added.
[ ] Code is modular.
[ ] Business logic is outside UI components.
[ ] The product does not feel like a todo list.
```

---

# 29. After V0.2

After V0.2 is approved, move to:

```text
V0.3 — Local Functional MVP
```

V0.3 will add:

```text
project create/edit
mission start/complete
postpone/reject
local history events
localStorage
real decision scoring
```

Still no Supabase.

Still no AI.

---

# 30. Final Instruction

Cursor must build the smallest version that makes Gigi OS feel real.

Do not impress with features.

Impress with clarity.

> **One mission. One screen. One reason. One action.**
