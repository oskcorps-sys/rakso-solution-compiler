# SDD Guard Check Matrix

## Classification

This document defines the read-only check matrix for SDD Guard.

SDD Guard checks are governance checks only. They do not authorize product work, implementation planning, Phase 6 work, runtime creation, scripts, agents, workflows, integrations, schemas, modules, tests, deployment, or source code changes.

## Current Baseline

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch active
- Completed phases: `[0, 1, 2, 3, 4, 5]`
- Baseline commit before this check matrix: `c8cfa3516684992615c01dfa39f21dfc89a95777`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized

## Default Allowed Inspection Surface

SDD Guard checks may inspect only:

- `README.md`
- `docs/sdd-guard/SDD_GUARD_CONTRACT.md`
- `docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md`
- `docs/sdd-guard/SDD_GUARD_CHECKS.md`
- Explicit SDD+ state or phase documents when identified by name in a committed SDD+ contract

## Default Forbidden Inspection Surface

Unless explicitly authorized by a committed SDD+ contract, SDD Guard must not inspect or operate on:

- `src/**`
- `app/**`
- `lib/**`
- `modules/**`
- `agents/**`
- `workflows/**`
- `integrations/**`
- `runtime/**`
- `deploy/**`
- `supabase/**`
- `schemas/**`
- `scripts/**`
- `tests/**`
- `.github/**`

## Check Output Contract

Every check must return:

```text
CHECK_ID:
STATUS: PASS | FAIL | REVIEW_REQUIRED | STOP
FILES_INSPECTED:
FORBIDDEN_SURFACE_TOUCHED: yes | no
FINDINGS:
NEXT_ALLOWED_ACTION:
```

A check must return `STOP` when it cannot determine whether the inspected surface is authorized.

## Finding Classification

Findings must use one of these classifications:

- `protective_usage` - term appears in a prohibition, boundary, warning, or authorization denial
- `future_non_authorized_usage` - term appears as long-term doctrine or conceptual future direction, explicitly marked as not currently authorized
- `risky_usage` - term may imply current authorization, lifecycle movement, or implementation readiness
- `violation_candidate` - term appears to authorize, plan, create, run, deploy, or execute forbidden work

## CHECK-001: State Summary Check

### Purpose

Confirm that the current governance documents preserve the known SDD+ state.

### Inputs

- `README.md`
- `docs/sdd-guard/SDD_GUARD_CONTRACT.md`
- `docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md`
- `docs/sdd-guard/SDD_GUARD_CHECKS.md`

### Required Assertions

- Phase 5 is completed
- Phase 5.1 is governance-only
- Completed phases are `[0, 1, 2, 3, 4, 5]`
- Product implementation is absent or not authorized
- Product build authorization is absent or not authorized
- Executable implementation planning is absent or not authorized
- Phase 6 product work is not authorized

### PASS Criteria

All required assertions are present or preserved without contradiction.

### FAIL Criteria

Any inspected document directly contradicts the current state.

### REVIEW_REQUIRED Criteria

A document uses unclear wording that could be interpreted as current implementation authorization.

## CHECK-002: Authorization Boundary Check

### Purpose

Confirm that current authorization remains closed.

### Required Denials

The inspected surface must deny current authorization for:

- Product implementation
- Product build
- Executable implementation planning
- Phase 6 product work
- Runtime
- Agents
- Workflows
- Integrations
- Schemas
- Modules
- Scripts
- Tests
- Deployment
- Source code
- Application code
- Infrastructure
- CI or GitHub Actions
- Supabase configuration
- External service integration

### PASS Criteria

All relevant denials are present and no contradictory authorization appears.

### FAIL Criteria

Any inspected document grants or implies current authorization for a forbidden scope.

### REVIEW_REQUIRED Criteria

Any inspected document uses future implementation language without explicit non-authorization wording.

## CHECK-003: Stale Lifecycle Wording Scan

### Purpose

Detect language that may suggest unauthorized lifecycle movement.

### Terms To Review

```text
build
implement
implementation
runtime
agent
workflow
integration
schema
module
deploy
deployment
production
script
test
source code
application code
infrastructure
CI
GitHub Actions
Supabase
external service
```

### Classification Rules

