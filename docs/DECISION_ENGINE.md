# Gigi OS — Decision Engine

> **Know what matters next.**

Version: `0.1`  
Status: Product Specification  
Module: Decision Engine  
Owner: Germain Caplain  
Purpose: Select the single most important mission for the user right now.

---

# 1. Purpose

The Decision Engine is the heart of Gigi OS.

Its role is not to manage tasks.

Its role is not to display projects.

Its role is not to behave like a chatbot.

Its role is to answer one question:

> **What is the most important thing the user should do next?**

Every other module exists to support this decision.

The Decision Engine must help the user move from confusion to execution.

---

# 2. Core Philosophy

Gigi OS is built for builders, creators and entrepreneurs who often have too many ideas, too many projects and not enough clarity.

The Decision Engine must protect the user from:

- distraction;
- overthinking;
- switching projects too often;
- starting new ideas before finishing important ones;
- emotional decision-making;
- wasting time on low-impact tasks;
- forgetting what matters most.

The engine must always produce one clear recommendation.

Not five.

Not ten.

One.

---

# 3. Main Output

The Decision Engine outputs a **Mission Recommendation**.

A mission recommendation includes:

```text
selected_project
selected_mission
priority_score
reason
estimated_duration
expected_impact
alternatives_considered
why_other_projects_were_not_selected
confidence_level
```

Example:

```text
Selected Mission:
Finish the Buildy Clear sales page.

Reason:
Buildy Clear is the closest project to generating revenue. The next action is clear, the effort is limited, and completing it moves the user directly toward the current financial objective.

Estimated duration:
45 minutes

Expected impact:
High

Confidence:
87%
```

---

# 4. What the Decision Engine Is

The Decision Engine is:

- a prioritization system;
- a mission selector;
- a scoring engine;
- an explanation generator;
- a focus protector;
- a strategic filter.

It compares all active projects and selects the action with the highest current value.

---

# 5. What the Decision Engine Is Not

The Decision Engine is not:

- a generic AI chat;
- a personal coach;
- a task list sorter;
- a calendar planner;
- a motivational assistant;
- a random suggestion generator;
- a complex productivity dashboard.

If the engine cannot explain its recommendation, the recommendation is invalid.

---

# 6. Primary Rule

The Decision Engine must always obey this rule:

> **One user. One objective. One mission.**

The user may have many projects.

The system may store many tasks.

But the interface must always push toward one mission.

---

# 7. Inputs

The Decision Engine uses structured inputs.

## 7.1 User Inputs

```text
north_star
monthly_revenue_target
available_time
energy_level
preferred_work_duration
current_focus
```

Example:

```text
North Star:
Create profitable digital products and software.

Monthly revenue target:
500 €

Available time today:
2 hours

Energy level:
medium
```

---

## 7.2 Project Inputs

Each project must provide:

```text
project_id
name
status
progress
priority
business_potential
strategic_value
urgency
risk_level
estimated_effort
next_action
current_blocker
last_worked_on
```

Example:

```text
Project:
Buildy Clear

Status:
active

Progress:
94%

Business potential:
high

Strategic value:
medium

Urgency:
high

Next action:
Finish sales page

Current blocker:
Tunnel not fully optimized
```

---

## 7.3 Mission Inputs

Each potential mission must provide:

```text
mission_id
project_id
title
description
estimated_duration
impact_level
clarity_level
effort_level
dependency_status
```

Example:

```text
Mission:
Rewrite Buildy Clear sales page headline and CTA.

Estimated duration:
45 minutes

Impact:
high

Clarity:
high

Effort:
low
```

---

# 8. Scoring Criteria

Each project or mission is scored using 7 criteria.

Each criterion is scored from `1` to `10`.

## 8.1 Business Impact

Measures how much the mission can contribute to revenue or monetization.

```text
1 = no business impact
5 = indirect business impact
10 = direct revenue impact
```

Example:

Finishing a sales page for Buildy Clear may score `9`.

Designing a future creative concept may score `3`.

---

## 8.2 Alignment

Measures how strongly the mission supports the user’s North Star.

```text
1 = unrelated
5 = somewhat aligned
10 = directly aligned
```

Example:

If the North Star is earning 500 €/month quickly, Buildy Clear is highly aligned.

---

