# Gigi OS — Project Model

> **Every project must always have a next action.**

Version: `0.1`  
Status: Product Specification  
Module: Project System  
Owner: Germain Caplain  
Purpose: Define how Gigi OS stores, understands, evaluates and prioritizes projects.

---

# 1. Purpose

The Project Model defines how Gigi OS represents projects.

A project is not just a folder.

A project is a living system with:

- a vision;
- a goal;
- a current state;
- a progress level;
- a next action;
- blockers;
- business potential;
- strategic value;
- decision history.

The Project Model exists so Gigi OS can compare projects and recommend the most important mission.

---

# 2. Core Definition

A project is:

> **A structured initiative that requires multiple missions to reach a meaningful outcome.**

A project can be:

- a software product;
- a digital product;
- a platform;
- a game;
- a creative series;
- an internal tool;
- a business experiment.

Examples:

```text
Buildy Crafts
Buildy Clear
Linko
1Millimètre
Le Dernier Souvenir
Gigi OS
```

---

# 3. What a Project Is Not

A project is not:

- a random idea;
- a single task;
- a note;
- a reminder;
- an emotion;
- a vague intention.

Bad project:

```text
Make money online.
```

Good project:

```text
Buildy Clear — a digital kit that helps homeowners verify construction quotes before signing.
```

---

# 4. Project Philosophy

Gigi OS must prevent project chaos.

The user may have many ideas, but not every idea should become an active project.

Projects must be classified clearly.

This allows the user to focus without losing ideas.

Gigi OS should never make the user feel that pausing a project means abandoning it.

---

# 5. Project Status

Every project must have one status.

## 5.1 Active

The project is currently allowed to receive missions.

Example:

```text
Buildy Clear
```

## 5.2 Paused

The project is important but not currently the focus.

Paused projects may appear in reviews, but should not usually generate daily missions unless reactivated.

Example:

```text
1Millimètre
```

## 5.3 Future

The project is an idea or opportunity for later.

Future projects should be stored but not actively prioritized.

Example:

```text
Le Dernier Souvenir
```

## 5.4 Archived

The project is no longer relevant.

Archived projects should not generate missions.

## 5.5 Completed

The project reached its intended outcome.

Completed projects should remain in history.

---

# 6. Project Categories

Projects can belong to categories.

Suggested categories:

```text
software
digital_product
platform
game
content
creative_project
internal_tool
business_experiment
automation
research
```

Examples:

```text
Buildy Crafts -> software
Buildy Clear -> digital_product
Linko -> platform
1Millimètre -> game
Le Dernier Souvenir -> creative_project
Gigi OS -> internal_tool / software
```

---

# 7. Project Priority

Each project must have a priority level.

Priority is not the same as status.

A paused project can still have high strategic value.

## Priority Values

```text
critical
high
medium
low
none
```

## Priority Meaning

### Critical

Must receive attention now.

Example:

```text
Buildy Clear if the current goal is to generate 500 €/month quickly.
```

### High

Important and active, but not always today's mission.

Example:

```text
Buildy Crafts.
```

### Medium

Useful, but can wait.

Example:

```text
Linko during early validation.
```

### Low

Interesting but not urgent.

Example:

```text
Le Dernier Souvenir before launch.
```

### None

Archived, completed or inactive.

---

# 8. Project Progress

Progress is a number from `0` to `100`.

Progress is not perfect.

It is an estimate used for prioritization.

## Progress Bands

```text
0–10   = idea
11–30  = early concept
31–60  = building
61–80  = advanced
81–95  = near launch
96–100 = launched or completed
```

Examples:

```text
Buildy Clear: 90–95%
Buildy Crafts: 65–80%
Linko: 15–25%
1Millimètre: 20–35%
Le Dernier Souvenir: 5–10%
Gigi OS: 1–10%
```

---

# 9. Project Fields

Each project must contain the following fields:

```text
id
name
slug
description
vision
status
category
progress
priority
business_potential
strategic_value
urgency
risk_level
estimated_effort
clarity
next_action
current_blocker
last_worked_on
created_at
updated_at
```

---

# 10. Field Definitions

## 10.1 id

Unique identifier.

Example:

```text
project_buildy_clear
```

## 10.2 name

Human-readable project name.

Example:

```text
Buildy Clear
```

## 10.3 slug

URL-friendly name.

Example:

```text
buildy-clear
```

## 10.4 description

Short explanation of the project.

Example:

```text
A digital kit that helps homeowners verify construction quotes before signing.
```

## 10.5 vision

Long-term ambition of the project.

Example:

