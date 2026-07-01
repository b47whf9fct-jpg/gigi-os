# Gigi OS — Master Product Requirements Document

> **Know what matters next.**

Version: `0.1`  
Status: Product Foundation  
Owner: Germain Caplain  
Product role: AI Operating System for builders, creators and entrepreneurs  
Primary objective: Help the user always know the most important next action.

---

# 1. Executive Summary

Gigi OS is an AI-powered operating system designed to help builders, creators and entrepreneurs manage multiple projects without getting lost in complexity.

It is not a chatbot.

It is not a task manager.

It is not a clone of Notion, Trello, Jira or ChatGPT.

Gigi OS is a decision system.

Its core mission is to answer one question better than any other tool:

> **What is the most important thing I should do next?**

The first version of Gigi OS must be simple, focused and useful before it becomes powerful.

The product starts with a single user and a real problem: managing several ambitious projects at the same time while staying focused on the action that creates the most progress.

Example projects:

- Buildy Crafts
- Buildy Clear
- Linko
- 1Millimètre
- Le Dernier Souvenir
- Gigi OS itself

Gigi OS should eventually become the central brain of all these projects.

---

# 2. Product Vision

The long-term vision of Gigi OS is to become:

> **The operating system for AI-driven execution.**

A user should be able to open Gigi OS every morning and immediately know:

- what matters today;
- why it matters;
- how long it should take;
- what the expected impact is;
- what should be ignored for now.

Gigi OS should reduce decision fatigue.

It should prevent project chaos.

It should turn ideas into execution.

It should become the central system that helps a founder build, manage and grow multiple projects.

---

# 3. Core Problem

Entrepreneurs and creators often do not fail because they lack ideas.

They fail because:

- they have too many ideas;
- they change priorities too often;
- they do not know which project deserves attention now;
- they spend too much time planning and not enough time executing;
- they forget previous decisions;
- they restart the same thinking again and again;
- they confuse excitement with priority;
- they lack a system that says “not now”.

Gigi OS exists to solve this.

The main problem is:

> **The user does not always know what to work on next.**

The product must solve this problem before adding anything else.

---

# 4. Product Promise

Gigi OS promises:

> **Open the app. Know what matters next. Start executing.**

The user should not open Gigi OS to browse.

The user should open Gigi OS to act.

---

# 5. What Gigi OS Is

Gigi OS is:

- a project operating system;
- a decision engine;
- a mission generator;
- a project memory;
- a prioritization layer;
- a future AI agent coordinator;
- a personal execution system.

Gigi OS helps the user move from:

```text
I have too many ideas.
```

to:

```text
This is the one thing I need to do now.
```

---

# 6. What Gigi OS Is Not

Gigi OS is not:

- a basic chatbot;
- a generic productivity app;
- a simple to-do list;
- a calendar replacement;
- a Notion clone;
- a Trello clone;
- a Jira clone;
- a social app;
- a gamified toy;
- a place to store random notes without action.

If a feature does not improve decision-making or execution, it does not belong in the MVP.

---

# 7. Product Philosophy

## 7.1 One Mission at a Time

The user should never see ten competing priorities.

Gigi OS must always identify one main mission.

Secondary tasks can exist, but the product experience should push the user toward the single highest-impact action.

## 7.2 Execution Beats Planning

Planning is useful only if it leads to action.

Gigi OS should avoid endless planning loops.

Every project must always have a next action.

## 7.3 Data Before Emotion

A project should not become the priority only because it feels exciting.

Gigi OS must consider:

- progress;
- business impact;
- urgency;
- risk;
- cost;
- available time;
- user goals;
- current blockers.

## 7.4 Ideas Are Never Lost

Gigi OS should not kill ideas.

It should classify them:

- active;
- paused;
- future;
- archived;
- completed.

This allows the user to focus without feeling like they are abandoning something important.

## 7.5 The System Must Be Explainable

Gigi OS must explain why it recommends a mission.

The user should never feel that the system is making random decisions.

Example:

```text
Buildy Clear is today's priority because it is close to launch, has short-term revenue potential, and requires less than 2 hours to complete the next milestone.
```

---

# 8. Target Users

## 8.1 Primary User

The first user is a solo builder / entrepreneur managing several projects at once.

Characteristics:

- has many ideas;
- builds digital products;
- uses AI tools;
- wants income;
- works alone or with a small team;
- needs structure;
- does not want complex project management software;
- wants clarity every day.

## 8.2 Future Users

Future user types may include:

- indie hackers;
- freelancers;
- creators;
- startup founders;
- small agencies;
- builders using AI agents;
- creators managing several content/product projects.

---

# 9. North Star

The product must always be driven by a North Star.

A North Star is the user’s highest-level objective.

Example:

```text
Generate 10,000 € per month from digital products and software.
```

Every project and mission should be evaluated against this objective.

