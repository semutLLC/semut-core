# Modules

## semut_core.trace

Stores and retrieves traces.

Responsibilities:

* create trace
* list traces
* search traces
* normalize event types

## semut_core.workspace

Manages user workspaces.

Responsibilities:

* create workspace
* assign traces to workspace
* manage workspace settings

## semut_core.policy

Evaluates user rules.

Responsibilities:

* spending limits
* schedule constraints
* approval rules
* notification rules

## semut_core.email

Handles email-based ingestion.

Responsibilities:

* receive forwarded emails
* parse sender and recipient
* extract useful events
* reject unsupported messages

## semut_core.calendar

Handles calendar actions.

Responsibilities:

* create events
* detect conflicts
* store reminders
* sync with external calendars

## semut_core.ai

Uses AI to convert unstructured text into structured events.

Responsibilities:

* summarize
* extract dates
* classify messages
* propose actions

## semut_core.notification

Sends user-facing alerts.

Responsibilities:

* reminders
* approvals
* warnings
* daily summaries

---

