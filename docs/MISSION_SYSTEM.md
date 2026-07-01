# Gigi OS — Mission System

> **One objective. One mission. One step forward.**

Version: `0.1`  
Status: Product Specification  
Module: Mission System  
Owner: Germain Caplain  
Purpose: Define how Gigi OS transforms priorities into focused execution.

---

# 1. Purpose

The Mission System is the execution layer of Gigi OS.

The Decision Engine answers:

```text
What matters next?
```

The Mission System answers:

```text
How do we make the user execute it?
```

A mission is not a random task.

A mission is the single highest-value action selected by Gigi OS for the user right now.

The Mission System must protect the user from distraction, overload and vague work.

---

# 2. Core Definition

A mission is:

> **A clear, focused, time-bounded action that moves one project forward.**

A mission must be:

- specific;
- actionable;
- connected to a project;
- connected to a goal;
- short enough to start;
- important enough to matter;
- explainable.

A mission is not:

- a vague intention;
- a long project;
- a generic todo;
- a random idea;
- a reminder;
- a note.

---

# 3. Mission vs Task

Gigi OS must make a strong distinction between tasks and missions.

## 3.1 Task

A task is something that could be done.

Example:

```text
Improve the sales page.
```

## 3.2 Mission

A mission is the thing that should be done now.

Example:

```text
Rewrite the headline and main call-to-action of the Buildy Clear sales page.
```

A task can exist in a list.

A mission is selected by the system.

A task is passive.

A mission is active.

---

# 4. Mission Philosophy

The user should never open Gigi OS and see a wall of tasks.

The user should open Gigi OS and see one mission.

The product experience must always push toward execution.

Gigi OS must reduce thinking, not increase it.

The Mission System exists to make work feel:

```text
clear
possible
focused
important
```

---

# 5. Mission Rules

## Rule 1 — One Active Mission

There can only be one active mission at a time.

The user may have many projects and many future tasks, but only one mission should be active.

---

## Rule 2 — A Mission Must Be Actionable

Bad mission:

```text
Work on Buildy Clear.
```

Good mission:

```text
Replace the first section of the Buildy Clear sales page with a clearer promise and stronger CTA.
```

---

## Rule 3 — A Mission Must Be Short Enough to Start

A mission should usually take between:

```text
15 and 90 minutes
```

Longer work must be split into smaller missions.

Bad mission:

```text
Launch Buildy Clear.
```

Good missions:

```text
Finalize the sales page headline.
Connect the payment button.
Prepare 5 TikTok scripts.
Publish the first video.
```

---

## Rule 4 — A Mission Must Belong to a Project

Every mission must be connected to one project.

No mission should exist without a project.

---

## Rule 5 — A Mission Must Have a Reason

Every mission must explain why it matters.

Example:

```text
This mission matters because Buildy Clear is the closest project to generating short-term revenue.
```

---

## Rule 6 — A Mission Can Be Rejected

The user can reject a mission.

But the rejection must be saved.

Gigi OS must learn from repeated rejection.

---

## Rule 7 — A Mission Can Be Postponed

Postponing means:

```text
This is still valid, but not now.
```

Rejecting means:

```text
This recommendation is wrong or not useful.
```

The system must treat these differently.

---

# 6. Mission Lifecycle

A mission follows this lifecycle:

```text
available
started
completed
postponed
rejected
expired
```

## 6.1 Available

The mission has been generated and recommended, but the user has not started it yet.

## 6.2 Started

The user has accepted the mission and entered Mission Mode.

## 6.3 Completed

The user finished the mission.

## 6.4 Postponed

The user delayed the mission.

## 6.5 Rejected

The user refused the mission.

## 6.6 Expired

The mission is no longer relevant because the project changed.

---

# 7. Mission States

## 7.1 Available State

Required UI:

```text
Mission title
Project name
Estimated duration
Expected impact
Reason
Start button
Postpone option
Reject option
Explain option
```

---

## 7.2 Started State

When a mission is started, the app enters Mission Mode.

Mission Mode must reduce the interface to only what matters.

Required UI:

```text
Mission title
Project name
Step list
Timer
Complete button
Exit option
```

The user should not see other projects during Mission Mode.

---

## 7.3 Completed State

When a mission is completed, the system must:

```text
1. Mark mission as completed.
2. Add event to history.
3. Update project progress if required.
4. Trigger new decision calculation.
5. Suggest the next mission.
```

Completion message:

```text
Mission completed.

Progress recorded.

New mission available.
```

---

## 7.4 Postponed State

When the user postpones a mission, the system must ask:

```text
Why postpone this mission?
```

Possible reasons:

```text
not_enough_time
low_energy
blocked
not_today
waiting_for_something
other
```

The system must store:

```text
mission_id
postponed_until
reason
created_at
```

---

## 7.5 Rejected State

When the user rejects a mission, the system must ask:

```text
Why is this not the right mission?
```

Possible reasons:

```text
wrong_priority
already_done
too_vague
too_large
not_relevant
blocked
other
```

The system must store this feedback and use it later.

---

# 8. Mission Mode

Mission Mode is one of the most important experiences in Gigi OS.

It is the focused execution environment.

## 8.1 Purpose

Mission Mode exists to remove distractions.

When Mission Mode is active, the user should not be encouraged to browse projects, open dashboards or explore new ideas.

The only goal is to complete the mission.

---

## 8.2 Mission Mode UI

The interface should be minimal.

Example:

```text
MISSION MODE

Buildy Clear

Rewrite the headline and CTA of the sales page.

Estimated time:
45 min

Steps:
[ ] Open Systeme.io sales page
[ ] Replace headline
[ ] Replace CTA
[ ] Save changes
[ ] Review page

[ COMPLETE MISSION ]
```

---

## 8.3 Mission Mode Rules

Mission Mode should:

- hide unrelated projects;
- avoid notifications;
- avoid secondary navigation;
- show only essential steps;
- keep the user focused;
- make completion easy.

Mission Mode should not:

- display analytics;
- show all projects;
- suggest new ideas;
- open unrelated modules;
- overload the user with information.

---

# 9. Mission Quality

A good mission has five qualities.

## 9.1 Clear

The user understands it immediately.

## 9.2 Actionable

The user knows what to do.

## 9.3 Bounded

The mission is not endless.

## 9.4 Valuable

The mission moves a project forward.

## 9.5 Explainable

The system can explain why it was selected.

---

# 10. Mission Examples

## 10.1 Good Missions

```text
Rewrite the first screen of the Buildy Clear sales page.
```

```text
Create 10 short TikTok scripts for Buildy Clear.
```

```text
Add the missing charpente category to the Buildy Crafts roadmap.
```

```text
Write the first 5 episodes outline for Le Dernier Souvenir.
```

```text
Create the README and product vision for Gigi OS.
```

---

## 10.2 Bad Missions

```text
Work on marketing.
```

```text
Improve the app.
```

```text
Make money.
```

```text
Do Buildy.
```

```text
Think about Linko.
```

These are not missions.

They are vague intentions.

---

# 11. Mission Generation

A mission can be created from:

- a project’s next action;
- a Decision Engine recommendation;
- user input;
- a future AI module;
- a weekly planning session.

For the MVP, missions can be generated manually from project fields.

Example:

Project next action:

```text
Finish sales page.
```

Generated mission:

```text
Rewrite the headline, CTA and guarantee section of the Buildy Clear sales page.
```

---

# 12. Mission Splitting

If a mission is too large, Gigi OS must split it.

Large mission:

```text
Launch Buildy Clear.
```

Split into:

```text
1. Finish sales page.
2. Connect payment.
3. Test checkout.
4. Prepare 10 videos.
5. Publish first video.
6. Check analytics.
```

The system should recommend only the first mission.

---

# 13. Mission Duration

Missions should have estimated durations.

Suggested duration bands:

```text
micro: 5–15 minutes
short: 15–30 minutes
standard: 30–60 minutes
deep: 60–90 minutes
too_large: more than 90 minutes
```

If a mission is `too_large`, it should be split.

---

# 14. Mission Impact

Each mission should have an expected impact.

Impact levels:

```text
low
medium
high
critical
```

Impact is based on:

- revenue potential;
- strategic value;
- blocker removal;
- milestone progress;
- urgency;
- alignment with North Star.

---

# 15. Mission Confidence

Gigi OS should estimate confidence.

Confidence measures how sure the system is that this is the right mission.

Example:

```text
Confidence: 87%
```

Confidence should be lower when:

- project data is incomplete;
- next action is vague;
- user recently rejected similar missions;
- several projects have similar scores;
- user energy/time does not match the mission.

---

# 16. Mission Feedback

The user’s feedback is essential.

Feedback types:

```text
accepted
started
completed
postponed
rejected
ignored
```

The system must use feedback to improve future recommendations.

Examples:

If the user often rejects long missions:

```text
Recommend shorter missions.
```

If the user often completes revenue-focused missions:

```text
Prioritize similar high-impact missions.
```

If the user keeps postponing the same project:

```text
Detect blocker.
```

---

# 17. Blocker Detection

A mission may reveal a blocker.

Signals:

```text
Mission postponed 3+ times
Mission rejected as blocked
Project has no next action
Mission too vague
Mission too large
No progress for several days
```

When a blocker is detected, Gigi OS should create a blocker-resolution mission.

Example:

```text
Clarify the next action for Buildy Clear.
```

