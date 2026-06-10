# SDD+ Integration Policy

RAKSO Solution Compiler uses SDD+ as its governance backbone.

Source repository:

```txt
https://github.com/oskcorps-sys/sdd-plus
```

## Why SDD+ is the base

SDD+ is a specification-driven, LLM-agnostic governance framework for AI-assisted development.

Its core principle is binding for this repo:

```txt
Specifications are binding. Code follows spec, not vice versa.
Audit is independent and impartial.
```

RAKSO Solution Compiler extends this idea from code into business solution design.

## Mapping

| SDD+ concept | RAKSO Solution Compiler usage |
|---|---|
| Spec-first workflow | Business reality must become structured artifacts before implementation |
| Independent audit gates | Builder and auditor must be different roles/executors |
| State machine | Major work must move through lifecycle states before approval |
| Role enforcement | Implementers and auditors have different file permissions |
| Audit loop | Artifacts must pass schema, contract, and Critical Lens review |
| Telemetry | Important transitions and audits should be logged |
| LLM-agnostic execution | Claude, Codex, GPT, Gemini, Ollama, or humans may execute roles |

## Required flow for implementation work

```txt
SDD+ Spec
  -> SDD+ Contract
  -> Implementation Issue
  -> Builder Execution
  -> Critical Lens Review
  -> External Audit
  -> Fix Loop
  -> Human Approval
  -> Merge
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

This repo should eventually use `AGENTS.yaml` role enforcement from SDD+.

Initial recommended roles:

- doctrine_owner
- implementer
- auditor
- example_author
- profile_author

Production mode should use `strict_allowlist` once schemas and module boundaries stabilize.

## Rule

No SDD+ contract, no build.

No independent audit, no merge.