Gigi OS should ask:

```text
Does this action move the user closer to the North Star?
```

If the answer is no, the action should be deprioritized.

---

# 10. MVP Scope

The MVP must be intentionally small.

The goal is not to build the full Gigi OS.

The goal is to prove that the system can help the user decide what to do next.

## 10.1 MVP Features

The MVP includes only:

1. Mission screen
2. Projects screen
3. Decision explanation screen
4. History screen
5. Basic project model
6. Basic decision engine
7. Basic mission completion flow

## 10.2 Out of Scope for MVP

The MVP must not include:

- Gmail integration;
- Google Calendar integration;
- GitHub automation;
- n8n workflows;
- advanced AI agents;
- payments;
- team accounts;
- public SaaS onboarding;
- complex analytics;
- mobile app;
- voice assistant;
- file uploads;
- complex dashboards.

These features are future versions.

The MVP must stay focused.

---

# 11. Core Screens

## 11.1 Mission Screen

This is the default home screen.

The user should not land on a dashboard.

The user should land on today’s mission.

### Purpose

Answer immediately:

```text
What should I do now?
```

### Required Elements

The Mission screen must show:

- mission title;
- related project;
- estimated duration;
- expected impact;
- reason for priority;
- Start Mission button;
- option to reject or postpone the mission.

### Example

```text
Today’s Mission

Finish Buildy Clear sales page

Estimated time:
45 minutes

Expected impact:
High

Why this mission:
Buildy Clear is the closest project to generating revenue.
```

---

## 11.2 Projects Screen

The Projects screen lists all active and paused projects.

### Required Elements

Each project card must show:

- project name;
- status;
- progress percentage;
- priority level;
- next action;
- business potential;
- current blocker, if any.

### Example Projects

```text
Buildy Clear
Status: Active
Progress: 94%
Priority: Critical
Next action: Finish sales page
Potential: Short-term revenue

Buildy Crafts
Status: Active
Progress: 70%
Priority: Strategic
Next action: Continue product stabilization
Potential: Long-term SaaS/app revenue

Linko
Status: Paused
Progress: 20%
Priority: Future strategic project
Next action: Validate name and positioning

1Millimètre
Status: Paused
Progress: 25%
Priority: Experimental
Next action: Improve core gameplay

Le Dernier Souvenir
Status: Idea
Progress: 5%
Priority: Creative side project
Next action: Build story bible
```

---

## 11.3 Brain Screen

The Brain screen explains decisions.

It is where the user can understand why Gigi selected the current mission.

### Purpose

Make the decision engine transparent.

### Required Elements

The Brain screen must show:

- selected mission;
- compared projects;
- scoring criteria;
- final reasoning;
- rejected alternatives;
- recommendation.

### Example

```text
Why Buildy Clear?

Buildy Clear was selected because:

- it is almost complete;
- it has direct revenue potential;
- the next action is clear;
- it requires little time;
- it supports the current financial goal.

Rejected today:

Buildy Crafts:
Important, but longer-term.

Linko:
Strategic, but not ready for monetization.

1Millimètre:
Interesting, but experimental.
```

---

## 11.4 History Screen

The History screen records execution.

### Required Elements

It must show:

- completed missions;
- postponed missions;
- rejected missions;
- project changes;
- important decisions;
- progress over time.

### Purpose

Prevent repeated thinking and create memory.

Gigi OS must not forget why something was done.

---

# 12. Project Model

Each project must have a structured model.

## Required Fields

```text
id
name
description
vision
status
category
progress
priority
business_potential
risk_level
estimated_effort
next_action
current_blocker
last_updated
created_at
```

## Status Values

```text
active
paused
future
archived
completed
```

## Priority Values

```text
critical
high
medium
low
none
```

## Category Examples

```text
software
digital_product
content
game
platform
internal_tool
creative_project
```

---

# 13. Mission Model

A mission is not a generic task.

A mission is the single action Gigi OS recommends now.

## Required Fields

```text
id
title
project_id
description
estimated_duration
expected_impact
reason
status
created_at
completed_at
```

## Mission Status Values

```text
available
started
completed
postponed
rejected
```

## Mission Rules

A mission must:

- be clear;
- be actionable;
- be short enough to start;
- belong to a project;
- have a reason;
- have an estimated impact;
- have a completion state.

A bad mission:

```text
Work on Buildy Clear.
```

A good mission:

```text
Rewrite the headline and call-to-action of the Buildy Clear sales page.
```

---

# 14. Decision Engine

The Decision Engine is the heart of Gigi OS.

It compares all projects and selects the next mission.

## 14.1 Decision Criteria

The first version should score each project/action using:

