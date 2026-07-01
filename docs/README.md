# Gigi OS — Documentation Index

> **Know what matters next.**

Version: `0.1`  
Status: Documentation Index  
Owner: Germain Caplain  
Purpose: Provide a clear reading order and structure for the Gigi OS product documentation.

---

# 1. Purpose

This folder contains the product, technical and strategic documentation for Gigi OS.

Gigi OS must be built from documentation first, then code.

This prevents the product from becoming:

```text
too complex
too vague
too AI-dependent
too dashboard-heavy
too integration-heavy
```

The documentation exists to protect the product vision.

---

# 2. Product Definition

Gigi OS is:

```text
An AI-powered operating system for builders, creators and entrepreneurs.
```

Its core promise is:

```text
Open Gigi. Know what matters next. Execute.
```

Gigi OS is not:

```text
a chatbot
a generic todo app
a Notion clone
a Trello clone
a Jira clone
a random AI agent system
```

Gigi OS is mission-first.

---

# 3. Core Product Question

Every part of Gigi OS must support one question:

```text
What is the most important thing the user should do next?
```

If a feature does not help answer this question, it should not be part of the MVP.

---

# 4. Recommended Reading Order

Cursor and any future developer should read the documentation in this order:

```text
1. README.md
2. docs/README.md
3. docs/MASTER_PRD.md
4. docs/OPERATING_RULES.md
5. docs/MVP_SPEC.md
6. docs/UX_FLOWS.md
7. docs/DESIGN_SYSTEM.md
8. docs/ARCHITECTURE.md
9. docs/DATA_MODEL.md
10. docs/DECISION_ENGINE.md
11. docs/MISSION_SYSTEM.md
12. docs/PROJECT_MODEL.md
13. docs/MEMORY_SYSTEM.md
14. docs/AI_MODULES.md
15. docs/AUTOMATION_SYSTEM.md
16. docs/SECURITY_PRIVACY.md
17. docs/ROADMAP.md
18. docs/CURSOR_BUILD_PLAN.md
19. docs/IMPLEMENTATION_CHECKLIST.md
```

---

# 5. Documentation Map

## 5.1 `MASTER_PRD.md`

The foundation document.

Defines:

```text
product vision
core problem
target users
MVP scope
main modules
long-term ambition
```

Read this first to understand what Gigi OS is.

---

## 5.2 `OPERATING_RULES.md`

The behavioral constitution of Gigi OS.

Defines:

```text
how Gigi behaves
when Gigi says no
how Gigi protects focus
how Gigi avoids chaos
how Gigi handles new ideas
```

This file protects the identity of the product.

---

## 5.3 `MVP_SPEC.md`

The exact MVP definition.

Defines:

```text
what must be built first
what must not be built
required screens
required flows
mock data
acceptance criteria
```

This file is essential before coding.

---

## 5.4 `UX_FLOWS.md`

The user experience specification.

Defines:

```text
first launch
daily use
mission screen
mission mode
postpone flow
reject flow
projects screen
brain screen
history screen
```

This file explains how the user experiences Gigi OS.

---

## 5.5 `DESIGN_SYSTEM.md`

The visual identity.

Defines:

```text
colors
typography
layout
cards
buttons
navigation
motion
tone
components
```

This file must guide all UI work.

---

## 5.6 `ARCHITECTURE.md`

The technical structure.

Defines:

```text
stack
layers
modules
repository structure
data flow
state strategy
AI boundaries
integration boundaries
```

This file prevents technical chaos.

---

## 5.7 `DATA_MODEL.md`

The database and domain model.

Defines:

```text
projects
missions
decisions
history
memory
blockers
settings
mock data
future Supabase schema
```

This file ensures Gigi OS can remember properly.

---

## 5.8 `DECISION_ENGINE.md`

The heart of Gigi OS.

Defines:

```text
scoring criteria
weights
priority calculation
mission selection
explainability
alternatives
rejection handling
```

This file explains how Gigi chooses what matters next.

---

## 5.9 `MISSION_SYSTEM.md`

The execution layer.

Defines:

```text
what a mission is
mission lifecycle
mission mode
mission quality
mission splitting
completion
postponement
rejection
```

This file prevents Gigi OS from becoming a generic todo list.

---

## 5.10 `PROJECT_MODEL.md`

The project structure.

Defines:

```text
project fields
statuses
categories
priorities
progress
health
blockers
project examples
```

This file explains how Gigi understands projects.

---

## 5.11 `MEMORY_SYSTEM.md`

The continuity layer.

Defines:

```text
what Gigi remembers
memory categories
decision memory
mission memory
project memory
blocker memory
memory quality
```

This file prevents Gigi OS from restarting from zero.

---

## 5.12 `AI_MODULES.md`

The AI boundaries.

Defines:

```text
when AI is useful
when AI is forbidden
AI modules
AI safety rules
structured inputs
structured outputs
future AI team
```

This file ensures AI improves decisions instead of creating chaos.

---

## 5.13 `AUTOMATION_SYSTEM.md`

The future automation layer.

Defines:

```text
automation maturity levels
approval rules
n8n strategy
GitHub
Gmail
Calendar
Drive
Cursor
external action risks
```

This file prevents automation from being added too early.

---

## 5.14 `SECURITY_PRIVACY.md`

The trust layer.

Defines:

```text
data ownership
privacy rules
memory privacy
AI privacy
external action approval
integration permissions
RLS later
security checklists
```

This file ensures Gigi OS remains trustworthy.

---

## 5.15 `ROADMAP.md`

The build sequence.

Defines:

```text
V0.1 documentation
V0.2 static prototype
V0.3 local MVP
V0.4 Supabase MVP
V0.5 AI-assisted MVP
V1.0 daily use version
future SaaS
```

This file defines the order of development.

---

## 5.16 `CURSOR_BUILD_PLAN.md`

The exact Cursor instruction plan.

Defines:

```text
what Cursor should build first
what files to create
what data to use
what screens to build
what not to build
first Cursor prompt
```

This file should be used when starting development.

---

## 5.17 `IMPLEMENTATION_CHECKLIST.md`

The build control checklist.

Defines:

```text
pre-build checklist
V0.2 checklist
V0.3 checklist
visual acceptance
code acceptance
failure signs
definition of done
```

This file is used to validate each phase.

---

# 6. Current Phase

Current phase:

```text
V0.1 — Documentation
```

Current objective:

```text
Complete the documentation foundation before starting development.
```

Current next phase:

```text
V0.2 — Static UI Prototype
```

---

# 7. Current MVP Target

The next product target is:

```text
V0.2 — Static UI Prototype
```

This version must include:

```text
Mission screen
Projects screen
Brain screen
History screen
premium dark design
mock data
static decision explanation
modular structure
```

This version must not include:

```text
Supabase
authentication
AI API
Stripe
Gmail
Calendar
GitHub API
n8n
payments
agents
automation
```

---

# 8. Core Screens

The MVP has four main screens:

```text
Mission
Projects
Brain
History
```

## Mission

The home screen.

Shows one recommended mission.

## Projects

Shows all projects and their state.

## Brain

Explains why the mission was selected.

## History

Shows progress and decisions over time.

---

# 9. Core Mock Projects

The first prototype must include:

```text
Buildy Clear
Buildy Crafts
Linko
1Millimètre
Le Dernier Souvenir
Gigi OS
```

The main recommended mission for the static prototype is:

```text
Finish the Buildy Clear sales page.
```

---

# 10. Development Rule

Cursor must not build the full product first.

Cursor must build only:

```text
V0.2 — Static UI Prototype
```

The first build should prove:

```text
Can Gigi OS feel useful before it becomes powerful?
```

---

# 11. Forbidden Early Features

Do not add early:

```text
AI agents
Supabase
authentication
payments
Gmail integration
Calendar integration
GitHub integration
n8n workflows
voice assistant
team accounts
advanced dashboards
mobile app
```

These belong to future versions.

---

# 12. Product Identity Rules

Gigi OS must remain:

```text
mission-first
decision-focused
calm
premium
structured
explainable
execution-oriented
```

Gigi OS must not become:

```text
dashboard-first
chat-first
todo-first
agent-first
automation-first
```

---

# 13. First Cursor Mission

The first Cursor mission is:

```text
Build V0.2 Static UI Prototype.
```

Cursor must read:

```text
docs/CURSOR_BUILD_PLAN.md
docs/MVP_SPEC.md
docs/DESIGN_SYSTEM.md
docs/UX_FLOWS.md
docs/ARCHITECTURE.md
```

Then build the static prototype.

---

# 14. Definition of Ready

The project is ready for Cursor when:

```text
[ ] README.md exists.
[ ] docs/README.md exists.
[ ] core documentation exists.
[ ] MVP scope is clear.
[ ] mock data is defined.
[ ] design system is defined.
[ ] architecture is defined.
[ ] Cursor build plan exists.
[ ] implementation checklist exists.
```

---

# 15. Definition of Done for Documentation

V0.1 documentation is done when:

```text
[ ] All core docs are committed.
[ ] The MVP is clearly defined.
[ ] The first Cursor prompt is ready.
[ ] The roadmap is clear.
[ ] Forbidden early features are listed.
[ ] The product identity is protected.
```

---

# 16. Final Principle

This documentation exists to make development easier, not heavier.

The goal is not to write documents forever.

The goal is to make sure Gigi OS is built in the right direction.

> **Document the brain. Then build the body.**
