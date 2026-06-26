# SDD Guard Governance Contract

## Classification

SDD Guard is a governance-only accelerator for SDD+.

It exists to reduce phase execution time by making SDD+ state, contract consistency, gate readiness, and next allowed actions easier to inspect.

SDD Guard is not Phase 6.
SDD Guard is not product work.
SDD Guard is not a product implementation plan.
SDD Guard is not an executable runtime.
SDD Guard is not authorized to create, modify, or plan product surfaces.

## Current Confirmed State

- Phase 5: completed
- Completed phases: `[0, 1, 2, 3, 4, 5]`
- Confirmed commit: `e1d38aaaf6a73001603b88a8eeb2a2cc59f7d063`
- Product implementation: absent
- Product build authorization: absent
- Executable implementation planning: absent
- Phase 6 product work: not authorized

## Purpose

SDD Guard may only help verify whether the repository and SDD+ governance documents remain consistent with the committed SDD+ state.

Its purpose is to support governance review, not to expand scope.

## Allowed Scope

SDD Guard may perform or request read-only governance checks for:

1. State summary
2. Stale lifecycle wording scan
3. Contract status mismatch scan
4. `next_allowed_action` scan
5. Forbidden surface scan
6. Gate readiness reporting
7. Exact next command recommendation

All checks must remain limited to authorized governance and documentation surfaces unless a committed SDD+ contract explicitly permits a broader scan.

## Forbidden Scope

SDD Guard must not create, modify, plan, or authorize any of the following:

- Product implementation
- Product build work
- Executable implementation planning
- Phase 6 product work
- Runtime systems
- Agents
- Workflows
- Integrations
- Schemas
- Modules
- Product prompts
- Product tools
- Scripts
- Tests
- Deployment configuration
- Infrastructure
- CI or GitHub Actions
- Source code
- Application code
- Supabase configuration
- External service integration

## Authority Boundary

SDD Guard can report.
SDD Guard can recommend within a closed set of allowed governance actions.
SDD Guard cannot authorize work.
SDD Guard cannot override SDD+ contracts.
SDD Guard cannot infer missing authorization.
SDD Guard cannot treat speed, convenience, or automation value as permission.

## Closed Next Allowed Action Set

SDD Guard outputs may recommend only one of the following actions:

- `create_sdd_guard_contract`
- `create_sdd_guard_report_template`
- `run_governance_scan`
- `patch_governance_docs`
- `request_phase_6_authorization`
- `stop`

SDD Guard must never recommend:

- `implement_product`
- `build_phase_6`
- `create_runtime`
- `create_agent`
- `create_schema`
- `create_workflow`
- `create_integration`
- `deploy`

## Scan Surface Policy

Default allowed scan surfaces:

- `README.md`
- `CHANGELOG.md`
- `docs/sdd-guard/SDD_GUARD_CONTRACT.md`
- `docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md`
- `docs/sdd-guard/SDD_GUARD_CHECKS.md`
- `docs/sdd-guard/CODEX_TASKS.md`
- `docs/sdd-guard/PHASE_6_AUTHORIZATION_PACKET.md`
- Explicit SDD+ state or phase documents when identified by name

Default forbidden scan surfaces unless explicitly authorized by committed SDD+ contract:

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

## Finding Classification

A forbidden or lifecycle term is not automatically a violation.

Findings must be classified as:

- `protective_usage` - the term appears in a prohibition or boundary statement
- `risky_usage` - the term may imply unauthorized lifecycle movement
- `violation_candidate` - the term appears to authorize or plan forbidden work

## Required Guard Metadata

Every SDD Guard report must include:

- Guard contract version
- SDD+ state reference
- Commit or ref inspected
- Assumption date
- Authorization status
- Scan surface used
- Whether product surfaces were avoided

## Non-Negotiable Rule

When unsure, SDD Guard must stop and report uncertainty.

Uncertainty is not permission.
