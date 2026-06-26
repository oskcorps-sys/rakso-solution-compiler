# SDD Guard Check Matrix

## Classification

This document defines the read-only check matrix for SDD Guard.

SDD Guard checks are governance checks only. They do not authorize product work, implementation planning, Phase 6 work, runtime creation, scripts, agents, workflows, integrations, schemas, modules, tests, deployment, or source code changes.

## Current Baseline

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch active
- Completed phases: `[0, 1, 2, 3, 4, 5]`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized unless explicitly approved, scoped, committed, and verified

## Default Allowed Inspection Surface

SDD Guard checks may inspect only:

- `README.md`
- `docs/sdd-guard/SDD_GUARD_CONTRACT.md`
- `docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md`
- `docs/sdd-guard/SDD_GUARD_CHECKS.md`
- `docs/sdd-guard/CODEX_TASKS.md`
- `docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md`
- Explicit SDD+ state or phase documents when identified by name in a committed SDD+ contract

## Default Forbidden Inspection Surface

Unless explicitly authorized by a committed SDD+ contract, SDD Guard must not inspect or operate on product, runtime, implementation, automation, deployment, infrastructure, CI, schema, integration, workflow, agent, script, test, source, application, or external-service surfaces.

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

- `protective_usage` - term appears in a prohibition, boundary, warning, or authorization denial
- `future_non_authorized_usage` - term appears as long-term doctrine or conceptual future direction, explicitly marked as not currently authorized
- `risky_usage` - term may imply current authorization, lifecycle movement, or implementation readiness
- `violation_candidate` - term appears to authorize, plan, create, run, deploy, or execute forbidden work

## CHECK-001: State Summary Check

Confirm that inspected governance documents preserve:

- Phase 5 completed
- Phase 5.1 governance-only
- Completed phases `[0, 1, 2, 3, 4, 5]`
- Product implementation absent or not authorized
- Product build authorization absent or not authorized
- Executable implementation planning absent or not authorized
- Phase 6 product work not authorized unless explicitly approved, scoped, committed, and verified

PASS when all assertions are preserved without contradiction.
FAIL when any inspected document contradicts current state.
REVIEW_REQUIRED when wording could be interpreted as current implementation authorization.

## CHECK-002: Authorization Boundary Check

Confirm that current authorization remains closed for product, build, executable planning, Phase 6 product work, runtime, agents, workflows, integrations, schemas, modules, scripts, tests, deployment, source, application, infrastructure, CI, Supabase, and external service scope unless explicitly approved, scoped, committed, and verified.

PASS when denials are present and no contradictory authorization appears.
FAIL when a document grants or implies current authorization for a forbidden scope.
REVIEW_REQUIRED when future implementation language lacks explicit non-authorization wording.

## CHECK-003: Stale Lifecycle Wording Scan

Review lifecycle terms including build, implement, implementation, runtime, agent, workflow, integration, schema, module, deploy, deployment, production, script, test, source code, application code, infrastructure, CI, GitHub Actions, Supabase, external service, Phase 6, authorization, and approved.

Classify each finding as protective, future non-authorized, risky, or violation candidate.

PASS when terms are protective or future non-authorized.
REVIEW_REQUIRED when terms are risky but not clearly violating.
FAIL when terms appear to authorize forbidden work.

## CHECK-004: Contract Status Mismatch Check

Detect contradictions between the SDD Guard contract, report template, check matrix, Codex tasks, Phase 6 authorization packet, and README boundary language.

Required consistency points:

- SDD Guard is governance-only
- SDD Guard is not Phase 6
- SDD Guard cannot authorize product work
- SDD Guard cannot infer missing authorization
- SDD Guard cannot override SDD+ contracts
- SDD Guard can only inspect, report, and recommend from a closed action set
- README must not override or weaken the SDD Guard contract
- The Phase 6 packet must remain a request unless explicitly approved, scoped, committed, and verified

## CHECK-005: Forbidden Surface Scan

PASS when only allowed files are inspected and no forbidden directories are inspected or modified.
FAIL when forbidden surface is inspected without explicit authorization or any file is modified during a read-only check.
STOP when the allowed status of a path cannot be determined.

## CHECK-006: Next Allowed Action Check

Allowed actions remain:

- `create_sdd_guard_contract`
- `create_sdd_guard_report_template`
- `run_governance_scan`
- `patch_governance_docs`
- `request_phase_6_authorization`
- `stop`

Any action that implies product work, Phase 6 work, runtime creation, agent creation, schema creation, workflow creation, integration creation, deployment, scripts, tests, or source changes fails this check.

## CHECK-007: Exact Next Command Check

The command must be PowerShell-compatible, governance-safe, and avoid repository-wide scans, product surfaces, script creation, tests, deployment, and Phase 6 work unless explicitly authorized.

## CHECK-008: Gate Readiness Check

Evaluate:

- State Integrity Gate
- No Product Surface Gate
- No Forbidden Drift Gate
- Next Action Lock Gate

PASS only when all required gates pass.
REVIEW_REQUIRED when at least one gate needs human review without direct violation.
FAIL when any gate fails due to contradiction or unauthorized scope.
STOP when authorized state cannot be determined.

## Minimum Report Order

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
