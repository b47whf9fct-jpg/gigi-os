# Gigi OS — Memory System

> **Never restart the same thinking twice.**

Version: `0.1`  
Status: Product Specification  
Module: Memory System  
Owner: Germain Caplain  
Purpose: Define how Gigi OS remembers projects, decisions, missions, context and execution history.

---

# 1. Purpose

The Memory System is the long-term context layer of Gigi OS.

Its role is to make sure Gigi OS does not forget:

- what projects exist;
- why they exist;
- what has already been done;
- what decisions were made;
- what missions were completed;
- what missions were rejected;
- what blockers exist;
- what the user is trying to achieve;
- what matters next.

Gigi OS must not behave like a chatbot that starts from zero every time.

It must behave like an operating system that remembers the state of the user’s work.

---

# 2. Core Philosophy

Memory exists for one reason:

> **To improve future decisions.**

Gigi OS should not remember everything randomly.

It should remember what helps:

- prioritize better;
- avoid repeated thinking;
- understand project history;
- detect patterns;
- prevent distraction;
- explain decisions;
- measure progress.

Memory is not decoration.

Memory is part of the decision engine.

---

# 3. Main Problem Solved

Without memory, the user has to repeatedly explain:

```text
What is Buildy Clear?
Where are we on Buildy Crafts?
Why is Linko paused?
What was the next action?
Why did we postpone this mission?
What was decided last week?
```

This creates friction.

Gigi OS must remove that friction.

The user should be able to open Gigi OS and the system already knows the current context.

---

# 4. Memory Principles

## 4.1 Memory Must Be Useful

Gigi OS should only store information that improves execution.

Bad memory:

```text
The user liked a random color today.
```

Good memory:

```text
Buildy Clear is the closest project to short-term revenue and should remain the main priority until the sales funnel is launched.
```

---

## 4.2 Memory Must Be Structured

Memory should not be a pile of notes.

It must be organized into clear categories:

```text
projects
missions
decisions
history
blockers
goals
preferences
lessons
```

---

## 4.3 Memory Must Be Explainable

The system must be able to explain:

```text
Why do I remember this?
How does it affect the recommendation?
When was it recorded?
Which project does it affect?
```

---

## 4.4 Memory Must Reduce Repetition

If the user already made a decision, Gigi OS should not ask the same question again unless something changed.

Example:

```text
Linko is paused because it is not the fastest path to short-term revenue.
```

Gigi OS should remember that and not keep recommending Linko every day.

---

## 4.5 Memory Must Support Focus

Memory should help Gigi OS say:

```text
Not now.
```

Example:

```text
You already decided that Buildy Clear is the short-term revenue priority. Starting another creative project today would go against the current plan.
```

---

# 5. What Gigi OS Must Remember

## 5.1 Project Memory

For each project, Gigi OS must remember:

```text
project name
vision
current status
progress
priority
next action
blockers
history
last update
reason for current priority
```

Example:

```text
Buildy Clear is an active digital product. It is near launch and has short-term revenue potential. Current blocker: sales tunnel not fully optimized.
```

---

## 5.2 Mission Memory

For each mission, Gigi OS must remember:

```text
mission title
related project
status
reason
estimated duration
completion state
feedback
history
```

Example:

```text
Mission completed: Create the README for Gigi OS.
```

---

## 5.3 Decision Memory

For each decision, Gigi OS must remember:

```text
selected mission
selected project
score
reason
alternatives considered
why alternatives were not selected
user response
date
```

Example:

```text
Decision: Buildy Clear was prioritized over Buildy Crafts because the current objective was short-term revenue.
```

---

## 5.4 Goal Memory

Gigi OS must remember the user’s current high-level goals.

Examples:

```text
Reach 300–500 € per month quickly.
Build long-term software products.
Use Gigi OS to manage all projects.
Avoid dispersion between too many ideas.
```

---

## 5.5 Blocker Memory

