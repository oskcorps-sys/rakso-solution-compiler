# SDD Guard Report Template

## Report Metadata

- Guard contract version:
- SDD+ state reference:
- Inspected commit or ref:
- Assumption date:
- Scan surface used:
- Product surfaces avoided: yes/no

## 1. Current State

- Current phase position:
- Completed phases:
- Last confirmed commit:
- Phase 5 status:
- Phase 6 authorization status:
- Product implementation status:
- Product build authorization status:
- Executable implementation planning status:

Expected current baseline:

```text
Phase 5 completed
completed_phases: [0,1,2,3,4,5]
commit: e1d38aaaf6a73001603b88a8eeb2a2cc59f7d063
product implementation absent
product build authorization absent
executable implementation planning absent
Phase 6 product work not authorized
```

## 2. Authorization Status

- Product implementation authorized: yes/no
- Product build authorized: yes/no
- Executable implementation planning authorized: yes/no
- Runtime creation authorized: yes/no
- Agent creation authorized: yes/no
- Workflow creation authorized: yes/no
- Integration creation authorized: yes/no
- Schema creation authorized: yes/no
- Deployment authorized: yes/no

Required default unless a committed SDD+ contract states otherwise:

```text
All authorization values must be no.
```

## 3. Contract Consistency

- Status: pass/fail/review_required
- Mismatches found:
- Stale lifecycle wording found:
- Files reviewed:

Finding format:

```text
- file:
  line:
  finding:
  classification: protective_usage | risky_usage | violation_candidate
  reason:
```

## 4. Forbidden Surface Scan

- Status: pass/fail/review_required
- Allowed governance files inspected:
- Forbidden surfaces avoided: yes/no
- Unauthorized product directory scan detected: yes/no
- Findings:

Default allowed inspection surface:

```text
README.md
CHANGELOG.md
docs/sdd-guard/SDD_GUARD_CONTRACT.md
docs/sdd-guard/SDD_GUARD_REPORT_TEMPLATE.md
docs/sdd-guard/SDD_GUARD_CHECKS.md
docs/sdd-guard/CODEX_TASKS.md
Explicit SDD+ state or phase documents when identified by name
```

Forbidden surfaces unless explicitly authorized:

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

## 5. Lifecycle Wording Review

Terms to review:

```text
build
implement
runtime
agent
workflow
integration
schema
module
deploy
production
script
test
```

Classification rules:

- `protective_usage`: term appears inside a prohibition or boundary statement
- `risky_usage`: term may imply unauthorized lifecycle movement
- `violation_candidate`: term appears to authorize, plan, or execute forbidden work

## 6. Gate Readiness

- State Integrity Gate: pass/fail/review_required
- No Product Surface Gate: pass/fail/review_required
- No Forbidden Drift Gate: pass/fail/review_required
- Next Action Lock Gate: pass/fail/review_required

Gate notes:

```text
State Integrity Gate verifies the confirmed phase and commit state.
No Product Surface Gate verifies no product work is authorized or created.
No Forbidden Drift Gate verifies no unauthorized lifecycle wording drift.
Next Action Lock Gate verifies the next action is from the closed allowed set.
```

## 7. Next Allowed Action

Choose exactly one:

```text
NEXT_ALLOWED_ACTION: create_sdd_guard_contract
NEXT_ALLOWED_ACTION: create_sdd_guard_report_template
NEXT_ALLOWED_ACTION: run_governance_scan
NEXT_ALLOWED_ACTION: patch_governance_docs
NEXT_ALLOWED_ACTION: request_phase_6_authorization
NEXT_ALLOWED_ACTION: stop
```

Never output:

```text
NEXT_ALLOWED_ACTION: implement_product
NEXT_ALLOWED_ACTION: build_phase_6
NEXT_ALLOWED_ACTION: create_runtime
NEXT_ALLOWED_ACTION: create_agent
NEXT_ALLOWED_ACTION: create_schema
NEXT_ALLOWED_ACTION: create_workflow
NEXT_ALLOWED_ACTION: create_integration
NEXT_ALLOWED_ACTION: deploy
```

## 8. Exact Next Command Recommendation

PowerShell-compatible command only.

Command:

```powershell

```

Constraints:

- Must not scan repository-wide unless explicitly authorized
- Must not touch product directories
- Must not create scripts
- Must not create product files
- Must not begin Phase 6

## 9. Final Guard Verdict

Choose one:

```text
GUARD_VERDICT: PASS
GUARD_VERDICT: FAIL
GUARD_VERDICT: REVIEW_REQUIRED
GUARD_VERDICT: STOP
```

Reason:

```text

```
