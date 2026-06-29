# Semut Core

Semut Core is the reusable coordination foundation for Semut applications.

It provides shared concepts, interfaces, and modules for building AI assistants that coordinate fragmented real-world activities across many systems.

Examples of Semut verticals:

* Semut Trace
* Semut Tennis
* Semut Ski
* Semut Business
* Semut Health
* Semut Volunteer

Semut Core is not a consumer app by itself. It is the foundation used by Semut products.

## Purpose

Most real-world activities are fragmented across:

* websites
* emails
* calendars
* forms
* payment receipts
* messages
* schedules
* local organizations

Semut Core helps convert those fragments into structured coordination.

## Core Idea

Semut applications follow this pattern:

```text
Trace
↓
Memory
↓
Knowledge
↓
Policy
↓
Action
```

Semut Core provides reusable building blocks for this process.

## Planned Modules

* Trace model
* Workspace model
* User preferences
* Policy engine
* Email ingestion
* Calendar integration
* Notification service
* AI extraction
* Event normalization
* Integration adapters
* Privacy controls

## Example

A tennis email arrives:

```text
League registration confirmed.
Match starts July 15 at 6 PM.
```

Semut Core can help:

```text
Extract event
Create trace
Update calendar
Check conflicts
Update budget
Notify user
Store memory
```

## Status

Early research and architecture draft.

---