```text
Become the easiest way for homeowners to avoid unclear construction quotes and costly mistakes.
```

## 10.6 status

Current project state.

Allowed values:

```text
active
paused
future
archived
completed
```

## 10.7 category

Project type.

Allowed examples:

```text
software
digital_product
platform
game
creative_project
internal_tool
```

## 10.8 progress

Estimated completion percentage.

Value:

```text
0–100
```

## 10.9 priority

Current priority level.

Allowed values:

```text
critical
high
medium
low
none
```

## 10.10 business_potential

How much the project can generate revenue.

Score:

```text
1–10
```

## 10.11 strategic_value

How important the project is long-term.

Score:

```text
1–10
```

## 10.12 urgency

How soon the project needs attention.

Score:

```text
1–10
```

## 10.13 risk_level

How risky the project is.

Score:

```text
1–10
```

High risk does not mean bad.

It means uncertain.

## 10.14 estimated_effort

Estimated effort required to reach the next major milestone.

Score:

```text
1–10
```

Low score = easy.

High score = heavy.

## 10.15 clarity

How clear the next action is.

Score:

```text
1–10
```

## 10.16 next_action

The next concrete action.

Example:

```text
Finish the Buildy Clear sales page.
```

## 10.17 current_blocker

What prevents progress.

Example:

```text
The sales tunnel is not fully finished.
```

## 10.18 last_worked_on

Date of last meaningful work.

## 10.19 created_at

Creation date.

## 10.20 updated_at

Last update date.

---

# 11. Project Lifecycle

A project follows this lifecycle:

```text
idea
future
active
paused
active
completed
archived
```

Not every project follows the full lifecycle.

A project can move backward.

Example:

```text
active -> paused
paused -> active
future -> active
active -> archived
```

---

# 12. Lifecycle Rules

## Rule 1 — New Ideas Start as Future

New ideas should not automatically become active projects.

This prevents distraction.

## Rule 2 — Active Projects Can Generate Missions

Only active projects should usually generate daily missions.

Paused projects can generate review missions but not execution missions.

## Rule 3 — Completed Projects Stay in Memory

Completed projects are not deleted.

They become part of the user’s execution history.

## Rule 4 — Archived Projects Do Not Generate Missions

Archived projects are stored but ignored by the Decision Engine.

## Rule 5 — A Project Without a Next Action Is Blocked

If a project has no next action, Gigi OS must mark it as unclear or blocked.

---

# 13. Project Health

Gigi OS should evaluate project health.

Project health helps detect problems.

## Health States

```text
healthy
unclear
blocked
stale
overloaded
ready_to_launch
```

## 13.1 Healthy

The project has:

- clear next action;
- recent progress;
- no major blocker.

## 13.2 Unclear

The project has no clear next action.

## 13.3 Blocked

The project cannot move forward without resolving an obstacle.

## 13.4 Stale

The project has not been worked on for a long time.

## 13.5 Overloaded

The project has too many open actions and needs simplification.

## 13.6 Ready to Launch

The project is close to being tested or sold.

---

# 14. Project Card Requirements

Each project card must show only the useful information.

Required fields:

```text
name
status
progress
priority
next_action
blocker
business_potential
```

Example:

```text
Buildy Clear

Status:
Active

Progress:
94%

Priority:
Critical

Next action:
Finish sales page

Potential:
Short-term revenue

Blocker:
Tunnel not finalized
```

---

# 15. Initial Project Examples

## 15.1 Buildy Clear

```text
Name:
Buildy Clear

Category:
digital_product

Status:
active

Progress:
94

Priority:
critical

Description:
A digital kit that helps homeowners verify unclear construction quotes before signing.

Vision:
Become the fastest and simplest way for homeowners to avoid costly mistakes on renovation quotes.

Business potential:
9

Strategic value:
7

Urgency:
9

Risk level:
4

Estimated effort:
3

Clarity:
9

Next action:
Finish the sales page and checkout flow.

Current blocker:
The sales tunnel is not fully optimized.
```

---

## 15.2 Buildy Crafts

```text
Name:
Buildy Crafts

Category:
software

Status:
active

Progress:
72

Priority:
high

Description:
A mobile app for artisans with quotes, projects, calculators, PDF exports and a construction material library.

Vision:
Become the reference app for artisans who want to create professional quotes and manage construction projects.

Business potential:
10

Strategic value:
10

Urgency:
6

Risk level:
7

Estimated effort:
8

Clarity:
7

Next action:
Continue stabilizing the product and expanding missing trade categories.

Current blocker:
Large content library still needs expansion.
```

---

## 15.3 Linko

