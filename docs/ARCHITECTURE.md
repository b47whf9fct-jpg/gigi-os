# Gigi OS — Architecture

> **Build the brain before the machine.**

Version: `0.1`  
Status: Technical Specification  
Module: Core Architecture  
Owner: Germain Caplain  
Purpose: Define the technical architecture, module boundaries and development strategy for Gigi OS.

---

# 1. Purpose

This document defines the technical architecture of Gigi OS.

The goal is to build a system that is:

- simple at the beginning;
- modular from day one;
- easy to understand;
- easy to extend;
- safe to refactor;
- ready for AI and automation later.

Gigi OS must not start as a complex SaaS.

It must start as a focused product prototype.

The architecture must protect the product from becoming too complicated too early.

---

# 2. Core Architecture Principle

The core architecture principle is:

> **Product logic first. Infrastructure later.**

Gigi OS must first prove that the mission recommendation system is useful.

Before adding:

```text
authentication
database
AI agents
GitHub integration
Gmail
Calendar
n8n
payments
team accounts
```

the product must prove that it can answer:

```text
What should the user do next?
```

---

# 3. MVP Technical Strategy

The MVP must be built in stages.

## V0.1 — Documentation

No app.

Only documentation.

Purpose:

```text
Define the product before building it.
```

## V0.2 — Static Prototype

No database.

No authentication.

No AI.

Mock data only.

Purpose:

```text
Validate the user experience.
```

## V0.3 — Local Functional MVP

Local state.

Mock persistence or local storage.

Purpose:

```text
Validate the decision engine and mission flow.
```

## V0.4 — Database MVP

Add Supabase and real persistence.

Purpose:

```text
Make the product usable across sessions.
```

## V0.5 — AI-Assisted MVP

Add AI carefully.

Purpose:

```text
Improve mission generation and explanations without losing control.
```

## V1.0 — Daily Use Version

Stable, simple, useful every morning.

Purpose:

```text
Become the user's daily execution system.
```

---

# 4. Recommended Stack

The first real application should use:

```text
Next.js
TypeScript
Tailwind CSS
Supabase
PostgreSQL
```

Optional later:

```text
OpenAI API or compatible LLM provider
n8n
GitHub API
Google Calendar API
Gmail API
Stripe
Vercel
```

---

# 5. Architecture Layers

Gigi OS should be organized into clear layers.

```text
UI Layer
Application Layer
Domain Modules
Data Layer
Integration Layer
AI Layer
```

---

# 6. Layer Responsibilities

## 6.1 UI Layer

Responsible for rendering screens and components.

Examples:

```text
Mission screen
Projects screen
Brain screen
History screen
Mission Mode
Project cards
Score breakdown
```

The UI layer should not contain business logic.

---

## 6.2 Application Layer

Responsible for connecting UI actions to domain logic.

Examples:

```text
startMission
completeMission
postponeMission
rejectMission
updateProject
selectRecommendedMission
```

---

## 6.3 Domain Modules

Responsible for core product logic.

Modules:

```text
projects
missions
decision-engine
memory
history
settings
```

This is the most important layer.

The product must work even before AI is added.

---

## 6.4 Data Layer

Responsible for storage.

In early versions:

```text
mock data
fixtures
local state
local storage
```

Later:

```text
Supabase
PostgreSQL
```

---

## 6.5 Integration Layer

Responsible for external services.

Not part of MVP.

Future integrations:

```text
GitHub
Gmail
Google Calendar
Google Drive
n8n
Stripe
Cursor workflows
```

---

## 6.6 AI Layer

Responsible for AI-assisted reasoning.

Not required for the first prototype.

Future AI features:

```text
mission generation
decision explanation
weekly review
project summaries
blocker detection
agent modules
```

AI must never replace the deterministic decision structure.

---

# 7. High-Level Architecture

