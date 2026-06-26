# Phase 6A Scope Contract

## Classification

This document is the committed scope contract for Phase 6A: Governance Scope Lock.

It is governance-only.
It does not authorize product implementation.
It does not authorize product build.
It does not authorize executable implementation planning.
It does not authorize runtime, agents, workflows, integrations, schemas, modules, scripts, tests, deployment, source code, application code, infrastructure, CI, GitHub Actions, Supabase configuration, or external service integration.

## Authorization Source

Phase 6A is authorized by:

```text
docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
commit: 46524449beb3c09f8e5706a48523090fa2f9420e
```

The approval is scoped and limited to Phase 6A Governance Scope Lock.

Anything outside this contract remains unauthorized.

## Current State

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch completed, aligned, and verified
- Phase 6 authorization decision: approved only for Phase 6A Governance Scope Lock
- Completed phases remain: `[0, 1, 2, 3, 4, 5]`
- Product-facing Phase 6 work: not authorized
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent

## Objective

Create a firm governance boundary for Phase 6 before any product-facing work can be considered.

The objective is to define:

- What Phase 6A may do
- What Phase 6A may not do
- Which files Phase 6A may touch
- Which files Phase 6A may not touch
- Which actions remain forbidden
- What must happen before any later product-facing Phase 6 scope can be requested

## Allowed Files

Phase 6A may touch only:

```text
docs/sdd-guard/PHASE_6_SCOPE_CONTRACT.md
docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
```

SDD Guard may inspect the established governance files:

```text
README.md
docs/sdd-guard/SDD_GUARD_CONTRACT.md
docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
docs/sdd-guard/SDD_GUARD_CHECKS.md
docs/sdd-guard/CODEX_TASKS.md
docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
docs/sdd-guard/PHASE_6_SCOPE_CONTRACT.md
```

## Forbidden Files

Phase 6A must not touch:

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

## Allowed Actions

Phase 6A may only:

- Create this scope contract
- Patch this scope contract if a governance wording correction is needed
- Patch the Phase 6 authorization packet if a governance wording correction is needed
- Run SDD Guard governance scans over allowed governance files
- Recommend the next governance-only action

## Forbidden Actions

Phase 6A must not:

- Implement product
- Build product
- Create executable implementation planning
- Create runtime
- Create agents
- Create workflows
- Create integrations
- Create schemas
- Create modules
- Create tools
- Create product prompts
- Create scripts
- Create or run tests
- Deploy
- Modify source code
- Modify application code
- Create infrastructure
- Configure CI or GitHub Actions
- Configure Supabase
- Integrate external services
- Begin product-facing Phase 6 work

## Required Guard Scan

After this contract is committed, SDD Guard must inspect:

```text
README.md
docs/sdd-guard/SDD_GUARD_CONTRACT.md
docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
docs/sdd-guard/SDD_GUARD_CHECKS.md
docs/sdd-guard/CODEX_TASKS.md
docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md
docs/sdd-guard/PHASE_6_SCOPE_CONTRACT.md
```

Required verdict:

```text
GUARD_VERDICT: PASS
```

Any `FAIL`, `REVIEW_REQUIRED`, or `STOP` means Phase 6A is blocked pending governance correction.

## Exit Criteria

Phase 6A is complete only when:

1. `PHASE_6_SCOPE_CONTRACT.md` exists.
2. The contract preserves the approved Phase 6A scope.
3. The contract does not authorize product-facing work.
4. SDD Guard returns `PASS`.
5. The next allowed action is either `stop` or a later explicit authorization request.

## Next Scope Rule

No later Phase 6 work may begin until a new explicit authorization packet is created, scoped, committed, and verified.

A later authorization packet must define:

```text
AUTHORIZED_PHASE_NAME:
AUTHORIZED_OBJECTIVE:
AUTHORIZED_ALLOWED_FILES:
AUTHORIZED_FORBIDDEN_FILES:
AUTHORIZED_ALLOWED_ACTIONS:
AUTHORIZED_FORBIDDEN_ACTIONS:
AUTHORIZED_EXIT_CRITERIA:
AUTHORIZED_ROLLBACK_RULE:
```

## Rollback Rule

Revert Phase 6A commits if:

- A forbidden surface is touched
- Product-facing work is implied
- Product implementation is authorized without later explicit scoped approval
- Executable planning is authorized without later explicit scoped approval
- SDD Guard returns `FAIL` or `STOP`

## Final Boundary

Phase 6A is a governance lock, not a product phase.

The lock exists so future work cannot start by accident.
