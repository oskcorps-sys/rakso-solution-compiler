# RAKSO Solution Compiler Roadmap

## Phase 0: Doctrine & Scope

Goal: define the system boundaries, language, artifacts, and non-negotiable rules.

Deliverables:

- `docs/00_DOCTRINE.md`
- `docs/01_BLUEPRINT.md`
- `docs/03_CRITICAL_LENS.md`
- glossary
- initial module map

Exit criteria:

- The system is clearly not just a prompt generator, skill, SaaS, or lead research tool.
- The core formula is accepted: Reality -> Evidence -> Diagnosis -> Money -> Offer -> Contract -> Execution.

## Phase 1: Manual Internal Workflow

Goal: prove the process manually before automating.

Deliverables:

- manual intake template
- evidence ledger schema
- operational diagnosis template
- pain-to-profit template
- offer brief template
- SDD+ contract template
- first complete example from messy input to deployment package

Exit criteria:

- One messy client input produces a coherent evidence report, diagnosis, offer, SDD+ contract, and implementation brief.

## Phase 2: Structured Artifacts

Goal: convert templates into schemas and golden outputs.

Deliverables:

- JSON/YAML schemas under `sdd/schemas/`
- example cases under `examples/`
- golden outputs under `tests/golden-outputs/`
- validation checklist

Exit criteria:

- Each artifact has a schema and at least one golden example.

## Phase 3: SpellWriter Refactor

Goal: turn SpellWriter into a provider-agnostic artifact compiler.

Deliverables:

- Spell IR v1
- compiler interface
- target adapters: generic markdown, Claude, Codex, Antigravity
- artifact validation layer

Exit criteria:

- One SDD+ contract can compile to at least three target formats.

## Phase 4: Agent Profile Compiler

Goal: convert agent profiles into runtime-specific instructions.

Deliverables:

- profile schema
- researcher profile
- coder profile
- devops profile
- critical lens profile
- outputs for SOUL.md, AGENTS.md, SKILL.md, and system prompt formats

Exit criteria:

- One agent profile can compile to at least three runtime formats.

## Phase 5: Lead / Market Expansion

Goal: use validated pain patterns to generate lead hypotheses and outreach angles.

Deliverables:

- pain pattern schema
- ICP profile template
- lead research brief template
- outreach angle template
- micro-ad variations

Exit criteria:

- One validated client pain produces a target lead hypothesis and outreach package.

## Phase 6: Automation Runtime

Goal: automate parts of the internal workflow without hiding the reasoning.

Deliverables:

- local CLI or app prototype
- artifact generator
- validation runner
- audit logs

Exit criteria:

- The manual process can be executed semi-automatically while preserving Evidence Ledger and Critical Lens checkpoints.

## Phase 7: Productization

Goal: decide whether this becomes an internal OS, paid service backend, SaaS, or hybrid.

Deliverables:

- packaging decision
- pricing model
- deployment model
- security model
- client-facing workflow

Exit criteria:

- Product path chosen based on real usage, not speculation.

## MVP v1 Scope

Included:

- manual input
- evidence ledger
- operational diagnosis
- pain-to-profit
- offer brief
- SDD+ contract
- basic artifact output

Excluded for now:

- full SaaS
- auth
- multi-tenant
- Supabase
- autonomous execution
- lead scraping
- complex agent bus
- marketplace