```text
Name:
Linko

Category:
platform

Status:
paused

Progress:
22

Priority:
medium

Description:
A trust platform for the construction industry where customers can find serious artisans and companies can claim their profiles.

Vision:
Become the trust layer between customers and building professionals.

Business potential:
9

Strategic value:
9

Urgency:
4

Risk level:
8

Estimated effort:
9

Clarity:
5

Next action:
Finalize positioning and validate name availability.

Current blocker:
Too early for immediate monetization.
```

---

## 15.4 1Millimètre

```text
Name:
1Millimètre

Category:
game

Status:
paused

Progress:
28

Priority:
low

Description:
A mobile precision-cutting game based on stopping a saw at the perfect moment.

Vision:
Create a simple, addictive mobile game that can generate revenue through ads or a small paid price.

Business potential:
6

Strategic value:
5

Urgency:
3

Risk level:
7

Estimated effort:
6

Clarity:
6

Next action:
Improve core gameplay feeling and visual polish.

Current blocker:
Gameplay may not yet be addictive enough.
```

---

## 15.5 Le Dernier Souvenir

```text
Name:
Le Dernier Souvenir

Category:
creative_project

Status:
future

Progress:
5

Priority:
low

Description:
A short-form animated mystery series built around a small character recovering lost memories.

Vision:
Create a recognizable story universe that can grow into videos, games, books and merchandise.

Business potential:
7

Strategic value:
6

Urgency:
2

Risk level:
8

Estimated effort:
7

Clarity:
4

Next action:
Write the story bible and define the visual identity.

Current blocker:
No production system yet.
```

---

## 15.6 Gigi OS

```text
Name:
Gigi OS

Category:
internal_tool

Status:
active

Progress:
5

Priority:
high

Description:
An AI operating system that helps builders know what to work on next.

Vision:
Become the central brain for projects, decisions, missions and execution.

Business potential:
8

Strategic value:
10

Urgency:
7

Risk level:
7

Estimated effort:
8

Clarity:
8

Next action:
Complete the core product documentation.

Current blocker:
The product must be clearly specified before development.
```

---

# 16. Project Scoring

The Project Model provides data to the Decision Engine.

Project scoring uses:

```text
business_potential
strategic_value
urgency
progress
clarity
estimated_effort
risk_level
status
```

The Decision Engine then selects a mission.

The Project Model does not choose the mission by itself.

It only provides structured data.

---

# 17. Project Freshness

Gigi OS must know when a project becomes stale.

A project may be stale if:

```text
last_worked_on is older than 14 days
status is active
progress has not changed
next_action is unchanged
```

If a project is stale, Gigi OS can create a review mission.

Example:

```text
Review Buildy Crafts and define the next concrete action.
```

---

# 18. Project Blockers

A blocker is anything preventing progress.

Common blockers:

```text
missing_information
technical_issue
lack_of_time
lack_of_money
unclear_next_action
waiting_for_external_tool
low_confidence
too_large_scope
```

A project with a blocker should not always be deprioritized.

Sometimes the best mission is to remove the blocker.

Example:

```text
Clarify the payment setup for Buildy Clear.
```

---

# 19. Project Review

Gigi OS should support project review.

Review frequency:

```text
daily for critical projects
weekly for active projects
monthly for paused/future projects
```

Review questions:

```text
Is this project still aligned with the North Star?
Has progress changed?
Is the next action still valid?
Is there a blocker?
Should the status change?
Should the priority change?
```

---

# 20. Project Creation Flow

When the user creates a project, Gigi OS should ask only essential questions.

Required questions:

```text
What is the project name?
What is the project goal?
What type of project is it?
What is the current progress?
What is the next action?
What is blocking it?
How important is it for revenue?
How important is it long-term?
```

The creation flow must not feel heavy.

The user should be able to create a project in less than 2 minutes.

---

# 21. Project Editing Flow

The user must be able to edit:

```text
name
description
vision
status
progress
priority
next_action
current_blocker
scores
```

Every meaningful edit should be stored in history.

Example:

```text
Buildy Clear progress changed from 90% to 94%.
```

---

# 22. Project History

Each project must have a history.

History events:

```text
project_created
project_updated
status_changed
priority_changed
progress_changed
next_action_changed
blocker_added
blocker_removed
mission_completed
project_paused
project_archived
project_completed
```

History prevents repeated thinking.

---

# 23. Data Model

## 23.1 projects

```text
id
name
slug
description
vision
status
category
progress
priority
business_potential
strategic_value
urgency
risk_level
estimated_effort
clarity
next_action
current_blocker
health_status
last_worked_on
created_at
updated_at
```

---