| Criterion | Description |
|---|---|
| Business impact | Can this create revenue or strategic value? |
| Urgency | Does this need attention now? |
| Completion proximity | Is the project close to a milestone? |
| Clarity | Is the next action obvious? |
| Effort | Can it be done in a reasonable time? |
| Risk | What happens if this is ignored? |
| Alignment | Does it support the North Star? |

## 14.2 Scoring System

Each criterion should be scored from 1 to 10.

Example:

```text
Business impact: 9
Urgency: 8
Completion proximity: 10
Clarity: 9
Effort: 8
Risk: 6
Alignment: 9
```

The Decision Engine should calculate a weighted score.

Initial suggested weights:

```text
Business impact: 25%
Alignment: 20%
Completion proximity: 15%
Urgency: 15%
Clarity: 10%
Effort: 10%
Risk: 5%
```

The scoring system can evolve later.

## 14.3 Decision Output

The Decision Engine must output:

```text
selected_project
selected_mission
score
reason
alternatives_considered
why_others_were_not_selected
```

## 14.4 Explainability Requirement

Every recommendation must be explainable in natural language.

The system must never simply say:

```text
This is recommended.
```

It must say why.

---

# 15. Memory System

The MVP memory system can be simple.

It does not need advanced AI memory at first.

## MVP Memory

The system should remember:

- projects;
- missions;
- completed missions;
- rejected missions;
- postponed missions;
- important decisions;
- project status changes.

## Future Memory

Later, Gigi OS should remember:

- user working patterns;
- recurring blockers;
- project history;
- business assumptions;
- lessons learned;
- past mistakes;
- previous strategic decisions.

## Memory Principle

Memory exists to avoid repeating the same thinking.

---

# 16. User Journey

## 16.1 First Use

The user opens Gigi OS.

The system asks:

```text
What is your North Star?
```

The user enters:

```text
Generate 500 € per month from my projects.
```

The system asks the user to add projects.

For each project, the user enters:

- name;
- goal;
- progress;
- next action;
- business potential.

Gigi OS then generates the first mission.

---

## 16.2 Daily Use

The user opens Gigi OS.

The first screen shows:

```text
Today’s Mission
```

The user can:

- start mission;
- complete mission;
- postpone mission;
- reject mission;
- ask why this mission was selected.

After completion, Gigi OS updates the project and suggests the next mission.

---

## 16.3 Weekly Review

Future version.

Gigi OS summarizes:

- what moved forward;
- what stayed blocked;
- which project gained priority;
- which project should be paused;
- what the next week should focus on.

---

# 17. UX Principles

## 17.1 Calm Interface

The interface must feel calm, premium and focused.

No visual noise.

No overloaded dashboards.

No unnecessary widgets.

## 17.2 Mission First

The first screen must always focus on the current mission.

## 17.3 Few Buttons

The user should not face too many options.

Primary actions:

- Start Mission
- Complete
- Postpone
- Reject
- Explain

## 17.4 Strong Hierarchy

The most important information must be visually obvious.

The user should understand the page in less than 5 seconds.

## 17.5 Premium Dark Design

Suggested visual identity:

- deep black background;
- glass cards;
- soft borders;
- white/off-white text;
- electric blue accents;
- subtle violet accents;
- copper/orange only for important actions.

---

# 18. Design Direction

Gigi OS should feel like:

```text
A calm command center for builders.
```

It should not feel like:

```text
A colorful task manager.
```

## Keywords

```text
premium
focused
dark
cinematic
minimal
intelligent
calm
precise
```

## Emotional Goal

When the user opens the app, they should feel:

```text
I know exactly what I need to do.
```

---

# 19. Technical Direction

The first real app can be built with:

```text
Next.js
TypeScript
Tailwind CSS
Supabase
PostgreSQL
OpenAI API or compatible LLM provider
```

However, the MVP can start without complex AI.

The first Decision Engine can be deterministic with transparent scoring.

AI should be added after the core product logic is validated.

## Suggested Architecture

```text
app/
components/
lib/
modules/
data/
docs/
```

## Suggested Modules

```text
modules/projects
modules/missions
modules/decision-engine
modules/memory
modules/history
modules/settings
```

---

# 20. Data Model Draft

## projects

```text
id
name
description
vision
status
category
progress
priority
business_potential
risk_level
estimated_effort
next_action
current_blocker
created_at
updated_at
```

## missions

```text
id
project_id
title
description
estimated_duration
expected_impact
reason
status
created_at
started_at
completed_at
```

## decisions

```text
id
mission_id
selected_project_id
score
reason
alternatives_json
created_at
```

## history_events

```text
id
event_type
project_id
mission_id
description
created_at
```

## user_settings

```text
id
north_star
monthly_revenue_target
preferred_work_duration
created_at
updated_at
```

---

# 21. AI Role

AI must not be used as decoration.

AI should only be used when it improves:

- reasoning;
- decision quality;
- project summaries;
- mission generation;
- explanation;
- long-term memory.

