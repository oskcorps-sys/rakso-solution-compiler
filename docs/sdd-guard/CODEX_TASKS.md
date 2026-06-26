# SDD Guard Codex Task Templates

## Classification

This document contains compact Codex task templates for running SDD Guard governance checks safely.

These templates are documentation only. They are not scripts, prompts for product runtime, agents, workflows, integrations, schemas, modules, tests, deployment instructions, or Phase 6 work.

## Current Baseline

- Phase 5: completed
- Phase 5.1: SDD Guard Governance Patch active
- Latest SDD Guard baseline before this file: `f827c95c3c4bde5e64cf2bfac6544f0457c9e058`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized

## Global Codex Constraints

Every task in this file inherits these constraints:

```text
Do not modify files unless the task explicitly says patch_governance_docs.
Do not create scripts.
Do not create tests.
Do not scan repository-wide.
Do not inspect product directories.
Do not create or modify source code.
Do not create runtime, agents, workflows, integrations, schemas, modules, tools, prompts, infrastructure, CI, deployment, or Supabase configuration.
Do not begin Phase 6.
Do not infer authorization.
If authorization is unclear, stop and report uncertainty.
```

## Allowed Inspection Files

```text
README.md
docs/sdd-guard/SDD_GUARD_CONTRACT.md
docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
docs/sdd-guard/SDD_GUARD_CHECKS.md
docs/sdd-guard/CODEX_TASKS.md
```

## Forbidden Surface

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

---

# TASK-001: State Summary

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-001 State Summary Check.

Inspect only:
- README.md
- docs/sdd-guard/SDD_GUARD_CONTRACT.md
- docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
- docs/sdd-guard/SDD_GUARD_CHECKS.md
- docs/sdd-guard/CODEX_TASKS.md

Report:
- Current phase position
- Completed phases
- Last known commit
- Product implementation authorization status
- Product build authorization status
- Executable implementation planning status
- Phase 6 authorization status

Do not modify files.
Do not scan repository-wide.
Do not begin Phase 6.
```

---

# TASK-002: Authorization Boundary

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-002 Authorization Boundary Check.

Inspect only allowed SDD Guard governance files and README.md.

Confirm current authorization is denied for:
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

Return PASS, FAIL, REVIEW_REQUIRED, or STOP.

Do not modify files.
Do not create scripts.
Do not scan product directories.
```

---

# TASK-003: Stale Lifecycle Wording Scan

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-003 Stale Lifecycle Wording Scan.

Inspect only allowed governance files and README.md.

Review these terms:
build, implement, implementation, runtime, agent, workflow, integration, schema, module, deploy, deployment, production, script, test, source code, application code, infrastructure, CI, GitHub Actions, Supabase, external service.

Classify findings as:
- protective_usage
- future_non_authorized_usage
- risky_usage
- violation_candidate

Return file path, line reference, classification, and reason.

Do not edit.
Do not scan repository-wide.
Do not touch forbidden surface.
```

---

# TASK-004: Contract Status Mismatch

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-004 Contract Status Mismatch Check.

Inspect only:
- README.md
- docs/sdd-guard/SDD_GUARD_CONTRACT.md
- docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
- docs/sdd-guard/SDD_GUARD_CHECKS.md
- docs/sdd-guard/CODEX_TASKS.md

Check for contradictions against:
- SDD Guard is governance-only
- SDD Guard is not Phase 6
- SDD Guard cannot authorize product work
- SDD Guard cannot infer missing authorization
- SDD Guard cannot override SDD+ contracts
- SDD Guard can only inspect, report, and recommend from a closed action set
- README must not override or weaken the SDD Guard contract

Do not modify files.
Report only mismatches.
```

---

# TASK-005: Forbidden Surface Confirmation

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-005 Forbidden Surface Scan.

Confirm that this SDD Guard run inspected only allowed files and did not inspect or modify:
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

Return:
- files inspected
- forbidden surface touched: yes/no
- unauthorized product directory scan detected: yes/no

Do not modify files.
Do not scan repository-wide.
```

---

# TASK-006: Next Allowed Action

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-006 Next Allowed Action Check.

Return exactly one NEXT_ALLOWED_ACTION from:
- create_sdd_guard_contract
- create_sdd_guard_report_template
- run_governance_scan
- patch_governance_docs
- request_phase_6_authorization
- stop

Never return:
- implement_product
- build_phase_6
- create_runtime
- create_agent
- create_schema
- create_workflow
- create_integration
- deploy
- create_script
- run_tests
- modify_source_code

Do not modify files.
```

---

# TASK-007: Exact Next Command

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-007 Exact Next Command Check.

Recommend one PowerShell-compatible command for the next allowed governance action.

The command must:
- Be governance-safe
- Avoid repository-wide scan unless explicitly authorized
- Avoid product directories
- Avoid script creation
- Avoid tests
- Avoid deployment
- Avoid Phase 6 work

Return only:
- command
- reason
- risk level: low | medium | high

Do not modify files.
```

---

# TASK-008: Gate Readiness

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run CHECK-008 Gate Readiness Check.

Evaluate:
- State Integrity Gate
- No Product Surface Gate
- No Forbidden Drift Gate
- Next Action Lock Gate

Return:
- PASS / FAIL / REVIEW_REQUIRED / STOP for each gate
- overall GUARD_VERDICT
- exact NEXT_ALLOWED_ACTION

Do not modify files.
Do not begin Phase 6.
```

---

# TASK-009: Full SDD Guard Scan

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Run the full SDD Guard scan using this order:
1. CHECK-001 State Summary Check
2. CHECK-002 Authorization Boundary Check
3. CHECK-003 Stale Lifecycle Wording Scan
4. CHECK-004 Contract Status Mismatch Check
5. CHECK-005 Forbidden Surface Scan
6. CHECK-006 Next Allowed Action Check
7. CHECK-007 Exact Next Command Check
8. CHECK-008 Gate Readiness Check

Inspect only:
- README.md
- docs/sdd-guard/SDD_GUARD_CONTRACT.md
- docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
- docs/sdd-guard/SDD_GUARD_CHECKS.md
- docs/sdd-guard/CODEX_TASKS.md

Stop immediately if any check returns STOP.

Return:
- SDD Guard Report
- Final GUARD_VERDICT
- NEXT_ALLOWED_ACTION
- PowerShell-compatible next command

Do not modify files.
Do not create scripts.
Do not scan repository-wide.
Do not begin Phase 6.
```

---

# TASK-010: Governance Docs Patch Proposal

```text
Repo: /workspace/rakso-solution-compiler
Framework: /workspace/sdd-plus

Task:
Prepare a patch proposal for governance docs only.

Allowed patch surface:
- README.md
- docs/sdd-guard/SDD_GUARD_CONTRACT.md
- docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
- docs/sdd-guard/SDD_GUARD_CHECKS.md
- docs/sdd-guard/CODEX_TASKS.md

Do not apply the patch unless explicitly instructed.

Proposal must include:
- file path
- issue found
- proposed wording
- reason
- risk level

Forbidden:
- product files
- scripts
- tests
- source code
- runtime
- agents
- workflows
- schemas
- integrations
- deployment
- Phase 6 work
```

## Non-Negotiable Stop Rule

If Codex cannot determine whether an action is authorized, it must stop and report uncertainty.

Uncertainty is not permission.
