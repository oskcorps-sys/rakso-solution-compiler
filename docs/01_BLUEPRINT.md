# RAKSO Solution Compiler Blueprint

## Definition

RAKSO Solution Compiler is an internal system for turning messy business reality into governed solution evidence, bounded scope, and eventually executable delivery only when SDD+ explicitly authorizes it.

The current repository is not in product-build mode. It is in an SDD+ governed lifecycle where each phase must be specified, contracted, implemented within scope, audited, and completed before later authority can exist.

## Operating Governance

SDD+ is the operating governance for this repository. It is not an optional add-on, integration, or documentation layer.

The active source of truth is the SDD+ artifact chain:

- `sdd/artifacts/STATE_SNAPSHOT.yaml`
- `sdd/artifacts/PHASE_1_DISCOVERY.yaml`
- `sdd/artifacts/PHASE_2_BOUNDARY.yaml`
- `sdd/artifacts/PHASE_3_READINESS.yaml`
- `sdd/artifacts/PHASE_4_ARCHITECTURE.yaml`

Committed SDD+ contracts define what work is allowed. `STATE_SNAPSHOT.yaml` defines the lifecycle state. Public docs are explanatory only and cannot authorize implementation, schemas, modules, integrations, workflows, prompts, tools, agents, AI behavior, runtime orchestration, implementation planning, or product build.

## Completed SDD+ Phase Chain

Phase 0: Genesis / governance setup - COMPLETED

- Established the SDD+ lifecycle foundation.
- Created the initial state snapshot and governance baseline.
- Product implementation was not authorized.

Phase 1: Discovery and problem definition - COMPLETED

- Output: `sdd/artifacts/PHASE_1_DISCOVERY.yaml`
- Defined the business problem, source-of-truth boundaries, evidence requirements, assumptions, open questions, non-goals, forbidden surface, and readiness criteria.
- Product implementation was not authorized.

Phase 2: Solution boundary definition - COMPLETED

- Output: `sdd/artifacts/PHASE_2_BOUNDARY.yaml`
- Defined solution-boundary decisions, allowed scope, evidence classification rules, open questions, deferrals, and forbidden surface.
- Product implementation was not authorized.

Phase 3: Architecture readiness definition - COMPLETED

- Output: `sdd/artifacts/PHASE_3_READINESS.yaml`
- Defined what evidence must exist before architecture can be authorized.
- Architecture design, implementation planning, and product build were not authorized.

Phase 4: Minimal architecture authorization - COMPLETED

- Output: `sdd/artifacts/PHASE_4_ARCHITECTURE.yaml`
- Authorized bounded/minimal architecture decisions and conceptual responsibility framing only.
- Product implementation, implementation planning, and product build remain forbidden.

## Current Architecture Rule

Phase 4 authorizes bounded/minimal architecture only.

Allowed current architecture surface:

- high-level architecture decisions traceable to Phase 3 readiness evidence
- conceptual component-boundary framing
- responsibility naming without executable design
- source-of-truth precedence
- readiness criteria for a later phase to decide whether implementation planning may be considered

Forbidden current surface:

- product implementation code
- product schemas
- executable modules
- runtime integrations
- automation workflows
- product artifacts
- prompts, tools, agents, or AI system behavior
- runtime orchestration
- executable interfaces or APIs
- data models
- infrastructure or deployment behavior
- workflow automation
- implementation planning
- product build authorization

## Conceptual Future Capabilities

Older blueprint layers remain useful vocabulary for future RAKSO Solution Compiler capability, but they are conceptual only unless a future committed SDD+ contract explicitly authorizes them.

Conceptual future layers include:

- Input Router
- Evidence Ledger
- Business Reality Diagnosis
- Pain-to-Profit Branch
- Offer Architecture Branch
- Solution Type Decision
- SDD+ Contract Builder
- SpellWriter / Artifact Compiler
- Execution Agent Profiles
- Deployment Package
- Market Expansion Loop

These names do not imply that product code, schemas, modules, integrations, workflows, prompts, tools, agents, AI behavior, runtime orchestration, implementation planning, or product build exists or is authorized now.

## Current System Shape

The current system shape is a governed SDD+ artifact chain through completed Phase 4:

```txt
STATE_SNAPSHOT.yaml
  -> PHASE_1_DISCOVERY.yaml
  -> PHASE_2_BOUNDARY.yaml
  -> PHASE_3_READINESS.yaml
  -> PHASE_4_ARCHITECTURE.yaml
```

The repository has completed governance discovery, solution boundary, architecture readiness, and minimal architecture authorization. It has not started implementation planning or product build.

## Non-Negotiable Rule

No product implementation begins until a later committed SDD+ contract explicitly authorizes it.

No implementation planning begins until a later committed SDD+ contract explicitly authorizes it.