## MVP AI Usage

Optional.

For the MVP, AI can help generate:

- mission descriptions;
- decision explanations;
- project summaries.

But the core prioritization should remain understandable and controllable.

## Future AI Usage

Future versions can include:

- CEO module;
- Developer module;
- Marketing module;
- Designer module;
- Finance module;
- Automation module;
- Research module.

These should be treated as modules inside the OS, not as separate random agents.

---

# 22. Product Modules

## 22.1 Brain Module

Responsible for:

- prioritization;
- recommendations;
- strategic reasoning;
- mission generation;
- decision explanation.

## 22.2 Projects Module

Responsible for:

- project creation;
- project status;
- project progress;
- next actions;
- blockers.

## 22.3 Mission Module

Responsible for:

- today’s mission;
- mission state;
- mission completion;
- mission history.

## 22.4 Memory Module

Responsible for:

- preserving decisions;
- recording history;
- preventing repeated thinking.

## 22.5 Future Team Module

Responsible for AI roles:

- CEO;
- Developer;
- Designer;
- Marketing;
- Business;
- Finance;
- Automation;
- Legal.

Not part of MVP.

---

# 23. Product Rules

## Rule 1

If a feature does not help the user decide or execute, it does not belong in the MVP.

## Rule 2

The product must always show one clear priority.

## Rule 3

Every project must always have a next action.

## Rule 4

Every mission must be explainable.

## Rule 5

The user can reject Gigi’s recommendation.

## Rule 6

Rejected missions must be remembered.

## Rule 7

The system should not punish the user for changing plans, but it should explain the tradeoff.

## Rule 8

Gigi OS should be allowed to say:

```text
Not now.
```

---

# 24. Acceptance Criteria for MVP

The MVP is successful if:

- the user can create projects;
- each project can store a next action;
- Gigi OS can recommend one mission;
- the recommendation includes a clear explanation;
- the user can start and complete a mission;
- completed missions are stored in history;
- project progress can be updated;
- the user feels less confused after opening the app.

The MVP fails if:

- the user sees too many choices;
- the app becomes a generic task manager;
- the decision logic is unclear;
- the user still has to decide manually between all projects;
- the app focuses on dashboards instead of action.

---

# 25. Initial Roadmap

## V0.1 — Documentation

Goal:

Create the full product foundation.

Includes:

- README
- Master PRD
- product philosophy
- decision rules
- MVP scope
- design direction

## V0.2 — Static Prototype

Goal:

Create a non-functional interface prototype.

Includes:

- Mission screen
- Projects screen
- Brain screen
- History screen

## V0.3 — Local MVP

Goal:

Make the prototype usable locally.

Includes:

- create projects;
- store projects locally;
- generate mission with simple scoring;
- complete mission;
- view history.

## V0.4 — Database MVP

Goal:

Persist data properly.

Includes:

- Supabase;
- authentication;
- database schema;
- project persistence;
- mission persistence.

## V0.5 — AI Assisted MVP

Goal:

Add AI reasoning carefully.

Includes:

- AI mission generation;
- AI explanation;
- AI weekly summary.

## V1.0 — First Daily Use Version

Goal:

Gigi OS becomes useful every morning.

Includes:

- stable mission system;
- strong project memory;
- simple settings;
- clean design;
- reliable history;
- daily workflow.

---

# 26. Future Vision

Future versions may include:

## GitHub Integration

Gigi OS reads repositories and understands project progress.

## Cursor Integration

Gigi OS prepares prompts and development tasks.

## n8n Integration

Gigi OS triggers automations.

## Gmail Integration

Gigi OS summarizes important emails.

## Calendar Integration

Gigi OS plans missions around available time.

## Finance Module

Gigi OS tracks revenue, costs and financial targets.

## Voice Interface

The user can say:

```text
Gigi, I have two hours. What should I do?
```

And Gigi answers with the best mission.

## Multi-user SaaS

Gigi OS becomes available to other entrepreneurs.

---

# 27. First Build Instruction for Cursor

Cursor must not start by building the full product.

Cursor must first create a clean documentation and prototype foundation.

## First Cursor Objective

Create the initial project structure:

```text
docs/
  MASTER_PRD.md
  ROADMAP.md
  DECISION_ENGINE.md
  DESIGN.md
  ARCHITECTURE.md

app/
  placeholder

README.md
```

Then create a first static UI prototype with four screens:

```text
Mission
Projects
Brain
History
```

No authentication.

No database.

No external API.

No AI calls.

Only a clean static prototype.

---

# 28. Final Product Statement

Gigi OS exists to help builders execute.

Its job is not to answer everything.

Its job is to choose what matters.

The product should always protect the user from chaos, distraction and unnecessary decisions.

The best version of Gigi OS is not the one with the most features.

It is the one that helps the user move forward every day.

> **Know what matters next.**