- If the term appears inside a prohibition or denial, classify as `protective_usage`
- If the term appears as explicitly future and non-authorized, classify as `future_non_authorized_usage`
- If the term appears without authorization context, classify as `risky_usage`
- If the term appears as an instruction to create, run, plan, deploy, or implement, classify as `violation_candidate`

### PASS Criteria

All lifecycle terms are protective or future non-authorized.

### REVIEW_REQUIRED Criteria

One or more terms are risky but not clearly violating.

### FAIL Criteria

One or more terms are violation candidates.

## CHECK-004: Contract Status Mismatch Check

### Purpose

Detect contradictions between the SDD Guard contract, the report template, the check matrix, and README boundary language.

### Required Consistency Points

- SDD Guard is governance-only
- SDD Guard is not Phase 6
- SDD Guard cannot authorize product work
- SDD Guard cannot infer missing authorization
- SDD Guard cannot override SDD+ contracts
- SDD Guard can only inspect, report, and recommend from a closed action set
- README must not override or weaken the SDD Guard contract

### PASS Criteria

No contradictions found.

### REVIEW_REQUIRED Criteria

Wording differs but does not clearly contradict the contract.

### FAIL Criteria

A document grants broader power than the SDD Guard contract allows.

## CHECK-005: Forbidden Surface Scan

### Purpose

Confirm that an SDD Guard run did not inspect or modify forbidden surfaces.

### PASS Criteria

- Only allowed files are inspected
- No forbidden directories are inspected
- No files are modified during read-only checks

### FAIL Criteria

- Any forbidden surface is inspected without explicit authorization
- Any file is modified during a read-only check
- Any product directory is touched

### STOP Criteria

The check cannot determine whether a path is allowed.

## CHECK-006: Next Allowed Action Check

### Purpose

Ensure every report ends with a next action from the closed allowed set.

### Closed Allowed Action Set

- `create_sdd_guard_contract`
- `create_sdd_guard_report_template`
- `run_governance_scan`
- `patch_governance_docs`
- `request_phase_6_authorization`
- `stop`

### Disallowed Next Actions

- `implement_product`
- `build_phase_6`
- `create_runtime`
- `create_agent`
- `create_schema`
- `create_workflow`
- `create_integration`
- `deploy`
- `create_script`
- `run_tests`
- `modify_source_code`

### PASS Criteria

The next action is from the closed allowed set.

### FAIL Criteria

The next action is outside the closed allowed set or implies product work.

## CHECK-007: Exact Next Command Check

### Purpose

Ensure the recommended command is PowerShell-compatible and governance-safe.

### PASS Criteria

The command:

- Is PowerShell-compatible
- Is read-only unless the next action is `patch_governance_docs`
- Does not scan repository-wide unless explicitly authorized
- Does not touch forbidden surfaces
- Does not create scripts
- Does not begin Phase 6

### FAIL Criteria

The command touches product surfaces, creates executable files, runs tests, deploys, modifies source code, or begins Phase 6.

### REVIEW_REQUIRED Criteria

The command is ambiguous or depends on external unstated authorization.

## CHECK-008: Gate Readiness Check

### Purpose

Summarize whether the repository is ready for the next governance action.

### Required Gates

- State Integrity Gate
- No Product Surface Gate
- No Forbidden Drift Gate
- Next Action Lock Gate

### PASS Criteria

All required gates pass.

### REVIEW_REQUIRED Criteria

At least one gate needs human review, but no direct violation is found.

### FAIL Criteria

At least one gate fails due to contradiction or unauthorized scope.

### STOP Criteria

The check cannot determine the authorized state.

## Minimum Report Order

A complete SDD Guard scan should run checks in this order:

1. CHECK-001: State Summary Check
2. CHECK-002: Authorization Boundary Check
3. CHECK-003: Stale Lifecycle Wording Scan
4. CHECK-004: Contract Status Mismatch Check
5. CHECK-005: Forbidden Surface Scan
6. CHECK-006: Next Allowed Action Check
7. CHECK-007: Exact Next Command Check
8. CHECK-008: Gate Readiness Check

## Non-Negotiable Stop Rule

If any check returns `STOP`, SDD Guard must stop the scan and report uncertainty.

Uncertainty is not permission.