or

```text
Split the Buildy Crafts stabilization task into 3 smaller missions.
```

---

# 18. Mission History

Every mission event must be stored.

History events include:

```text
mission_created
mission_started
mission_completed
mission_postponed
mission_rejected
mission_expired
mission_split
```

History matters because Gigi OS must not forget previous decisions.

---

# 19. Data Model

## 19.1 missions

```text
id
project_id
title
description
status
estimated_duration
duration_band
expected_impact
confidence
reason
created_at
started_at
completed_at
updated_at
```

---

## 19.2 mission_steps

```text
id
mission_id
title
status
order
created_at
updated_at
```

Step status values:

```text
todo
done
skipped
```

---

## 19.3 mission_feedback

```text
id
mission_id
feedback_type
reason
comment
created_at
```

---

## 19.4 mission_history_events

```text
id
mission_id
project_id
event_type
description
created_at
```

---

# 20. TypeScript Types Draft

```ts
export type MissionStatus =
  | "available"
  | "started"
  | "completed"
  | "postponed"
  | "rejected"
  | "expired";

export type MissionImpact =
  | "low"
  | "medium"
  | "high"
  | "critical";

export type DurationBand =
  | "micro"
  | "short"
  | "standard"
  | "deep"
  | "too_large";

export type MissionFeedbackType =
  | "accepted"
  | "started"
  | "completed"
  | "postponed"
  | "rejected"
  | "ignored";

export type MissionStepStatus =
  | "todo"
  | "done"
  | "skipped";

export type Mission = {
  id: string;
  projectId: string;
  title: string;
  description: string;
  status: MissionStatus;
  estimatedDuration: number;
  durationBand: DurationBand;
  expectedImpact: MissionImpact;
  confidence: number;
  reason: string;
  createdAt: string;
  startedAt?: string;
  completedAt?: string;
  updatedAt: string;
};

export type MissionStep = {
  id: string;
  missionId: string;
  title: string;
  status: MissionStepStatus;
  order: number;
};

export type MissionFeedback = {
  id: string;
  missionId: string;
  feedbackType: MissionFeedbackType;
  reason?: string;
  comment?: string;
  createdAt: string;
};
```

---

# 21. MVP Requirements

The MVP Mission System must allow the user to:

```text
1. View the current recommended mission.
2. Start the mission.
3. View mission steps.
4. Complete the mission.
5. Postpone the mission.
6. Reject the mission.
7. Save mission history.
```

The MVP does not require:

```text
AI generation
calendar integration
notifications
recurring missions
team missions
mobile push
voice mode
advanced analytics
```

---

# 22. UI Requirements

## 22.1 Mission Screen

Required elements:

```text
Mission title
Project name
Reason
Estimated duration
Expected impact
Confidence
Start button
Postpone button
Reject button
Explain link
```

---

## 22.2 Mission Mode Screen

Required elements:

```text
Mission title
Project name
Timer
Mission steps
Complete button
Exit button
```

---

## 22.3 Completion Screen

Required elements:

```text
Completion confirmation
Progress recorded message
Next mission available message
Return button
```

---

# 23. Acceptance Criteria

The Mission System MVP is successful if:

- the user sees only one primary mission;
- the mission is clear and actionable;
- the mission can be started;
- mission steps can be displayed;
- the mission can be completed;
- completion is saved in history;
- the user can reject or postpone the mission;
- the interface feels focused, not overwhelming.

The MVP fails if:

- the mission feels like a vague todo;
- the user sees too many tasks at once;
- Mission Mode contains distractions;
- completion does not update history;
- rejection feedback is not stored;
- missions are too large to execute.

---

# 24. Cursor Build Instructions

Cursor should implement the Mission System as a clean module.

Suggested structure:

```text
modules/missions/
  missionTypes.ts
  missionFixtures.ts
  missionUtils.ts
  createMissionFromNextAction.ts
  splitMission.ts
  updateMissionStatus.ts
  missionHistory.ts
```

The first version should use mock data.

No database.

No external API.

No AI calls.

The goal is to build the product logic and UI experience first.

---

# 25. First Prototype Missions

Initial mock missions can include:

```text
Rewrite the Buildy Clear sales page headline and CTA.
```

```text
Create 10 TikTok scripts for Buildy Clear.
```

```text
Review the Buildy Crafts roadmap and identify the next missing trade category.
```

```text
Write the product positioning for Linko.
```

```text
Create the first story bible outline for Le Dernier Souvenir.
```

---

# 26. Final Principle

The Mission System must make work feel simple.

The user should never think:

```text
I have too much to do.
```

The user should think:

```text
I know what to do now.
```

A mission is not just a task.

A mission is a commitment to move forward.

> **One mission. One action. One step closer.**
