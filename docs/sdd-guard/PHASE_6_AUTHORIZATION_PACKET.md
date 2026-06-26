# Phase 6 Authorization Packet

## Classification

This document is a governance authorization packet.

It does not authorize Phase 6 by itself.
It does not begin Phase 6.
It does not authorize product implementation, product build, executable implementation planning, runtime, agents, workflows, integrations, schemas, modules, scripts, tests, deployment, source code, application code, infrastructure, CI, GitHub Actions, Supabase configuration, or external service integration.

This packet exists only to make the Phase 6 authorization decision explicit, reviewable, and auditable.

## Current Confirmed State

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch completed, aligned, and verified
- Latest verified governance baseline before this packet: `22c026a4b5c2a3a193196e7670464a0ec3d8d317`
- Completed phases: `[0, 1, 2, 3, 4, 5]`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized

## Purpose

The purpose of this packet is to request an explicit decision on whether Phase 6 may be authorized.

No implicit authorization is allowed.
No inferred authorization is allowed.
No tool, commit, scan, report, or acceleration mechanism may substitute for the authorization decision.

## Required Decision

One and only one decision may be selected:

```text
PHASE_6_AUTHORIZATION_DECISION: APPROVED
PHASE_6_AUTHORIZATION_DECISION: DENIED
PHASE_6_AUTHORIZATION_DECISION: DEFERRED
```

If the decision is `APPROVED`, the authorization must also define the allowed Phase 6 scope before any Phase 6 work begins.

If the decision is `DENIED`, Phase 6 remains closed.

If the decision is `DEFERRED`, Phase 6 remains closed until a future authorization packet is approved.

## Approval Requirements

Phase 6 may only begin if all of the following are true:

1. The authorization decision is explicitly `APPROVED`.
2. The authorized Phase 6 scope is written in this packet or in a committed SDD+ contract that references this packet.
3. The forbidden surface remains closed unless explicitly opened by the approved scope.
4. SDD Guard returns `PASS` after the authorization packet is committed.
5. The next allowed action changes from `request_phase_6_authorization` to the exact approved Phase 6 governance action.

## Scope Declaration Required For Approval

If approved, fill this section before Phase 6 starts:

```text
AUTHORIZED_PHASE_6_NAME:
AUTHORIZED_PHASE_6_OBJECTIVE:
AUTHORIZED_PHASE_6_ALLOWED_FILES:
AUTHORIZED_PHASE_6_FORBIDDEN_FILES:
AUTHORIZED_PHASE_6_ALLOWED_ACTIONS:
AUTHORIZED_PHASE_6_FORBIDDEN_ACTIONS:
AUTHORIZED_PHASE_6_EXIT_CRITERIA:
AUTHORIZED_PHASE_6_ROLLBACK_RULE:
```

Blank scope means Phase 6 is not authorized.

## Default Forbidden Surface

Unless explicitly authorized in the approved Phase 6 scope, the following remain forbidden:

```text
src/**
app/**
lib/**
modules/**
agents/**
workflows/**
integrations/**
runtime/**
deploy/**
supabase/**
schemas/**
scripts/**
tests/**
.github/**
```

## Default Forbidden Actions

Unless explicitly authorized in the approved Phase 6 scope, the following remain forbidden:

- Product implementation
- Product build
- Executable implementation planning
- Runtime creation
- Agent creation
- Workflow creation
- Integration creation
- Schema creation
- Module creation
- Tool creation
- Product prompt creation
- Script creation
- Test creation or execution
- Deployment
- Source code modification
- Application code modification
- Infrastructure creation
- CI or GitHub Actions configuration
- Supabase configuration
- External service integration

## SDD Guard Requirement

Before any Phase 6 work may begin, SDD Guard must inspect this packet together with:

```text
README.md
docs/sdd-guard/SDD_GUARD_CONTRACT.md
docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
docs/sdd-guard/SDD_GUARD_CHECKS.md
docs/sdd-guard/CODEX_TASKS.md
docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
```

The required verdict is:

```text
GUARD_VERDICT: PASS
```

Any `FAIL`, `REVIEW_REQUIRED`, or `STOP` means Phase 6 remains closed.

## Decision Log

Current decision:

```text
PHASE_6_AUTHORIZATION_DECISION: DEFERRED
```

Reason:

```text
Authorization packet created for review. Phase 6 remains closed until explicit approval and scope declaration are committed.
```

## Current Next Allowed Action

```text
NEXT_ALLOWED_ACTION: run_governance_scan
```

This scan must verify that this packet is a request only and does not itself authorize Phase 6.

## Non-Negotiable Rule

A request is not approval.

Phase 6 remains closed until approval is explicit, scoped, committed, and verified.
