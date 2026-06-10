# SDD+ Genesis Governance Policy

RAKSO Solution Compiler is born under SDD+ Genesis Governance.

SDD+ is not a helper, add-on, or optional integration. It is the genesis governance framework for every project that RAKSO creates.

Source repository:

```txt
https://github.com/oskcorps-sys/sdd-plus
```

## Core position

```txt
SDD+ = Project Genesis OS
RAKSO Solution Compiler = Business Solution Genesis Module built under SDD+
```

SDD+ governs how a project is born, refined, locked, implemented, audited, completed, and evolved.

RAKSO Solution Compiler extends SDD+ with business-specific artifacts:

- Evidence Ledger
- Business Reality Diagnosis
- Pain-to-Profit
- Offer Architecture
- Solution Type Decision
- Market Expansion Loop

## Binding principle

```txt
Specifications are binding. Code follows spec, not vice versa.
Audit is independent and impartial.
```

For this repo, the principle expands into:

```txt
Business reality becomes evidence.
Evidence becomes diagnosis.
Diagnosis becomes money logic.
Money logic becomes offer.
Offer becomes SDD+ contract.
Contract becomes execution.
```

## Hierarchy

| Level | System | Role |
|---|---|---|
| 0 | SDD+ | Genesis governance framework |
| 1 | RAKSO Solution Compiler | Business solution generation module |
| 2 | SpellWriter / Artifact Compiler | Runtime artifact compiler |
| 3 | Codex / Claude / Antigravity / Human | Executors |
| 4 | External Auditor | Independent validation gate |

## Mapping

| SDD+ concept | RAKSO Solution Compiler usage |
|---|---|
| Project genesis | No project starts from code, prompt, automation, or agent design |
| Spec-first workflow | Business reality must become structured artifacts before implementation |
| Independent audit gates | Builder and auditor must be different roles/executors |
| State machine | Major work must move through lifecycle states before approval |
| Role enforcement | Implementers and auditors have different file permissions |
| Audit loop | Artifacts must pass schema, contract, and Critical Lens review |
| Telemetry | Important transitions and audits should be logged |
| LLM-agnostic execution | Claude, Codex, GPT, Gemini, Ollama, or humans may execute roles |

## Required flow for project genesis

```txt
Idea / Business Need / Client Chaos
  -> SDD+ Phase 0 Spec
  -> SDD+ Contract
  -> LOCKED Scope
  -> Implementation Issue
  -> Builder Execution
  -> Critical Lens Review
  -> External Audit
  -> Fix Loop
  -> Human Approval
  -> Completed Phase
```

## Builder != Auditor

The executor that builds an artifact cannot be the only executor that approves it.

Allowed patterns:

- Codex builds, ChatGPT audits
- Codex builds, Claude audits
- Claude builds, Codex audits
- Human builds, AI audits
- AI builds, human audits

Forbidden pattern:

- Builder builds and self-approves without independent audit

## Minimum gate before merge

No important artifact is complete unless it has:

1. SDD+ contract reference
2. acceptance criteria
3. schema validation when applicable
4. Critical Lens review
5. independent audit result
6. human approval for merge

## State model alignment

SDD+ state machine:

```txt
DRAFT -> REFINED -> LOCKED -> IMPLEMENTING -> AUDITING -> COMPLETED
```

RAKSO artifact interpretation:

- `DRAFT`: idea or rough artifact exists
- `REFINED`: evidence and scope clarified
- `LOCKED`: contract frozen for implementation
- `IMPLEMENTING`: builder is producing artifact
- `AUDITING`: external audit and Critical Lens review
- `COMPLETED`: approved, versioned, and ready for next phase

## Enforcement policy

This repo should use `AGENTS.yaml` role enforcement from SDD+ once the initial Phase 0 contract is ready.

Initial recommended roles:

- doctrine_owner
- implementer
- auditor
- example_author
- profile_author

Production mode should use `strict_allowlist` once schemas and module boundaries stabilize.

## Rules

```txt
Every RAKSO project begins under SDD+.
No project starts directly from code, prompt, automation, or agent design.
No SDD+ contract, no build.
No independent audit, no merge.
```