Gigi OS must remember blockers.

Examples:

```text
Buildy Clear: sales tunnel incomplete.
Buildy Crafts: large content library still needs expansion.
Linko: early stage and not ready for monetization.
Gigi OS: documentation must be completed before development.
```

---

## 5.6 Preference Memory

Gigi OS may remember stable work preferences that improve execution.

Examples:

```text
The user prefers clear next actions.
The user works better with strong structure.
The user wants direct guidance instead of vague options.
The user likes premium dark interfaces.
```

Preference memory must remain useful and non-invasive.

---

## 5.7 Lesson Memory

Gigi OS should remember lessons learned from past work.

Examples:

```text
Large vague tasks are less effective than short missions.
Starting new projects too quickly can slow down existing projects.
A project close to launch should usually be finished before starting a new one.
```

---

# 6. What Gigi OS Should Not Remember

Gigi OS should not store:

- random personal details;
- emotional comments that do not help execution;
- sensitive information without a clear reason;
- temporary frustration as permanent truth;
- irrelevant conversation fragments;
- private data that does not support project decisions.

Memory must serve the product.

Not curiosity.

---

# 7. Memory Categories

The Memory System should organize memories into categories.

## 7.1 Project State

Current facts about projects.

Example:

```text
Buildy Clear is active and near launch.
```

## 7.2 Strategic Decisions

Important decisions that affect priorities.

Example:

```text
For the short term, Buildy Clear is prioritized over Linko because it can generate revenue faster.
```

## 7.3 Execution History

What was done.

Example:

```text
README.md was created for Gigi OS.
```

## 7.4 User Goals

Current targets.

Example:

```text
Reach 500 €/month first, then scale larger projects.
```

## 7.5 Blockers

Things preventing progress.

Example:

```text
Cursor credits are limited.
```

## 7.6 Working Preferences

Stable preferences that improve recommendations.

Example:

```text
The user prefers one clear priority instead of many options.
```

## 7.7 Product Rules

Rules that must guide future work.

Example:

```text
Gigi OS MVP must not include Gmail, Calendar, n8n or advanced agents.
```

---

# 8. Memory Lifecycle

A memory can have different lifecycle states.

```text
active
outdated
archived
superseded
deleted
```

## 8.1 Active

Currently relevant.

## 8.2 Outdated

May no longer be true.

## 8.3 Archived

No longer used for current decisions, but kept for history.

## 8.4 Superseded

Replaced by a newer memory.

## 8.5 Deleted

Removed intentionally.

---

# 9. Memory Freshness

Some memories expire.

Some memories are stable.

## 9.1 Stable Memory

Examples:

```text
Gigi OS philosophy
project vision
product principles
design direction
```

## 9.2 Dynamic Memory

Examples:

```text
current priority
project progress
next action
monthly revenue target
blockers
```

Dynamic memory should be reviewed regularly.

---

# 10. Memory Review

Gigi OS should periodically review memory.

## Daily Review

Used for:

```text
current mission
active blockers
today’s priority
```

## Weekly Review

Used for:

```text
project status
progress changes
stale projects
repeated blockers
```

## Monthly Review

Used for:

```text
North Star
strategic priorities
paused projects
future projects
```

---

# 11. Decision Memory

Decision memory is one of the most important parts of Gigi OS.

Every important recommendation must create a decision record.

## Required Decision Memory Fields

```text
id
selected_project_id
selected_mission_id
decision_reason
score
alternatives_considered
user_response
created_at
```

## Example

```text
Selected project:
Buildy Clear

Selected mission:
Finish the sales page.

Reason:
Buildy Clear has the strongest short-term revenue potential and is closest to launch.

Alternatives:
Buildy Crafts, Linko, Gigi OS

User response:
accepted
```

---

# 12. Why Decision Memory Matters

Decision memory allows Gigi OS to say:

```text
We already decided this.
```

Example:

If the user asks to start a new project while Buildy Clear is unfinished, Gigi OS can respond:

```text
This is a good idea, but not now. The current plan is to finish Buildy Clear first because it is closest to short-term revenue.
```

This is not stubbornness.

It is strategic continuity.

---

# 13. Mission Memory

Mission memory stores execution.

Each mission should create history events.

## Mission Events

```text
mission_created
mission_started
mission_completed
mission_postponed
mission_rejected
mission_expired
mission_split
```

## Example

```text
mission_completed:
Create docs/DECISION_ENGINE.md
```

---

# 14. Project Memory

Project memory stores the evolving state of each project.

## Project Events

```text
project_created
project_updated
status_changed
priority_changed
progress_changed
next_action_changed
blocker_added
blocker_removed
project_paused
project_archived
project_completed
```

## Example

```text
Gigi OS status changed from idea to active.
```

---

# 15. Blocker Memory

Blockers must be stored clearly because they affect decisions.

## Blocker Fields

```text
id
project_id
title
description
severity
status
created_at
resolved_at
```

## Severity

```text
low
medium
high
critical
```

## Status

```text
open
in_progress
resolved
ignored
```

Example:

```text
Blocker:
Gigi OS has no full product documentation yet.

Severity:
high

Resolution mission:
Create the core documentation files.
```

---

# 16. User Pattern Memory

Future versions of Gigi OS should detect working patterns.

Examples:

```text
The user completes shorter missions more often.
The user starts new ideas when blocked.
The user prefers concrete instructions.
The user loses time when too many options are visible.
```

This memory should improve mission recommendations.

Example:

```text
Because you often complete missions under 60 minutes, I recommend a 45-minute mission today.
```

---

# 17. Memory and Personalization

Memory should make Gigi OS feel personal without becoming creepy.

Good personalization:

```text
You usually work better with one clear next action, so I am hiding secondary tasks.
```

Bad personalization:

```text
You seemed anxious yesterday, so I changed your plan.
```

Gigi OS should use observable work patterns, not emotional assumptions.

---

# 18. Memory Priority

Not all memories are equally important.

## Priority Levels

```text
critical
high
medium
low
archive
```

## Critical Memory

Affects today’s decision directly.

Example:

```text
The current short-term objective is 500 €/month.
```

## High Memory

Important for current projects.

Example:

```text
Buildy Clear is near launch.
```

## Medium Memory

Useful context.

Example:

```text
Le Dernier Souvenir is a future creative project.
```

## Low Memory

Nice to know, but not decision-critical.

## Archive

Historical only.

---

# 19. Memory Retrieval

When Gigi OS decides what to recommend, it should retrieve:

```text
current North Star
active projects
current project statuses
recent decisions
open blockers
recent mission feedback
user available time
```

It should not retrieve everything.

Memory retrieval must be focused.

---

# 20. Memory Summaries

Long history should be summarized.

Example:

Instead of storing and reading 100 raw events every time, Gigi OS can create a project summary:

```text
Buildy Clear summary:
Digital product nearly ready to sell. Main objective is to finish the sales tunnel and create traffic videos. Short-term revenue potential is high.
```

Summaries should be updated when major events happen.

---

# 21. Memory Conflicts

Sometimes memory will conflict.

Example:

Old memory:

```text
Linko is the main priority.
```

New memory:

```text
Buildy Clear is the main short-term priority.
```

Gigi OS must handle this by marking older memory as superseded.

The newest strategic decision should win unless manually overridden.

---

# 22. Memory Editing

The user must be able to correct memory.

Required actions:

```text
edit memory
archive memory
delete memory
mark memory as outdated
pin memory
```

Pinned memory should have stronger influence.

Example:

```text
Pinned:
The MVP must stay simple.
```

---

# 23. Memory Privacy

Gigi OS must treat memory carefully.

Principles:

```text
The user owns their memory.
Memory should be visible.
Memory should be editable.
Memory should be deletable.
Memory should not be hidden from the user.
```