## 23.2 project_history_events

```text
id
project_id
event_type
description
previous_value
new_value
created_at
```

---

## 23.3 project_scores

```text
id
project_id
business_potential
strategic_value
urgency
risk_level
estimated_effort
clarity
created_at
```

---

# 24. TypeScript Types Draft

```ts
export type ProjectStatus =
  | "active"
  | "paused"
  | "future"
  | "archived"
  | "completed";

export type ProjectPriority =
  | "critical"
  | "high"
  | "medium"
  | "low"
  | "none";

export type ProjectCategory =
  | "software"
  | "digital_product"
  | "platform"
  | "game"
  | "content"
  | "creative_project"
  | "internal_tool"
  | "business_experiment"
  | "automation"
  | "research";

export type ProjectHealth =
  | "healthy"
  | "unclear"
  | "blocked"
  | "stale"
  | "overloaded"
  | "ready_to_launch";

export type Project = {
  id: string;
  name: string;
  slug: string;
  description: string;
  vision: string;
  status: ProjectStatus;
  category: ProjectCategory;
  progress: number;
  priority: ProjectPriority;
  businessPotential: number;
  strategicValue: number;
  urgency: number;
  riskLevel: number;
  estimatedEffort: number;
  clarity: number;
  nextAction: string;
  currentBlocker?: string;
  healthStatus: ProjectHealth;
  lastWorkedOn?: string;
  createdAt: string;
  updatedAt: string;
};

export type ProjectHistoryEvent = {
  id: string;
  projectId: string;
  eventType:
    | "project_created"
    | "project_updated"
    | "status_changed"
    | "priority_changed"
    | "progress_changed"
    | "next_action_changed"
    | "blocker_added"
    | "blocker_removed"
    | "mission_completed"
    | "project_paused"
    | "project_archived"
    | "project_completed";
  description: string;
  previousValue?: string;
  newValue?: string;
  createdAt: string;
};
```

---

# 25. MVP Requirements

The MVP Project System must allow the user to:

```text
1. View projects.
2. Create a project.
3. Edit a project.
4. Set project status.
5. Set project progress.
6. Set project priority.
7. Set next action.
8. Set current blocker.
9. See project cards.
10. Provide project data to the Decision Engine.
```

The MVP does not require:

```text
team collaboration
file attachments
GitHub sync
calendar sync
advanced analytics
financial tracking
public sharing
multi-user permissions
```

---

# 26. UI Requirements

## 26.1 Projects Screen

The Projects screen must show a clean list of project cards.

Each card should include:

```text
Project name
Status
Progress
Priority
Next action
Blocker
Potential
```

The layout must remain calm and readable.

No overloaded dashboards.

---

## 26.2 Project Detail Screen

The project detail screen should include:

```text
Project vision
Description
Current status
Progress
Priority
Scores
Next action
Current blocker
Recent history
Related missions
```

For the MVP, this can be simplified.

---

## 26.3 Project Creation Screen

The creation screen should ask:

```text
Name
Description
Category
Status
Progress
Next action
Business potential
Strategic value
Urgency
```

It must be fast to complete.

---

# 27. Acceptance Criteria

The Project Model MVP is successful if:

- the user can create a structured project;
- each project has a clear status;
- each project has a next action;
- each project can be scored;
- the Decision Engine can compare projects;
- project progress can be updated;
- project history can be recorded;
- the user understands the state of each project quickly.

The MVP fails if:

- projects feel like random notes;
- projects have no next action;
- the user cannot tell which project matters;
- the system becomes a generic task manager;
- the project data is too vague for prioritization.

---

# 28. Cursor Build Instructions

Cursor should implement the Project System as a clean module.

Suggested structure:

```text
modules/projects/
  projectTypes.ts
  projectFixtures.ts
  projectUtils.ts
  createProject.ts
  updateProject.ts
  calculateProjectHealth.ts
  projectHistory.ts
```

The first implementation should use mock data.

No database.

No authentication.

No external API.

The goal is to make the product logic clear before adding infrastructure.

---

# 29. Initial Mock Projects

Cursor should create mock data for:

```text
Buildy Clear
Buildy Crafts
Linko
1Millimètre
Le Dernier Souvenir
Gigi OS
```

These mock projects will be used by:

```text
Projects screen
Mission screen
Decision Engine
Brain screen
History screen
```

---

# 30. Final Principle

A project inside Gigi OS is not just something the user wants to do.

It is something the system must understand well enough to prioritize.

If Gigi OS does not understand the project, it cannot recommend the right mission.

Therefore:

> **Every project needs a status, a goal, a next action and a reason to exist.**
