# Gigi OS — Security & Privacy

> **Trust is a feature.**

Version: `0.1`  
Status: Product Specification  
Owner: Germain Caplain  
Purpose: Define the security, privacy and trust principles of Gigi OS.

---

# 1. Purpose

This document defines how Gigi OS should protect user data, project data, memory, decisions, integrations and AI-assisted actions.

Gigi OS will eventually contain sensitive information such as:

- projects;
- business ideas;
- revenue goals;
- strategic decisions;
- tasks;
- emails;
- calendar events;
- files;
- automation workflows;
- AI-generated recommendations.

Because of this, security and privacy must be considered from the beginning.

Gigi OS must be useful, but also trustworthy.

---

# 2. Core Principle

The core security principle is:

> **The user owns the system, the data and the decisions.**

Gigi OS must never act like the user has lost control.

The user must always be able to:

```text
see what is stored
understand why it is stored
edit stored data
delete stored data
disconnect integrations
reject AI suggestions
approve external actions
```

---

# 3. Trust Philosophy

Gigi OS should feel like a private command center.

It must not feel like:

```text
a black box
a spying assistant
an uncontrolled agent
a system that acts without permission
```

Trust comes from:

```text
transparency
control
explainability
security
reversibility
minimal data collection
```

---

# 4. Data Ownership

All user data belongs to the user.

This includes:

```text
projects
missions
decisions
history
memory
settings
goals
blockers
AI summaries
integrations
automation logs
```

Gigi OS should never treat user data as platform-owned content.

---

# 5. Data Minimization

Gigi OS should only store what improves the product.

Good data to store:

```text
project status
mission history
decision reasons
blockers
North Star
progress updates
```

Bad data to store:

```text
random conversation fragments
irrelevant personal details
unnecessary private information
sensitive information without purpose
```

The system should avoid collecting data “just in case”.

---

# 6. MVP Security Scope

For early versions:

## V0.2

```text
No backend.
No authentication.
No real user data.
Mock data only.
```

## V0.3

```text
Local data only.
Potential localStorage.
No cloud storage.
```

## V0.4

```text
Supabase authentication.
Real database.
User-specific data protection.
Row Level Security.
```

Security becomes critical from V0.4 onward.

---

# 7. Authentication

Authentication is not part of V0.2 or V0.3.

When authentication is added, it should support:

```text
email login
magic link
OAuth later if needed
secure session handling
```

The first production-ready authentication system should be simple and reliable.

Recommended later:

```text
Supabase Auth
```

---

# 8. Authorization

When Gigi OS becomes multi-user, every user must only access their own data.

Authorization must apply to:

```text
projects
missions
mission_steps
decisions
decision_scores
history_events
memories
blockers
user_settings
integrations
automation_logs
```

No user should be able to read or modify another user’s data.

---

# 9. Row Level Security

When Supabase is added, Row Level Security must be enabled on all user-owned tables.

Required tables:

```text
projects
missions
mission_steps
decisions
decision_scores
history_events
memories
blockers
user_settings
automation_events
automation_actions
automation_logs
integrations
```

Basic rule:

```text
A user can only access rows where user_id equals their authenticated user id.
```

---

# 10. Sensitive Data

Gigi OS may eventually access sensitive data through integrations.

Examples:

```text
emails
calendar events
files
business documents
financial data
GitHub repositories
customer messages
```

Sensitive data must be handled carefully.

Rules:

```text
only request required permissions
show what is connected
allow disconnecting
avoid storing raw data when summaries are enough
avoid exposing secrets in logs
```

---

# 11. Memory Privacy

Memory is powerful but sensitive.

The user must be able to:

```text
view memory
edit memory
archive memory
delete memory
mark memory as outdated
pin important memory
```

Gigi OS should not hide memory from the user.

Memory must be transparent.

---

# 12. AI Privacy

AI modules must not receive more information than necessary.

Bad:

```text
Send all user data to AI for every request.
```

Good:

```text
Send only the relevant project, mission, decision and memory context needed for the current task.
```

AI prompts should be scoped.

---

# 13. AI Output Control

