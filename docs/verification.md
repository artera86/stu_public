# Verification Overview

This document summarizes Stu's public verification evidence without exposing private source code, fixtures, academic data, or internal test implementation details.

## Release-candidate automated baseline

The release-candidate baseline completed **74 of 74 automated tests successfully**.

That count belongs to the release-candidate baseline only. It is not intended as a cumulative total for every later validation activity.

The automated baseline covers representative areas such as:

- academic record ingestion and validation
- canonical course and assignment state
- deterministic prioritization behavior
- capacity-aware planning behavior
- progress and study-feedback handling
- evidence and freshness qualification
- archival and status separation behavior
- release gates and feature-to-test traceability

Detailed test names, fixtures, implementation paths, private academic data, and proprietary assertions are intentionally omitted from this public repository.

## Later strict audits

After the 74/74 release-candidate baseline, stricter audits were performed as separate verification passes. These audits are not folded into the 74-test count.

Their purpose was to challenge assumptions, inspect release evidence more critically, and identify gaps that a normal regression pass might not surface. Public claims therefore distinguish the automated release baseline from later audit activity.

## Manual acceptance

Manual acceptance was performed separately from automated verification.

Manual acceptance is used to confirm user-visible behavior and end-to-end workflows that are better evaluated through direct interaction than by counting automated assertions. A successful manual acceptance pass does not increase the 74-test automated baseline, and the automated baseline does not substitute for manual acceptance.

## Evidence model

Stu treats verification as layered evidence rather than a single test count:

1. **Automated regression baseline** — reproducible checks against expected behavior.
2. **Strict audit/review passes** — separate scrutiny of assumptions, evidence, and release quality.
3. **Manual acceptance** — hands-on confirmation of user-visible workflows and release readiness.

This repository publishes only sanitized evidence suitable for portfolio review. The canonical implementation, raw test artifacts, detailed audit material, and private release records remain in the private project.
