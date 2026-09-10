# Stu - Student Operating System

Stu is a student-focused software platform designed to turn academic obligations into an actionable, evidence-aware plan.

Rather than acting as another task list, Stu connects course requirements, assignments, deadlines, availability, progress, and study feedback so a student can understand what matters now, what fits into the time available, and why a recommendation was made.

> **Project status:** Private alpha  
> **Repository purpose:** Public portfolio showcase  
> **Canonical application source:** Maintained privately

## Product strategy

Students often manage coursework across an LMS, calendars, notes, reminders, and disconnected study tools. That fragmentation creates a planning problem: knowing that work exists is different from knowing what to do next.

Stu is being developed around five principles:

1. **One authoritative academic record** - SQLite remains the source of truth; visual interfaces are projections of that state.
2. **Actionable prioritization** - deadlines, importance, readiness, and available capacity contribute to a deterministic plan.
3. **Explainable recommendations** - advice should identify its supporting evidence and freshness instead of presenting opaque conclusions.
4. **Student control** - LMS integration is read-only; Stu does not submit or modify coursework.
5. **Local-first privacy** - academic data remains portable and under the student's control.

## Core capabilities

- Versioned `stu-lms-v1` ingestion contract
- Experimental Blackboard-oriented import workflow
- Canonical course, assignment, and completion records
- Deterministic priority ranking
- Capacity-aware study scheduling
- Progress and study-feedback adaptation
- Evidence-qualified recommendations
- Separation of course status from assignment submission state
- Local archival of completed coursework
- Release gates and feature-to-test traceability

## Degree visualization

Stu is developing a degree-scale visual model intended to make academic structure and progress easier to navigate. The current design language uses a "cosmos" metaphor internally, with degree, semester, course, work, resource, and prerequisite relationships projected from the authoritative academic record.

This visualization is not a second database, and its public-facing interaction model is still evolving.

## Architecture

![Stu system architecture](docs/stu-architecture.svg)

The architecture graphic is embedded here as a sanitized view of the private implementation: versioned academic ingestion feeds the authoritative SQLite record, which supports deterministic planning, evidence-qualified recommendations, student actions, feedback, and visualization.

## Engineering evidence

The **release-candidate baseline passed 74 of 74 automated tests**. That number refers specifically to the release-candidate baseline and should not be read as a count of every verification activity performed afterward.

Later strict audits were run as separate verification passes. Manual acceptance was also performed separately from the automated suite. This distinction matters: automated regression evidence, stricter audit/review work, and hands-on acceptance each validate different aspects of the product.

Development uses explicit specifications, reproducible checkpoints, severity policy, and feature-to-test traceability so public product claims remain tied to evidence without exposing private implementation details.

See the sanitized [verification overview](docs/verification.md) for the public evidence model.

## Technology

- Next.js and JavaScript
- SQLite
- Versioned JSON Schema contracts
- Deterministic planning and recommendation logic
- Automated verification

## Documentation

- [Architecture](docs/stu-architecture.svg)
- [Verification overview](docs/verification.md)
- [Documentation index](docs/README.md)

## Portfolio notice

This repository presents selected, sanitized materials from Stu for professional evaluation. The complete application and source code are proprietary and maintained privately.

See [LICENSE.md](LICENSE.md) for permitted use.
