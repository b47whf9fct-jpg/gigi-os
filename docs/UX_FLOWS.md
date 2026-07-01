# Gigi OS — UX Flows

> **Open Gigi. Know what matters. Execute.**

Version: `0.1`  
Status: Product Specification  
Module: UX / Product Experience  
Owner: Germain Caplain  
Purpose: Define the main user flows of Gigi OS MVP.

---

# 1. Purpose

This document defines the core user experience flows for Gigi OS.

The goal of the UX is not to show many features.

The goal is to guide the user toward the most important action.

Gigi OS must feel like a calm command center.

The user should open it and immediately understand:

```text
This is what I need to do now.
```

---

# 2. Core UX Principle

The core UX principle is:

> **Mission first. Everything else second.**

Gigi OS is not a dashboard-first product.

It is not a task-list-first product.

It is not a chat-first product.

It is a mission-first product.

The first screen should always answer:

```text
What matters next?
```

---

# 3. Main UX Goals

The UX must help the user:

- avoid decision fatigue;
- stop switching between projects randomly;
- understand the current priority;
- start a clear mission quickly;
- complete work with focus;
- see progress over time;
- trust Gigi’s recommendations.

---

# 4. MVP Screens

The MVP has four core screens:

```text
Mission
Projects
Brain
History
```

No extra screens should be added unless required.

---

# 5. Global Navigation

The MVP navigation should be simple.

Suggested navigation:

```text
Mission
Projects
Brain
History
```

The Mission screen must be the default screen.

The navigation should not compete with the mission.

---

# 6. First Launch Flow

## 6.1 Goal

Help the user set up Gigi OS quickly without creating friction.

The first launch flow should not feel like enterprise onboarding.

It should feel like Gigi is learning what matters.

---

## 6.2 Flow

```text
1. Welcome screen
2. Define North Star
3. Define short-term target
4. Add first projects
5. Confirm project data
6. Generate first mission
```

---

## 6.3 Welcome Screen

Purpose:

Explain Gigi OS in one sentence.

Suggested copy:

```text
Gigi OS helps you decide what to work on next.
```

Secondary copy:

```text
Add your projects, define your objective, and Gigi will recommend the highest-impact mission.
```

Primary action:

```text
Start setup
```

---

## 6.4 North Star Screen

Purpose:

Capture the user’s highest-level objective.

Suggested question:

```text
What is your North Star?
```

Examples:

```text
Reach 500 € per month from my projects.
Build profitable digital products.
Launch my first SaaS.
Grow my company with AI.
```

Required field:

```text
north_star
```

---

## 6.5 Short-Term Target Screen

Purpose:

Capture the current practical target.

Suggested question:

```text
What is your current target?
```

Examples:

```text
Generate 300–500 € per month.
Get the first sale.
Finish the MVP.
Launch the first product.
```

Required field:

```text
current_target
```

---

## 6.6 Add Projects Screen

Purpose:

Let the user add projects quickly.

Required fields:

```text
project_name
description
status
progress
next_action
business_potential
strategic_value
urgency
```

The user must be able to add at least one project.

The setup should not require perfect data.

Gigi OS can improve project data later.

---

## 6.7 Generate First Mission

After setup, Gigi OS runs the Decision Engine.

Output:

```text
first recommended mission
reason
estimated duration
expected impact
confidence
```

The user lands on the Mission screen.

---

# 7. Daily Use Flow

## 7.1 Goal

Let the user open Gigi OS and start working quickly.

---

## 7.2 Flow

```text
1. User opens Gigi OS
2. Mission screen appears
3. Gigi shows today’s mission
4. User reads reason
5. User starts, postpones or rejects
6. If started, Mission Mode opens
7. User completes mission
8. History is updated
9. Gigi recalculates next mission
```

---

# 8. Mission Screen Flow

## 8.1 Purpose

The Mission screen is the main screen of Gigi OS.

It must show only one primary mission.

---

## 8.2 Required Content

```text
mission title
project name
reason
estimated duration
expected impact
confidence
primary action
secondary actions
```

---

## 8.3 Example Layout

```text
Today's Mission

Finish the Buildy Clear sales page

Project:
Buildy Clear

Estimated time:
45 minutes

Expected impact:
High

Why this matters:
Buildy Clear is the closest project to generating short-term revenue.

Confidence:
87%

[ Start Mission ]

Postpone
Reject
Explain decision
```

---

## 8.4 Primary Action

The primary action is always:

```text
Start Mission
```

This button must be visually dominant.

---

## 8.5 Secondary Actions

Secondary actions:

```text
Postpone
Reject
Explain decision
```

These actions must be visible but less prominent.

---

# 9. Start Mission Flow

## 9.1 Trigger

User clicks:

```text
Start Mission
```

