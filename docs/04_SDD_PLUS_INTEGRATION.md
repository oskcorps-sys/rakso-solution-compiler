# SDD+ Integration Policy

## Core Position

RAKSO Solution Compiler is built under SDD+ governance.

SDD+ is the rules engine and contract system that keeps RAKSO evidence-backed, scope-controlled, tool-agnostic, and audit-ready.

SDD+ is not a permanent production bottleneck. Its intensity changes by lifecycle mode.

## Lifecycle Doctrine

```txt
SDD+ governs uncertainty.
Contracts govern execution.
Tests govern behavior.
Audits govern drift.
The human operator governs direction.
```

## SDD+ Lifecycle Roles

| Mode | SDD+ Role |
|---|---|
| Discovery Mode | Govern strongly, force evidence, block premature design |
| Contract Mode | Close scope, define allowed and forbidden surfaces, define acceptance criteria |
| Build Mode | Verify executor stays inside the committed contract |
| Audit Mode | Check results against contract, acceptance criteria, drift, and forbidden surface |
| Maintenance Mode | Control future changes, regression risk, rollback, and scope drift |

## RAKSO Solution Compiler Role

RAKSO Solution Compiler extends SDD+ with business-specific framework artifacts:

- Evidence Ledger
- Business Reality Diagnosis
- Pain-to-Profit Map
- Offer Direction
- Solution Type Decision
- Discovery-to-Contract Bridge
- Repository Boundary
- Velocity Mode
- Critical Lens

These are generic compiler capabilities, not vehicle-specific product artifacts.

## Repository Boundary

This repository contains RAKSO OS and compiler framework only.

Vehicle-specific work belongs in separate vehicle repositories or workspaces.

TaxPak, Bookkeeping AI, Credit tools, and future vehicles may use the compiler framework, but their discovery, scope, contracts, MVPs, and build plans must not live in this repo.

## Binding Principle

```txt
Specifications are binding.
Contracts define allowed work.
Code follows contract, not vice versa.
Audit is independent and impartial.
```

For this repo, the principle expands into:

```txt
Business reality becomes evidence.
Evidence becomes diagnosis.
Diagnosis becomes money logic.
Money logic becomes offer direction.
Offer direction becomes SDD+ contract.
Contract becomes authorized execution only when explicitly permitted.
```

## Capability Hierarchy

| Level | Capability | Role |
|---|---|---|
| 0 | Human Operator | Final direction and approval |
| 1 | SDD+ | Rules engine and contract authority |
| 2 | RAKSO Solution Compiler | Business-to-contract framework |
| 3 | Source of Truth | Versioned state, committed artifacts, audit trail |
| 4 | Executors | Authorized work inside contract boundaries |
| 5 | External Audit | Independent validation and red-team review |
| 6 | Drift Guard | Lightweight state and boundary checks |

Capability roles may be filled by different tools over time. Vendor names are examples, not dependencies.

## Mapping

| SDD+ concept | RAKSO Solution Compiler usage |
|---|---|
| Project genesis | No project starts from code, prompt, automation, or agent design |
| Spec-first workflow | Business reality becomes structured artifacts before implementation |
| Independent audit gates | Builder and auditor must be different roles or review paths |
| State machine | Major work moves through lifecycle states before approval |
| Role enforcement | Executors and auditors have distinct responsibilities |
| Audit loop | Artifacts pass contract, Critical Lens, and independent review |
| Telemetry | Important transitions and audits should be logged |
| Tool-agnostic execution | Models, executors, auditors, repo hosts, and orchestrators may be replaced |
| Repository boundary | Vehicles stay outside the compiler repo |
| Velocity Mode | Authorized work should not be delayed by repeated permission loops |

## Required Flow For Framework Or Vehicle Genesis

```txt
Idea / Business Need / Client Chaos
  -> Evidence
  -> Diagnosis
  -> Money Logic
  -> Offer Direction
  -> SDD+ Contract
  -> Human Approval
  -> Authorized Execution or Deferral
  -> Critical Lens Review
  -> External Audit when needed
  -> Fix Loop if needed
  -> Completed Artifact
```

## Builder != Auditor

The executor that builds or modifies an artifact cannot be the only reviewer that approves it.

Allowed patterns:

- AI executor builds, human audits
- Human builds, AI audits
- One model builds, another model audits
- Primary executor builds, external auditor reviews
- Manual artifact is reviewed by Critical Lens and independent audit

Forbidden pattern:

- Builder builds and self-approves without independent audit or human authority

## Minimum Gate Before Important Completion

No important artifact is complete unless it has:

1. SDD+ contract or doctrine reference
2. acceptance criteria or clear purpose
3. Critical Lens review when applicable
4. independent audit when risk justifies it
5. human approval or explicit direction
6. repository-boundary compliance

## State Model Alignment

SDD+ lifecycle states:

```txt
DRAFT -> REFINED -> LOCKED -> IMPLEMENTING -> AUDITING -> COMPLETED
```

RAKSO interpretation:

- `DRAFT`: idea or rough artifact exists
- `REFINED`: evidence and scope clarified
- `LOCKED`: contract frozen for authorized work
- `IMPLEMENTING`: builder is producing authorized artifact
- `AUDITING`: Critical Lens or external audit is reviewing the artifact
- `COMPLETED`: approved, versioned, and ready for next action

## Enforcement Policy

Current enforcement is documentation and review based.

Future enforcement may include:

- SDD Guard CLI
- CI checks
- forbidden-surface scanner
- vehicle-boundary scanner
- lifecycle-state validator

Those automation surfaces must be explicitly authorized before implementation.

## Rules

```txt
Every RAKSO project begins under evidence and SDD+ discipline.
No project starts directly from code, prompt, automation, or agent design.
No SDD+ contract, no build.
No independent review, no important completion.
No vehicle-specific discovery inside the compiler repo.
No repeated approval loop when a committed contract already authorizes the work.
```
