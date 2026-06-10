# RAKSO Solution Compiler Roadmap

## North Star

```txt
Technologies change. Agents change. Models change. Systems endure.

RAKSO builds systems first, then chooses tools.
```

## Governance rule

RAKSO Solution Compiler is developed under SDD+ Genesis Governance.

No important work starts from code, prompt, automation, or agent design.

Every phase must produce SDD+ artifacts before implementation.

## Core formula

```txt
Reality -> Evidence -> Diagnosis -> Money -> Offer -> Contract -> Execution
```

---

# Phase 0: SDD+ Genesis Setup

## Goal

Initialize this repository as a project born under SDD+.

## Deliverables

- SDD+ Phase 0 spec
- SDD+ Phase 0 contract
- SDD+ state snapshot
- initial `AGENTS.yaml` role matrix
- external audit policy
- phase acceptance criteria

## Exit criteria

- SDD+ lifecycle is initialized.
- Scope is clear.
- Builder and auditor roles are separated.
- No implementation work starts without a locked contract.

---

# Phase 1: Doctrine & Boundaries

## Goal

Define the system boundaries, language, artifacts, and non-negotiable rules.

## Deliverables

- `docs/00_DOCTRINE.md`
- `docs/01_BLUEPRINT.md`
- `docs/03_CRITICAL_LENS.md`
- `docs/04_SDD_PLUS_INTEGRATION.md`
- glossary
- initial module map

## Exit criteria

- The system is clearly not just a prompt generator, skill, SaaS, or lead research tool.
- The core formula is accepted.
- SDD+ is documented as Genesis Governance, not an optional integration.

---

# Phase 2: Manual Internal Workflow

## Goal

Prove the process manually before automating.

## Deliverables

- manual intake template
- evidence ledger template
- operational diagnosis template
- pain-to-profit template
- offer brief template
- SDD+ contract template
- first complete example from messy input to deployment package

## Exit criteria

- One messy client input produces a coherent evidence report, diagnosis, offer, SDD+ contract, and implementation brief.
- Critical Lens review is applied to the complete example.

---

# Phase 3: Structured Artifacts

## Goal

Convert templates into schemas and golden outputs.

## Deliverables

- JSON/YAML schemas under `sdd/schemas/`
- example cases under `examples/`
- golden outputs under `tests/golden-outputs/`
- validation checklist

## Required schemas

- `evidence_ledger.schema.yaml`
- `operational_diagnosis.schema.yaml`
- `pain_to_profit.schema.yaml`
- `offer_brief.schema.yaml`
- `solution_decision.schema.yaml`
- `sdd_contract.schema.yaml`

## Exit criteria

- Each artifact has a schema and at least one golden example.
- Schemas can be validated deterministically.

---

# Phase 4: SpellWriter Refactor

## Goal

Turn SpellWriter into a provider-agnostic artifact compiler.

## Deliverables

- Spell IR v1
- compiler interface
- target adapters: generic markdown, Claude, Codex, Antigravity
- artifact validation layer

## Exit criteria

- One SDD+ contract can compile to at least three target formats.
- No target runtime is hardcoded into the core.

---

# Phase 5: Agent Profile Compiler

## Goal

Convert agent profiles into runtime-specific instructions.

## Deliverables

- profile schema
- researcher profile
- coder profile
- devops profile
- discovery analyst profile
- offer architect profile
- critical lens profile
- outputs for SOUL.md, AGENTS.md, SKILL.md, and system prompt formats

## Exit criteria

- One agent profile can compile to at least three runtime formats.
- Execution profiles remain runtime-agnostic.

---

# Phase 6: Lead / Market Expansion

## Goal

Use validated pain patterns to generate lead hypotheses and outreach angles.

## Deliverables

- pain pattern schema
- ICP profile template
- lead research brief template
- outreach angle template
- micro-ad variations

## Exit criteria

- One validated client pain produces a target lead hypothesis and outreach package.
- Lead research is marked as hypothesis, not truth.

---

# Phase 7: Automation Runtime

## Goal

Automate parts of the internal workflow without hiding the reasoning.

## Deliverables

- local CLI or app prototype
- artifact generator
- validation runner
- audit logs

## Exit criteria

- The manual process can be executed semi-automatically while preserving Evidence Ledger and Critical Lens checkpoints.

---

# Phase 8: Productization Decision

## Goal

Decide whether this becomes an internal OS, paid service backend, SaaS, or hybrid.

## Deliverables

- packaging decision
- pricing model
- deployment model
- security model
- client-facing workflow

## Exit criteria

- Product path chosen based on real usage, not speculation.

---

# MVP v1 Scope

## Included

- SDD+ genesis setup
- manual input
- evidence ledger
- operational diagnosis
- pain-to-profit
- offer brief
- SDD+ contract
- basic artifact output

## Excluded for now

- full SaaS
- auth
- multi-tenant
- Supabase
- autonomous execution
- lead scraping
- complex agent bus
- marketplace

---

# Operating sequence for Codex

Codex must not start from vague instructions.

Every Codex task should have:

1. SDD+ contract reference
2. issue number
3. affected layer
4. acceptance criteria
5. forbidden actions
6. expected files
7. audit checklist

Codex builds. It does not self-approve.