Future SaaS versions must make memory management transparent.

---

# 24. MVP Memory Scope

The MVP does not need advanced AI memory.

The first version only needs structured memory.

## MVP Must Remember

```text
projects
missions
mission status
completed missions
rejected missions
postponed missions
decision reasons
basic history events
North Star
```

## MVP Does Not Need

```text
semantic search
vector database
automatic pattern detection
emails
calendar events
file analysis
voice history
AI long-term memory
```

---

# 25. Memory Data Model

## 25.1 memories

```text
id
type
title
content
priority
status
related_project_id
related_mission_id
created_at
updated_at
```

## 25.2 memory_events

```text
id
memory_id
event_type
description
created_at
```

## 25.3 decisions

```text
id
selected_project_id
selected_mission_id
score
reason
alternatives_json
user_response
created_at
```

## 25.4 history_events

```text
id
event_type
project_id
mission_id
description
metadata_json
created_at
```

## 25.5 blockers

```text
id
project_id
title
description
severity
status
created_at
resolved_at
```

---

# 26. Memory Types

Allowed memory types:

```text
project_state
strategic_decision
mission_history
blocker
user_goal
user_preference
product_rule
lesson
system_event
```

---

# 27. History Event Types

Allowed history events:

```text
project_created
project_updated
mission_created
mission_started
mission_completed
mission_postponed
mission_rejected
decision_created
blocker_added
blocker_resolved
goal_updated
memory_created
memory_updated
memory_archived
```

---

# 28. TypeScript Types Draft

```ts
export type MemoryType =
  | "project_state"
  | "strategic_decision"
  | "mission_history"
  | "blocker"
  | "user_goal"
  | "user_preference"
  | "product_rule"
  | "lesson"
  | "system_event";

export type MemoryPriority =
  | "critical"
  | "high"
  | "medium"
  | "low"
  | "archive";

export type MemoryStatus =
  | "active"
  | "outdated"
  | "archived"
  | "superseded"
  | "deleted";

export type Memory = {
  id: string;
  type: MemoryType;
  title: string;
  content: string;
  priority: MemoryPriority;
  status: MemoryStatus;
  relatedProjectId?: string;
  relatedMissionId?: string;
  createdAt: string;
  updatedAt: string;
};

export type HistoryEventType =
  | "project_created"
  | "project_updated"
  | "mission_created"
  | "mission_started"
  | "mission_completed"
  | "mission_postponed"
  | "mission_rejected"
  | "decision_created"
  | "blocker_added"
  | "blocker_resolved"
  | "goal_updated"
  | "memory_created"
  | "memory_updated"
  | "memory_archived";

export type HistoryEvent = {
  id: string;
  eventType: HistoryEventType;
  projectId?: string;
  missionId?: string;
  description: string;
  metadata?: Record<string, unknown>;
  createdAt: string;
};

export type BlockerSeverity =
  | "low"
  | "medium"
  | "high"
  | "critical";

export type BlockerStatus =
  | "open"
  | "in_progress"
  | "resolved"
  | "ignored";

export type Blocker = {
  id: string;
  projectId: string;
  title: string;
  description: string;
  severity: BlockerSeverity;
  status: BlockerStatus;
  createdAt: string;
  resolvedAt?: string;
};
```

---

# 29. Memory UI

The MVP does not need a complex Memory screen.

Memory should appear mainly through:

```text
History screen
Brain screen
Project detail screen
Mission explanation
```

Future versions may include a dedicated Memory app.

---

# 30. History Screen Requirements

The History screen must show:

```text
completed missions
rejected missions
postponed missions
decision records
project changes
blocker changes
goal changes
```

History should be readable and calm.

It should not feel like logs for developers.

It should feel like a timeline of progress.

Example:

```text
Today
Mission completed: Create docs/PROJECT_MODEL.md

Yesterday
Decision: Buildy Clear stayed priority because it is closest to revenue.
```