---

## 9.2 System Actions

The system must:

```text
1. Mark mission as started.
2. Create history event.
3. Enter Mission Mode.
4. Hide unrelated distractions.
```

---

# 10. Mission Mode Flow

## 10.1 Purpose

Mission Mode is the focused execution environment.

The goal is to help the user complete one mission without distraction.

---

## 10.2 Required Content

```text
mission title
project name
mission description
estimated duration
timer
steps
complete button
exit option
```

---

## 10.3 Example Layout

```text
Mission Mode

Buildy Clear

Rewrite the sales page headline and CTA.

Estimated time:
45 minutes

Steps:
[ ] Open Systeme.io
[ ] Go to the Buildy Clear sales page
[ ] Replace the headline
[ ] Replace the CTA
[ ] Save changes
[ ] Review the page

[ Complete Mission ]

Exit mission
```

---

## 10.4 Mission Mode Rules

Mission Mode must not show:

```text
other projects
new ideas
analytics
all tasks
unrelated navigation
complex settings
```

Mission Mode must show only what helps completion.

---

# 11. Complete Mission Flow

## 11.1 Trigger

User clicks:

```text
Complete Mission
```

---

## 11.2 System Actions

The system must:

```text
1. Mark mission as completed.
2. Save completion time.
3. Create history event.
4. Ask if project progress changed.
5. Update project data if needed.
6. Recalculate next mission.
```

---

## 11.3 Completion Screen

Suggested copy:

```text
Mission completed.

Progress recorded.

Gigi is recalculating what matters next.
```

Possible next action:

```text
View next mission
```

---

# 12. Postpone Mission Flow

## 12.1 Trigger

User clicks:

```text
Postpone
```

---

## 12.2 System Question

Gigi asks:

```text
Why postpone this mission?
```

Options:

```text
Not enough time
Low energy
Blocked
Not today
Waiting for something
Other
```

Optional field:

```text
postpone_until
```

---

## 12.3 System Actions

The system must:

```text
1. Mark mission as postponed.
2. Save reason.
3. Create history event.
4. Recalculate recommendation.
```

---

## 12.4 UX Rule

Postponing should feel allowed.

Gigi OS should not shame the user.

But if the same mission is postponed repeatedly, Gigi should detect a blocker.

---

# 13. Reject Mission Flow

## 13.1 Trigger

User clicks:

```text
Reject
```

---

## 13.2 System Question

Gigi asks:

```text
Why is this not the right mission?
```

Options:

```text
Wrong priority
Already done
Too vague
Too large
Not relevant
Blocked
Other
```

---

## 13.3 System Actions

The system must:

```text
1. Mark mission as rejected.
2. Save rejection reason.
3. Create history event.
4. Update decision memory.
5. Recalculate next mission.
```

---

## 13.4 UX Rule

Rejecting a mission must improve the system.

A rejected mission should never disappear without memory.

---

# 14. Explain Decision Flow

## 14.1 Trigger

User clicks:

```text
Explain decision
```

---

## 14.2 Destination

The user opens the Brain screen.

---

## 14.3 Brain Screen Content

The Brain screen must show:

```text
selected mission
selected project
score
decision criteria
alternatives considered
why other projects were not selected
related memories
```

---

## 14.4 Example Copy

```text
Why this mission?

Buildy Clear was selected because it is close to launch, has direct short-term revenue potential, and the next action is clear.

Other projects considered:

Buildy Crafts:
Strategic, but longer-term.

Linko:
Promising, but too early for monetization.

1Millimètre:
Experimental and not aligned with the current financial target.
```

---

# 15. Projects Screen Flow

## 15.1 Purpose

Let the user understand the state of all projects without overwhelming them.

---

## 15.2 Required Content

Each project card must show:

```text
project name
status
progress
priority
next action
blocker
business potential
```

---

## 15.3 Example Project Card

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

Blocker:
Sales tunnel not fully optimized

Potential:
Short-term revenue
```

---

## 15.4 Actions

The user can:

```text
view project
edit project
change status
update progress
edit next action
add blocker
```

---

# 16. Create Project Flow

## 16.1 Trigger

User clicks:

```text
Add Project
```

---

## 16.2 Required Fields

```text
name
description
category
status
progress
next_action
business_potential
strategic_value
urgency
```

---

## 16.3 UX Rule

Project creation must take less than 2 minutes.

The user should not need perfect information.

The system can accept approximate values.

---

## 16.4 After Creation

The system must:

```text
1. Save project.
2. Create history event.
3. Recalculate mission recommendation.
```

---

# 17. Edit Project Flow

## 17.1 Trigger

User opens a project and clicks:

```text
Edit
```

---

## 17.2 Editable Fields

```text
description
vision
status
progress
priority
next_action
current_blocker
scores
```

---

## 17.3 System Actions

The system must:

```text
1. Save changes.
2. Create project history event.
3. Update memory if needed.
4. Recalculate priorities if relevant.
```

---

# 18. Brain Screen Flow

## 18.1 Purpose

Make Gigi OS explainable.

The user should trust the recommendation because they understand it.

---

## 18.2 Required Sections

```text
Current recommendation
Scoring breakdown
Alternatives considered
Memory used
Decision reasoning
Tradeoff explanation
```

---

## 18.3 Example Layout

```text
Brain