## 8.3 Completion Proximity

Measures how close the project is to a meaningful milestone.

```text
1 = very early idea
5 = halfway
10 = almost ready
```

Example:

A project at 94% completion scores high because a small action can unlock a milestone.

---

## 8.4 Urgency

Measures whether the mission should be handled soon.

```text
1 = can wait
5 = useful soon
10 = urgent now
```

Urgency can come from:

- launch timing;
- financial pressure;
- deadlines;
- blocking other work;
- active opportunity.

---

## 8.5 Clarity

Measures whether the next action is obvious and executable.

```text
1 = vague
5 = somewhat clear
10 = extremely clear
```

Bad mission:

```text
Work on marketing.
```

Good mission:

```text
Write 10 TikTok scripts for Buildy Clear.
```

---

## 8.6 Effort Efficiency

Measures the ratio between impact and effort.

This score is higher when a task has strong impact and low effort.

```text
1 = high effort, low impact
5 = balanced
10 = low effort, high impact
```

---

## 8.7 Risk of Delay

Measures what happens if the mission is ignored.

```text
1 = no consequence
5 = some delay
10 = serious risk
```

Risk can include:

- missed opportunity;
- project becoming stale;
- revenue delay;
- technical debt;
- user motivation loss;
- blocker accumulation.

---

# 9. Default Weights

The initial scoring weights are:

```text
Business Impact: 25%
Alignment: 20%
Completion Proximity: 15%
Urgency: 15%
Clarity: 10%
Effort Efficiency: 10%
Risk of Delay: 5%
```

Total:

```text
100%
```

These weights are intentionally business-focused because the current early objective is to create income.

---

# 10. Weighted Score Formula

The weighted score is calculated as:

```text
score =
business_impact * 0.25 +
alignment * 0.20 +
completion_proximity * 0.15 +
urgency * 0.15 +
clarity * 0.10 +
effort_efficiency * 0.10 +
risk_of_delay * 0.05
```

The final score is converted to a percentage:

```text
priority_score = score * 10
```

Example:

```text
Business Impact: 9
Alignment: 9
Completion Proximity: 10
Urgency: 8
Clarity: 9
Effort Efficiency: 8
Risk of Delay: 6
```

Calculation:

```text
9 * 0.25 = 2.25
9 * 0.20 = 1.80
10 * 0.15 = 1.50
8 * 0.15 = 1.20
9 * 0.10 = 0.90
8 * 0.10 = 0.80
6 * 0.05 = 0.30

Total = 8.75
Priority score = 87.5%
```

---

# 11. Priority Bands

The Decision Engine classifies missions by score.

```text
90–100 = Critical mission
75–89 = High-priority mission
60–74 = Useful mission
40–59 = Low-priority mission
0–39 = Not recommended now
```

Only one mission should be selected.

If several missions are close, the engine must explain the tradeoff.

---

# 12. Mission Selection Rules

## Rule 1 — Active Projects First

Active projects are considered before paused, future or archived projects.

Archived and completed projects must not generate missions.

---

## Rule 2 — Revenue Pressure Matters

If the user has a short-term revenue goal, revenue-generating projects receive a scoring boost.

Example:

If the user needs 300–500 €/month, Buildy Clear should outrank a long-term creative idea unless there is a strong reason otherwise.

---

## Rule 3 — Completion Beats Starting

When two projects have similar potential, the project closest to completion should win.

Example:

A 94% finished product should usually outrank a 5% idea.

---

## Rule 4 — Clarity Beats Excitement

A clear actionable task should usually outrank an exciting but vague idea.

---

## Rule 5 — Gigi Can Say Not Now

If the user wants to start a new project while an important near-complete project is blocked, Gigi OS should be allowed to respond:

```text
Not now.
```

But it must explain why.

---

## Rule 6 — The User Can Override

The user is always the final decision-maker.

The Decision Engine recommends.

The user decides.

If the user rejects a mission, the rejection must be saved in history.

---

# 13. Decision Flow

The Decision Engine follows this process:

```text
1. Read the North Star.
2. Read all active projects.
3. Exclude archived and completed projects.
4. Generate or read each project's next mission.
5. Score each mission.
6. Rank missions by weighted score.
7. Select the highest-scoring mission.
8. Generate a plain-language explanation.
9. Store the decision.
10. Display the mission to the user.
```