---

# 31. Brain Screen Memory Usage

The Brain screen must use memory to explain decisions.

Example:

```text
I selected Gigi OS documentation today because the project is currently blocked by missing specifications. Yesterday, the Decision Engine and Project Model were created. The next logical memory layer is the Memory System.
```

This creates continuity.

---

# 32. Memory and the Decision Engine

The Decision Engine must use memory to improve recommendations.

Examples:

If a mission was rejected as too large:

```text
Recommend a smaller version next time.
```

If a project has been stale for 14 days:

```text
Create a review mission.
```

If a project is near launch:

```text
Increase completion proximity score.
```

If the user repeatedly switches projects:

```text
Recommend focus on the current mission.
```

---

# 33. Memory and the Mission System

The Mission System must use memory to:

```text
avoid repeating completed missions
remember postponed missions
detect missions that are too large
track completion patterns
generate better next actions
```

Example:

```text
The last mission was completed successfully. The next mission should continue the same project unless a higher-priority blocker appears.
```

---

# 34. Memory and the Project System

The Project System must use memory to:

```text
show project history
track progress changes
store blockers
remember status changes
identify stale projects
```

Example:

```text
Buildy Clear has been active for 12 days and remains close to launch.
```

---

# 35. Memory Quality Rules

A memory is good if it is:

```text
specific
useful
current
connected to a project or goal
actionable or explanatory
```

A memory is bad if it is:

```text
vague
random
overly personal
not useful for decisions
duplicated
outdated
```

---

# 36. Example Memories

## 36.1 Good Memory

```text
Type:
strategic_decision

Title:
Buildy Clear is the short-term revenue priority.

Content:
Buildy Clear should remain the main short-term priority because it is near launch and can potentially generate the first 300–500 €/month faster than other projects.
```

---

## 36.2 Good Memory

```text
Type:
product_rule

Title:
Gigi OS MVP must stay focused.

Content:
The MVP must not include integrations such as Gmail, Google Calendar, GitHub or n8n. It must first prove the mission recommendation system.
```

---

## 36.3 Bad Memory

```text
The user said this was cool.
```

This is too vague.

---

## 36.4 Bad Memory

```text
The user was stressed.
```

This is not useful unless connected to an execution pattern and handled carefully.

---

# 37. Cursor Build Instructions

Cursor should implement the Memory System as a clean module.

Suggested structure:

```text
modules/memory/
  memoryTypes.ts
  memoryFixtures.ts
  createMemory.ts
  updateMemory.ts
  archiveMemory.ts
  createHistoryEvent.ts
  getRelevantMemories.ts
  summarizeProjectMemory.ts
```

For the first prototype:

```text
No database.
No AI.
No vector search.
No external API.
Use mock data.
Use local in-memory structures or fixtures.
```

---

# 38. MVP Acceptance Criteria

The Memory System MVP is successful if:

- completed missions are stored;
- rejected missions are stored;
- postponed missions are stored;
- decisions are stored with reasons;
- project updates create history events;
- the Brain screen can reference previous decisions;
- the History screen shows useful progress;
- Gigi OS does not repeat the same recommendation without context.

The MVP fails if:

- history is not saved;
- decision reasons disappear;
- rejected missions are forgotten;
- the user must repeat project context manually;
- memory becomes a random notes database;
- memory does not improve recommendations.

---

# 39. Future Memory Features

Future versions may include:

```text
semantic search
automatic project summaries
weekly memory review
long-term pattern detection
AI memory compression
memory conflict resolution UI
memory pinning
memory importance scoring
cross-project insights
```

---

# 40. Final Principle

Memory is not here to collect information.

Memory is here to create continuity.

Without memory, Gigi OS is just another assistant.

With memory, Gigi OS becomes a system.

A system that remembers what matters, protects focus and improves every decision over time.

> **Remember the work. Improve the next move.**