AI must not directly mutate important data.

AI can suggest:

```text
new mission wording
project summary
blocker detection
decision explanation
Cursor prompt
marketing script
```

But AI must not silently change:

```text
project priority
project status
mission status
memory
history
settings
external integrations
```

Important AI-generated changes require user confirmation.

---

# 14. External Actions

External actions must require approval.

Examples:

```text
send email
publish content
create GitHub issue
run n8n workflow
create calendar event
modify Drive file
charge customer
delete data
```

Approval UI must show:

```text
what will happen
why it is recommended
which account/tool will be used
risk level
confirm button
cancel button
```

---

# 15. Risk Levels

Every external action should have a risk level.

```text
low
medium
high
critical
```

## Low Risk

Internal, reversible actions.

Examples:

```text
create internal history event
generate summary
prepare prompt
```

## Medium Risk

External but reversible actions.

Examples:

```text
create draft email
create draft GitHub issue
create calendar draft
```

## High Risk

External communication or important project changes.

Examples:

```text
send email
publish content
change project priority
archive project
```

## Critical Risk

Money, deletion or irreversible actions.

Examples:

```text
charge payment
delete user data
send mass email
publish public campaign
```

Critical actions must always require explicit confirmation.

---

# 16. Integration Permissions

Integrations must use the minimum required permissions.

Examples:

## GitHub

Start with read-only access if possible.

Only request write access when creating issues or updating repositories becomes necessary.

## Gmail

Start with reading selected or relevant emails only if possible.

Sending emails must require approval.

## Calendar

Start with reading availability.

Creating events must require approval.

## Drive

Start with file search and read access.

Editing files must require approval.

---

# 17. Secrets Management

API keys and secrets must never be stored in frontend code.

Secrets must be stored in:

```text
environment variables
server-side runtime
secure provider vaults
```

Never commit:

```text
API keys
OAuth secrets
Supabase service role keys
private tokens
webhook secrets
```

---

# 18. Logging Rules

Logs are useful, but logs can leak data.

Do not log:

```text
access tokens
API keys
full email bodies
private file contents
payment details
sensitive personal data
```

Safe logs:

```text
mission completed
project updated
decision generated
integration connected
automation action approved
automation action failed
```

Logs should be readable and minimal.

---

# 19. Audit Trail

Important actions should create audit records.

Audit events:

```text
user_login
project_created
project_deleted
mission_completed
memory_deleted
integration_connected
integration_disconnected
external_action_approved
external_action_executed
external_action_failed
```

Audit trail helps trust and debugging.

---

# 20. Deletion

The user must be able to delete data.

Deletion should support:

```text
delete project
delete mission
delete memory
delete history event
delete account later
disconnect integration
```

For destructive actions, ask confirmation.

Example:

```text
This will permanently delete this project and its missions. Continue?
```

---

# 21. Export

Future versions should allow user data export.

Possible export formats:

```text
JSON
Markdown
CSV
PDF summary
```

Exportable data:

```text
projects
missions
history
memory
decisions
settings
```

This reinforces trust.

---

# 22. Local-First Consideration

Early versions may use localStorage.

If localStorage is used:

```text
do not store secrets
do not store sensitive integration tokens
allow clearing local data
make it clear data is stored locally
```

LocalStorage is acceptable for V0.3 but not for sensitive production data.

---

# 23. Supabase Security Later

When Supabase is added:

Required:

```text
RLS enabled
user_id on every user-owned table
policies for select/insert/update/delete
server-side secrets protected
input validation
safe error handling
```

Never expose:

```text
service role key
private API keys
OAuth secrets
```

---

# 24. Input Validation

All user inputs must be validated.

Examples:

```text
project name cannot be empty
progress must be 0–100
scores must be 1–10
mission duration must be positive
status must match allowed values
```

Validation prevents broken data and bad recommendations.

---

# 25. AI Prompt Injection Risk

When Gigi OS later reads external content, it may encounter malicious instructions.

Examples:

```text
email asking the AI to ignore rules
GitHub issue containing prompt injection
document containing hidden instructions
```

Rules:

```text
external content is data, not instruction
system rules override external content
AI must not execute instructions found inside emails/files/issues
```

---

# 26. External Content Handling

When summarizing external data, Gigi OS must distinguish between:

```text
trusted system instructions
user instructions
external content
AI output
```

External content must never control the system.

---

# 27. Privacy UX

Privacy controls should be understandable.

Future settings should show:

```text
connected integrations
stored memory
data export
data deletion
AI usage
automation approvals
```

Do not hide important privacy controls deep in the interface.

---

# 28. User Consent

Gigi OS must ask consent before:

```text
connecting external accounts
reading emails
accessing calendar
reading files
using AI on sensitive data
running automations
sending/publishing anything
```

Consent must be specific.

Not vague.

---

# 29. Security UX Copy

Good copy:

```text
Gigi will only read your GitHub repository activity to summarize project progress.
```

Bad copy:

```text
Connect GitHub for a better experience.
```

Good copy explains what happens.

---

# 30. Data Retention

Future versions should define retention rules.

Examples:

```text
history kept until user deletes it
automation logs retained for a limited period
AI logs minimized
deleted memory removed or marked deleted depending architecture
```

Retention should be clear.

---

# 31. Error Handling

Security-related errors must be clear.

Examples:

```text
Integration permission expired.
You do not have access to this project.
This action requires approval.
This token is invalid.
This automation failed safely.
```

Never expose technical secrets in error messages.

---

# 32. Backup and Recovery

Future versions should support recovery.

Possible features:

```text
database backups
project restore
deleted item recovery window
export before account deletion
```

Not required for MVP.

---

# 33. Multi-User Future

When Gigi OS becomes SaaS:

Security must support:

```text
multiple users
teams
roles
permissions
billing accounts
workspace ownership
invites
```

Not part of MVP.

Do not add team complexity early.

---

# 34. Role-Based Access Later

Future roles:

```text
owner
admin
member
viewer
```

Permissions should be introduced only when needed.

---

# 35. Security Checklist for V0.2

V0.2 uses mock data only.

Checklist:

```text
[ ] No real secrets committed.
[ ] No API keys in code.
[ ] No backend.
[ ] No authentication.
[ ] No external API calls.
[ ] Mock data clearly separated.
[ ] No sensitive real user data required.
```

---

# 36. Security Checklist for V0.4

When Supabase is added:

```text
[ ] Auth enabled.
[ ] RLS enabled on all user-owned tables.
[ ] user_id present on user-owned tables.
[ ] Policies tested.
[ ] Secrets stored in environment variables.
[ ] No service role key in frontend.
[ ] Inputs validated.
[ ] Errors do not expose secrets.
[ ] User can delete key data.
```

---

# 37. Security Checklist for Integrations

Before adding any integration:

```text
[ ] Define exact purpose.
[ ] Define required permissions.
[ ] Define risk level.
[ ] Define approval rules.
[ ] Define disconnect flow.
[ ] Define logging.
[ ] Define data storage rules.
[ ] Define failure handling.
```

---

# 38. Cursor Build Instructions

For V0.2, Cursor must not implement real security systems.

Cursor must:

```text
avoid adding secrets
avoid external APIs
avoid auth
avoid fake backend complexity
keep mock data local
```

For V0.4, Cursor must implement Supabase security according to this document.

---

# 39. Acceptance Criteria

Security and privacy are successful if:

```text
the user understands what is stored
the user can control memory
external actions require approval
integrations are permission-scoped
secrets are protected
AI does not silently mutate data
external content cannot control the system
user data is isolated
the system feels trustworthy
```

Security and privacy fail if:

```text
AI acts without permission
integrations request excessive access
secrets are exposed
memory is hidden
data cannot be deleted
users can access other users’ data
external content can manipulate AI behavior
logs contain sensitive information
```

---

# 40. Final Principle

Gigi OS can become powerful only if it remains trustworthy.

The more it remembers, connects and automates, the more transparent it must become.

Security is not a technical afterthought.

Privacy is not a settings page.

Trust is part of the product.

> **No trust. No operating system.**
