# Core Concepts

## Trace

A trace is evidence that something happened.

Examples:

# ARCHITECTURE.md

# Architecture

Semut Core is organized around reusable coordination modules.

## High-Level Architecture

```text
External Sources
  ↓
Ingestion Layer
  ↓
Trace Layer
  ↓
Memory Layer
  ↓
Policy Layer
  ↓
Action Layer
  ↓
User Interface / API
```

## External Sources

Examples:

* Email
* Calendar
* Website forms
* APIs
* PDFs
* Manual input
* Browser automation
* Messages

## Ingestion Layer

Converts incoming information into structured records.

Examples:

* Parse email
* Extract event date
* Detect registration
* Identify payment
* Detect deadline

## Trace Layer

Stores raw or semi-structured events.

A trace is evidence that something happened.

Example:

```json
{
"type": "registration_confirmed",
"source": "email",
"workspace": "tennis",
"timestamp": "2026-06-29T18:00:00",
"data": {
  "league": "USTA Singles",
  "fee": 35
}
}
```

## Memory Layer

Turns repeated traces into useful user context.

Examples:

* User prefers Saturday mornings.
* User avoids matches over 30 minutes away.
* User usually accepts events under $40.

## Policy Layer

Stores user-defined rules.

Examples:

* Ask before spending over $50.
* Do not schedule after 9 PM.
* Prefer doubles over singles.
* Avoid conflicts with work calendar.

## Action Layer

Executes or proposes actions.

Examples:

* Add calendar event.
* Send reminder.
* Draft reply.
* Recommend registration.
* Ask user for approval.

---

# ROADMAP.md

# Roadmap

## Phase 0: Documentation

* Define Semut Core concepts
* Draft shared interfaces
* Document reusable modules
* Clarify relationship to Semut Trace and Semut Tennis

## Phase 1: Minimal Core Library

* Workspace model
* Trace model
* User preference model
* Policy model
* Basic event schema
* SQLite storage

## Phase 2: Semut Trace Integration

* Use Semut Core trace schema
* Store events consistently
* Add workspace field
* Add source field
* Add event type field

## Phase 3: Semut Tennis Integration

* Use Semut Core for tennis events
* Store player preferences
* Store registration traces
* Store match events
* Store payment traces
* Add calendar reminders

## Phase 4: Reusable Modules

* Email ingestion
* Calendar integration
* Notification service
* AI extraction
* Policy engine
* Event normalization

## Phase 5: Multi-Vertical Support

* Semut Ski
* Semut Business
* Semut Volunteer
* Semut Health

## Phase 6: GUI-Text Hybrid Patterns

* Natural language commands
* Structured UI updates
* Human approval flows
* Reusable assistant actions

---

# CONCEPTS.md

# Core Concepts

## Trace

A trace is evidence that something happened.

Examples:

* Email received
* Match scheduled
* Customer request submitted
* Payment completed
* Registration confirmed

## Memory

Memory is organized history derived from traces.

Example:

```text
The user usually plays tennis on Saturday mornings.
```

## Knowledge

Knowledge is a useful pattern inferred from memory.

Example:

```text
The user rarely accepts events more than 30 minutes away.
```

## Policy

A policy is a user-defined rule that guides action.

Example:

```text
Auto-add tennis events to calendar, but ask before paying fees over $40.
```

## Workspace

A workspace is a bounded activity area.

Examples:

* Tennis
* Ski
* Business
* Health
* Volunteer

Each workspace can have its own:

* email
* calendar
* preferences
* documents
* budget
* policies
* memory

## Action

An action is something Semut performs or proposes.

Examples:

* Create reminder
* Draft message
* Add event
* Suggest registration
* Ask for approval

---

