# Phase 6 Authorization Packet

## Classification

This document is a governance authorization packet.

This packet authorizes only Phase 6A: Governance Scope Lock.

It does not authorize product implementation, product build, executable implementation planning, runtime, agents, workflows, integrations, schemas, modules, scripts, tests, deployment, source code, application code, infrastructure, CI, GitHub Actions, Supabase configuration, or external service integration.

This packet exists only to make the Phase 6A governance authorization decision explicit, reviewable, and auditable.

## Current Confirmed State

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch completed, aligned, and verified
- Latest verified governance baseline before original packet: `22c026a4b5c2a3a193196e7670464a0ec3d8d317`
- Latest verified governance baseline before approval: `106b830066281035d46f34e483f7b9d9fa688fd6`
- Completed phases: `[0, 1, 2, 3, 4, 5]`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized

## Purpose

The purpose of this packet is to approve a limited Phase 6A governance action.

No implicit authorization is allowed.
No inferred authorization is allowed.
No tool, commit, scan, report, or acceleration mechanism may substitute for the authorization decision.

## Required Decision

```text
PHASE_6_AUTHORIZATION_DECISION: APPROVED
```

Approval is limited to the written scope below.

## Authorized Phase 6 Scope

```text
AUTHORIZED_PHASE_6_NAME: Phase 6A - Governance Scope Lock
AUTHORIZED_PHASE_6_OBJECTIVE: Create the committed governance contract that defines what Phase 6 may and may not do before any product-facing work can be considered.
AUTHORIZED_PHASE_6_ALLOWED_FILES:
- docs/sdd-guard/PHASE_6_SCOPE_CONTRACT.md
- docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
AUTHORIZED_PHASE_6_FORBIDDEN_FILES:
- src/**
- app/**
- lib/**
- modules/**
- agents/**
- workflows/**
- integrations/**
- runtime/**
- deploy/**
- supabase/**
- schemas/**
- scripts/**
- tests/**
- .github/**
AUTHORIZED_PHASE_6_ALLOWED_ACTIONS:
- Create docs/sdd-guard/PHASE_6_SCOPE_CONTRACT.md
- Patch this packet only if needed to correct governance wording
- Run SDD Guard governance scans over allowed governance files
AUTHORIZED_PHASE_6_FORBIDDEN_ACTIONS:
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
AUTHORIZED_PHASE_6_EXIT_CRITERIA:
- PHASE_6_SCOPE_CONTRACT.md exists
- SDD Guard returns PASS
- Phase 6 product work remains unauthorized unless a later explicit scoped packet approves it
AUTHORIZED_PHASE_6_ROLLBACK_RULE:
- Revert Phase 6A commits if any forbidden surface is touched or if any product authorization is implied without explicit scoped approval
```

## Approval Requirements

Phase 6A may only proceed if all of the following are true:

1. The authorization decision is explicitly `APPROVED`.
2. The approved scope is limited to Phase 6A Governance Scope Lock.
3. The forbidden surface remains closed.
4. SDD Guard returns `PASS` after this approval is committed.
5. The next allowed action changes to `create_phase_6_scope_contract`.

## Default Forbidden Surface

Unless explicitly authorized in a later approved scope, the following remain forbidden:

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

Unless explicitly authorized in a later approved scope, the following remain forbidden:

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

Before Phase 6A work proceeds beyond this packet, SDD Guard must inspect this packet together with:

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

Any `FAIL`, `REVIEW_REQUIRED`, or `STOP` means Phase 6A remains blocked.

## Decision Log

Current decision:

```text
PHASE_6_AUTHORIZATION_DECISION: APPROVED
```

Reason:

```text
Approved only for Phase 6A Governance Scope Lock. Product-facing work remains unauthorized.
```

## Current Next Allowed Action

```text
NEXT_ALLOWED_ACTION: run_governance_scan
```

This scan must verify that this packet authorizes only Phase 6A Governance Scope Lock and does not authorize product-facing Phase 6 work.

## Non-Negotiable Rule

Approval is scoped.

Anything outside the written approved scope remains unauthorized.