---

# 14. Pseudocode

```text
function selectMission(user, projects):
    activeProjects = filter(projects, status in ["active", "paused"])

    candidateMissions = []

    for project in activeProjects:
        if project.next_action is empty:
            mission = generateMissionFromProject(project)
        else:
            mission = createMissionFromNextAction(project)

        score = calculateMissionScore(user, project, mission)

        candidateMissions.append({
            project,
            mission,
            score
        })

    sortedMissions = sortByScoreDescending(candidateMissions)

    selected = sortedMissions[0]
    alternatives = sortedMissions[1:4]

    explanation = generateDecisionExplanation(selected, alternatives, user)

    return {
        selected_project: selected.project,
        selected_mission: selected.mission,
        score: selected.score,
        reason: explanation,
        alternatives_considered: alternatives
    }
```

---

# 15. Explanation Requirements

Every recommendation must be human-readable.

The explanation must answer:

```text
Why this mission?
Why now?
Why not the other projects?
What happens after completion?
```

Example:

```text
Buildy Clear is selected today because it is the closest project to generating short-term revenue. The next action is clear, the effort is limited, and completing the sales page unlocks the next step: publishing traffic videos.

Buildy Crafts remains strategically important, but it requires longer development time before generating revenue.

Linko is promising, but it is still too early for monetization.

1Millimètre is interesting, but experimental and not aligned with the current 500 €/month target.
```

---

# 16. Rejection Handling

The user can reject a mission.

When a mission is rejected, the system must ask for a reason.

Possible rejection reasons:

```text
not_today
too_long
not_motivated
blocked
wrong_priority
already_done
other
```

The rejection must be stored.

The Decision Engine must use this information later.

Example:

If the user rejects long missions multiple times, Gigi OS should recommend shorter missions.

---

# 17. Postponement Handling

The user can postpone a mission.

Postponement is different from rejection.

A postponed mission remains valid but is not selected immediately.

Postponement fields:

```text
mission_id
postponed_until
reason
created_at
```

If a mission is postponed too many times, Gigi OS should flag it as a potential blocker.

---

# 18. Mission Completion

When the user completes a mission, the system must:

```text
1. Mark the mission as completed.
2. Add an event to history.
3. Update project progress if needed.
4. Generate the next possible mission.
5. Recalculate priorities.
```

Completion should feel satisfying but not childish.

The interface may show:

```text
Mission completed.

Progress recorded.

New mission available.
```

---

# 19. Edge Cases

## 19.1 No Project Exists

If there are no projects, the system must ask the user to create the first project.

```text
Before I can choose your next mission, I need at least one project.
```

---

## 19.2 No Next Action Exists

If a project has no next action, the system must generate one or ask the user to define one.

```text
This project has no next action. Gigi OS cannot prioritize vague work.
```

---

## 19.3 Two Missions Have Similar Scores

If two missions are within 5 points, the system must explain the tradeoff.

Example:

```text
Buildy Clear and Buildy Crafts are close. Buildy Clear wins because it has faster revenue potential.
```

---

## 19.4 User Keeps Ignoring Same Mission

If the user repeatedly postpones or rejects the same mission, the system must identify it as a blocker.

Example:

```text
You have postponed this mission 4 times. It may be too large, unclear or emotionally blocked. I recommend splitting it.
```

---

## 19.5 New Idea Appears

When the user adds a new idea, the Decision Engine must not automatically prioritize it.

New ideas start as:

```text
future
```

Unless the user explicitly marks them as active.

---

# 20. Decision Memory

Every decision must be stored.

A decision record includes:

```text
decision_id
selected_mission_id
selected_project_id
score
reason
alternatives_json
created_at
user_response
```

Possible user responses:

```text
accepted
started
completed
postponed
rejected
ignored
```

This allows Gigi OS to improve over time.

---

# 21. Data Model

## 21.1 decisions

```text
id
selected_project_id
selected_mission_id
score
reason
alternatives_json
created_at
user_response
```

---

## 21.2 decision_scores

```text
id
decision_id
project_id
mission_id
business_impact
alignment
completion_proximity
urgency
clarity
effort_efficiency
risk_of_delay
final_score
created_at
```

---