```text
Gigi OS
│
├── UI
│   ├── Mission Screen
│   ├── Projects Screen
│   ├── Brain Screen
│   └── History Screen
│
├── Modules
│   ├── Projects
│   ├── Missions
│   ├── Decision Engine
│   ├── Memory
│   └── History
│
├── Data
│   ├── Mock Data
│   ├── Local Storage
│   └── Supabase later
│
├── AI Layer
│   └── Optional after MVP
│
└── Integrations
    └── Future only
```

---

# 8. Suggested Repository Structure

```text
gigi-os/
│
├── docs/
│   ├── MASTER_PRD.md
│   ├── DECISION_ENGINE.md
│   ├── MISSION_SYSTEM.md
│   ├── PROJECT_MODEL.md
│   ├── MEMORY_SYSTEM.md
│   ├── UX_FLOWS.md
│   ├── DESIGN_SYSTEM.md
│   └── ARCHITECTURE.md
│
├── app/
│   ├── page.tsx
│   ├── mission/
│   ├── projects/
│   ├── brain/
│   └── history/
│
├── components/
│   ├── ui/
│   ├── mission/
│   ├── projects/
│   ├── brain/
│   └── history/
│
├── modules/
│   ├── decision-engine/
│   ├── projects/
│   ├── missions/
│   ├── memory/
│   └── history/
│
├── data/
│   ├── mockProjects.ts
│   ├── mockMissions.ts
│   └── mockHistory.ts
│
├── lib/
│   ├── utils.ts
│   └── constants.ts
│
└── README.md
```

---

# 9. Module Boundaries

Each module must have a clear responsibility.

## 9.1 Projects Module

Responsible for:

```text
project types
project creation
project updates
project health
project fixtures
project history
```

Should not decide today’s mission.

That belongs to the Decision Engine.

---

## 9.2 Missions Module

Responsible for:

```text
mission types
mission lifecycle
mission status updates
mission steps
mission splitting
mission feedback
```

Should not decide which mission is most important.

That belongs to the Decision Engine.

---

## 9.3 Decision Engine Module

Responsible for:

```text
scoring projects
scoring missions
ranking options
selecting one mission
explaining decisions
comparing alternatives
```

This is the core brain.

---

## 9.4 Memory Module

Responsible for:

```text
storing decisions
storing mission history
storing project state
retrieving relevant memories
summarizing context
```

Should not become a random notes database.

---

## 9.5 History Module

Responsible for:

```text
timeline events
completed missions
project changes
decision logs
feedback events
```

History is the visible form of memory.

---

# 10. First Implementation Rule

The first implementation must use mock data.

Cursor must not add:

```text
Supabase
authentication
OpenAI API
server actions
complex API routes
payments
integrations
```

until the static product experience is approved.

---

# 11. Data Flow

## 11.1 Initial MVP Data Flow

```text
Mock Projects
     ↓
Decision Engine
     ↓
Mission Recommendation
     ↓
Mission Screen
     ↓
User Action
     ↓
Mission Status Update
     ↓
History Event
     ↓
Decision Engine Recalculates
```

---

## 11.2 Future Data Flow

```text
Supabase
     ↓
Project Module
     ↓
Decision Engine
     ↓
Mission Module
     ↓
Memory Module
     ↓
UI
     ↓
User Feedback
     ↓
Supabase
```

---

# 12. Decision Engine Architecture

Suggested structure:

```text
modules/decision-engine/
│
├── decisionTypes.ts
├── decisionWeights.ts
├── calculateMissionScore.ts
├── selectMission.ts
├── explainDecision.ts
├── rankMissions.ts
├── decisionFixtures.ts
└── index.ts
```

## Responsibilities

```text
calculateMissionScore.ts
Calculates weighted score.

selectMission.ts
Selects the best mission.

explainDecision.ts
Generates human-readable explanation.

rankMissions.ts
Sorts candidate missions.

decisionWeights.ts
Stores scoring weights.
```

---

# 13. Projects Module Architecture

Suggested structure:

```text
modules/projects/
│
├── projectTypes.ts
├── projectFixtures.ts
├── createProject.ts
├── updateProject.ts
├── calculateProjectHealth.ts
├── projectHistory.ts
└── index.ts
```

