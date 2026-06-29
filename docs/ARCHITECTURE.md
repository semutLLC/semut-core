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