Current recommendation:
Finish Buildy Clear sales page

Score:
87%

Why:
Closest to short-term revenue and near launch.

Scoring:
Business impact: 9
Alignment: 9
Completion proximity: 10
Urgency: 8
Clarity: 9
Effort efficiency: 8
Risk of delay: 6

Alternatives:
Buildy Crafts — important but longer-term
Linko — strategic but paused
Gigi OS — active but not revenue-first today
```

---

# 19. History Screen Flow

## 19.1 Purpose

Show continuity and progress.

The History screen must help the user see that work is moving forward.

---

## 19.2 Required Content

```text
completed missions
started missions
postponed missions
rejected missions
project changes
decisions
blockers
goal updates
```

---

## 19.3 Example Layout

```text
Today

Mission completed:
Create docs/MEMORY_SYSTEM.md

Decision:
Gigi OS documentation stayed priority because development should not start before the core specs are complete.

Yesterday

Mission completed:
Create docs/PROJECT_MODEL.md
```

---

# 20. Empty States

## 20.1 No Projects

```text
Before Gigi can choose your next mission, add your first project.
```

Primary action:

```text
Add Project
```

---

## 20.2 No Mission

```text
No mission is available yet.
```

Possible reasons:

```text
No active project
No next action
All missions postponed
Project data incomplete
```

Primary action:

```text
Review Projects
```

---

## 20.3 No History

```text
Your execution history will appear here once missions are started.
```

---

# 21. Error States

## 21.1 Missing Next Action

```text
This project has no next action. Gigi cannot prioritize vague work.
```

Primary action:

```text
Add next action
```

---

## 21.2 Mission Too Large

```text
This mission is too large to execute in one session.
```

Primary action:

```text
Split mission
```

---

## 21.3 Decision Confidence Low

```text
Gigi needs clearer project data to recommend the best mission.
```

Primary action:

```text
Review project data
```

---

# 22. UX Tone

Gigi should sound:

```text
calm
clear
direct
strategic
supportive
focused
```

Gigi should not sound:

```text
cute
childish
overly motivational
corporate
cold
vague
```

---

# 23. Example Gigi Voice

Good:

```text
Buildy Clear is the best mission today because it is closest to short-term revenue.
```

Bad:

```text
You got this! Let's crush your goals today!
```

Good:

```text
Not now. This idea is interesting, but it would distract from the current launch objective.
```

Bad:

```text
Sure, let's start another project!
```

---

# 24. Interaction Rules

## Rule 1

Always show one primary action.

## Rule 2

Never show too many equal choices.

## Rule 3

Every recommendation must be explainable.

## Rule 4

Every rejection must be remembered.

## Rule 5

Every mission completion must create history.

## Rule 6

The interface should reduce pressure, not increase it.

---

# 25. MVP UX Acceptance Criteria

The MVP UX is successful if:

- the user opens the app and sees one mission;
- the user understands why that mission matters;
- the user can start the mission quickly;
- Mission Mode feels focused;
- the user can complete, postpone or reject a mission;
- project state is understandable;
- history shows progress;
- the Brain screen explains decisions clearly.

The MVP UX fails if:

- the user sees too many options;
- the first screen feels like a dashboard;
- missions feel vague;
- navigation distracts from execution;
- the user still has to decide manually what matters;
- the interface feels like a generic task manager.

---

# 26. Cursor Build Instructions

Cursor should create static UI flows for:

```text
Mission screen
Mission Mode
Projects screen
Project detail
Brain screen
History screen
First launch setup
```

For the first prototype:

```text
No database
No authentication
No AI calls
No external APIs
Mock data only
Static interactions allowed
```

Suggested structure:

```text
app/
  page.tsx
  mission/
  projects/
  brain/
  history/

components/
  MissionCard.tsx
  ProjectCard.tsx
  ScoreBreakdown.tsx
  HistoryTimeline.tsx
  MissionMode.tsx

modules/
  projects/
  missions/
  decision-engine/
  memory/
```

---

# 27. Final Principle

The best UX for Gigi OS is not the one with the most screens.

It is the one that makes the next action obvious.

The user should never feel lost inside Gigi OS.

They should feel guided.

> **Less browsing. More building.**