## 21.3 mission_feedback

```text
id
mission_id
feedback_type
reason
created_at
```

---

# 22. Example Decision

## Input Projects

```text
Buildy Clear
Progress: 94%
Next action: Finish sales page
Business potential: high
Urgency: high

Buildy Crafts
Progress: 70%
Next action: Continue stabilization
Business potential: high
Urgency: medium

Linko
Progress: 20%
Next action: Validate positioning
Business potential: high
Urgency: low

1Millimètre
Progress: 25%
Next action: Improve gameplay
Business potential: medium
Urgency: low

Le Dernier Souvenir
Progress: 5%
Next action: Write story bible
Business potential: unknown
Urgency: low
```

## Output

```text
Selected Mission:
Finish Buildy Clear sales page.

Score:
87%

Reason:
Buildy Clear is closest to generating short-term revenue and supports the current financial target. The task is clear, short, and directly unlocks the next step: publishing traffic content.

Rejected alternatives:
Buildy Crafts is strategically important but longer-term.
Linko is promising but too early.
1Millimètre is experimental.
Le Dernier Souvenir is creative but not aligned with short-term revenue.
```

---

# 23. MVP Implementation

For the MVP, the Decision Engine should be deterministic.

No external AI API is required.

The first version can use:

```text
static project data
manual project fields
weighted scoring function
basic mission generation from next_action
plain explanation templates
```

AI can be added later.

The system must work even without AI.

---

# 24. Future AI Layer

Later, AI can improve:

- mission wording;
- explanation quality;
- next action generation;
- blocker detection;
- weekly review;
- strategic recommendations.

But AI must never replace the core decision structure.

The Decision Engine must remain explainable.

---

# 25. Acceptance Criteria

The Decision Engine MVP is accepted if:

- it can compare at least 3 projects;
- it selects one mission;
- it produces a score;
- it explains the decision clearly;
- it records the decision;
- the user can accept, reject or postpone the mission;
- rejected and postponed missions are remembered;
- the selected mission feels more useful than a random task.

The MVP fails if:

- the user still has to manually choose between projects;
- the system recommends vague tasks;
- the explanation is generic;
- the selected mission does not match the current objective;
- too many missions are shown at once.

---

# 26. Cursor Build Instructions

Cursor must implement the Decision Engine in a clean and modular way.

Suggested structure:

```text
modules/decision-engine/
  calculateMissionScore.ts
  selectMission.ts
  explainDecision.ts
  decisionTypes.ts
  decisionWeights.ts
  decisionFixtures.ts
```

No external API.

No AI calls.

No database required for the first static prototype.

The first implementation should work with mock data.

---

# 27. TypeScript Types Draft

```ts
export type ProjectStatus =
  | "active"
  | "paused"
  | "future"
  | "archived"
  | "completed";

export type MissionStatus =
  | "available"
  | "started"
  | "completed"
  | "postponed"
  | "rejected";

export type Project = {
  id: string;
  name: string;
  description: string;
  status: ProjectStatus;
  progress: number;
  businessPotential: number;
  strategicValue: number;
  urgency: number;
  riskLevel: number;
  clarity: number;
  estimatedEffort: number;
  nextAction: string;
  currentBlocker?: string;
  lastWorkedOn?: string;
};

export type Mission = {
  id: string;
  projectId: string;
  title: string;
  description: string;
  estimatedDuration: number;
  expectedImpact: number;
  clarity: number;
  effortEfficiency: number;
  status: MissionStatus;
};

export type DecisionScore = {
  businessImpact: number;
  alignment: number;
  completionProximity: number;
  urgency: number;
  clarity: number;
  effortEfficiency: number;
  riskOfDelay: number;
  finalScore: number;
};

export type MissionRecommendation = {
  selectedProject: Project;
  selectedMission: Mission;
  score: DecisionScore;
  reason: string;
  alternatives: Array<{
    project: Project;
    mission: Mission;
    score: DecisionScore;
    reasonNotSelected: string;
  }>;
  confidenceLevel: number;
};
```

---

# 28. Final Principle

The Decision Engine is not here to make the user busy.

It is here to make the user effective.

The best recommendation is not always the most exciting.

It is the one that moves the user closer to the North Star.

> **One objective. One mission. One step forward.**