---

# 14. Missions Module Architecture

Suggested structure:

```text
modules/missions/
│
├── missionTypes.ts
├── missionFixtures.ts
├── createMissionFromNextAction.ts
├── splitMission.ts
├── updateMissionStatus.ts
├── missionHistory.ts
└── index.ts
```

---

# 15. Memory Module Architecture

Suggested structure:

```text
modules/memory/
│
├── memoryTypes.ts
├── memoryFixtures.ts
├── createMemory.ts
├── updateMemory.ts
├── archiveMemory.ts
├── getRelevantMemories.ts
├── createHistoryEvent.ts
└── index.ts
```

---

# 16. UI Component Architecture

Suggested structure:

```text
components/ui/
│
├── GlassCard.tsx
├── PrimaryButton.tsx
├── SecondaryButton.tsx
├── StatusBadge.tsx
├── ProgressBar.tsx
├── ConfidenceIndicator.tsx
└── SectionHeader.tsx
```

```text
components/mission/
│
├── MissionCard.tsx
├── MissionMode.tsx
├── MissionSteps.tsx
└── MissionActions.tsx
```

```text
components/projects/
│
├── ProjectCard.tsx
├── ProjectList.tsx
└── ProjectDetail.tsx
```

```text
components/brain/
│
├── ScoreBreakdown.tsx
├── DecisionReason.tsx
└── AlternativesList.tsx
```

```text
components/history/
│
├── HistoryTimeline.tsx
└── HistoryEventCard.tsx
```

---

# 17. App Routes

For the MVP:

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

Optional later:

```text
/projects/[id]
Project detail

/mission/[id]
Mission detail

/settings
Settings

/onboarding
First launch setup
```

---

# 18. State Management

The MVP should avoid complex state management.

Recommended order:

```text
1. Static mock data
2. React state
3. Local storage
4. Supabase
5. Global state only if necessary
```

Avoid adding:

```text
Redux
Zustand
complex stores
server state libraries
```

unless the need is proven.

---

# 19. Persistence Strategy

## V0.2

No persistence.

Mock data.

## V0.3

Local persistence.

Possible options:

```text
localStorage
IndexedDB
simple JSON fixtures
```

## V0.4

Supabase persistence.

Tables:

```text
projects
missions
decisions
history_events
memories
settings
```

---

# 20. Database Architecture Later

When Supabase is added, suggested tables:

```text
profiles
projects
missions
mission_steps
decisions
decision_scores
history_events
memories
blockers
user_settings
```

Do not add database too early.

The product logic must be validated first.

---

# 21. AI Architecture Later

AI should be introduced only after the deterministic version works.

AI features must be isolated.

Suggested structure:

```text
modules/ai/
│
├── aiTypes.ts
├── generateMission.ts
├── summarizeProject.ts
├── explainDecisionWithAI.ts
├── detectBlockers.ts
└── prompts/
```

The AI layer should receive structured inputs and return structured outputs.

It should not directly control the product state.

---

# 22. AI Safety Rule

AI must not silently change:

```text
project status
mission status
priority
memory
history
settings
```

AI can suggest.

The system or user decides.

---

# 23. Deterministic First Rule

The core recommendation must work without AI.

This is critical.

Bad architecture:

```text
Ask AI what to do next.
```

Good architecture:

```text
Use structured scoring to choose a mission.
Use AI later to improve explanation and wording.
```

---

# 24. Integration Architecture Later

Future integrations must be isolated.

Suggested structure:

```text
integrations/
│
├── github/
├── gmail/
├── calendar/
├── drive/
├── n8n/
└── stripe/
```

Each integration must have:

```text
client
types
service
sync logic
error handling
```

No integration should leak complexity into core modules.

---

# 25. Error Handling

The app must handle simple errors clearly.

Examples:

```text
No active project
No next action
Mission too large
Decision confidence low
Missing project data
```

Errors should create useful recovery actions.

Example:

```text
This project has no next action.
Add one so Gigi can prioritize it.
```

---

# 26. Testing Strategy

Tests should focus first on product logic.

Priority tests:

```text
Decision Engine scoring
Mission selection
Mission lifecycle
Project health
Memory creation
History events
```

UI tests can come later.

---

# 27. Suggested Test Structure

```text
modules/decision-engine/__tests__/
  calculateMissionScore.test.ts
  selectMission.test.ts

modules/missions/__tests__/
  updateMissionStatus.test.ts
  splitMission.test.ts

modules/projects/__tests__/
  calculateProjectHealth.test.ts

modules/memory/__tests__/
  createHistoryEvent.test.ts
```

---

# 28. Code Quality Rules

## Rule 1

Domain logic must not live inside React components.

## Rule 2

Types must be explicit.

## Rule 3

Modules must be independent.

## Rule 4

No external API in the first prototype.

## Rule 5

No hidden magic.

## Rule 6

Every important decision should be traceable.

---

# 29. TypeScript Standards

Use TypeScript strictly.

Recommended:

```text
strict mode enabled
no implicit any
clear domain types
small pure functions
explicit return types for core logic
```

Avoid:

```text
large untyped objects
business logic inside JSX
deeply nested conditional UI logic
```

---

# 30. Performance Principles

The MVP will be small, but performance should stay clean.

Rules:

```text
avoid unnecessary dependencies
keep components simple
avoid heavy animation
avoid large global state
load only needed data
```

---

# 31. Security Principles

Security is not central in V0.2 because there is no backend.

Later, when Supabase is added:

```text
use Row Level Security
protect user data
validate inputs
avoid exposing API keys
store secrets server-side
use proper auth
```

---

# 32. Deployment Strategy

Recommended later:

```text
Vercel for Next.js
Supabase for database
GitHub for source control
```

Deployment should come after the static prototype works locally.

---

# 33. Development Phases

## Phase A — Documentation

Complete:

```text
MASTER_PRD
DECISION_ENGINE
MISSION_SYSTEM
PROJECT_MODEL
MEMORY_SYSTEM
UX_FLOWS
DESIGN_SYSTEM
ARCHITECTURE
```

## Phase B — Static UI Prototype

Build:

```text
Mission screen
Projects screen
Brain screen
History screen
```

## Phase C — Mock Logic

Add:

```text
mock projects
mock missions
deterministic decision engine
mission lifecycle
history events
```

## Phase D — Local Persistence

Add:

```text
local storage
editable projects
editable missions
saved history
```

## Phase E — Supabase

Add:

```text
auth
database
user data
real persistence
```

## Phase F — AI Assistance

Add:

```text
AI summaries
AI mission generation
AI explanations
weekly review
```

---

# 34. MVP Acceptance Criteria

The architecture is successful if:

- the app can be built without database first;
- the decision engine works with mock data;
- the UI can display one recommended mission;
- modules remain separate;
- the product does not become complex too early;
- Cursor can understand where to place files;
- the codebase can later accept Supabase and AI without being rewritten.

The architecture fails if:

- everything is built in one component;
- AI is required before the product works;
- database is added before product logic is validated;
- modules are unclear;
- the app becomes a generic dashboard;
- the decision logic is hidden or impossible to test.

---

# 35. First Cursor Build Instruction

Cursor must start with this goal:

```text
Create a clean static prototype of Gigi OS with four screens and mock data.
```

Cursor must not add:

```text
auth
database
AI API
payment
integrations
complex settings
```

Initial build should include:

```text
Next.js
TypeScript
Tailwind CSS
AppShell
Mission screen
Projects screen
Brain screen
History screen
Mock project data
Mock mission data
Basic decision engine logic
```

---

# 36. Final Principle

Gigi OS must be built like a serious product, but not overbuilt too early.

The architecture should be strong enough to grow.

But simple enough to ship.

> **Start simple. Stay modular. Scale only when useful.**
