# RAKSO Solution Compiler Roadmap Status

## Current Verdict

The RAKSO Solution Compiler framework is sufficiently closed to process the first vehicle through a separate workspace or repository.

It is not a product runtime.
It is not a SaaS.
It is not TaxPak.
It is the framework layer that processes vehicles.

## Completed SDD+ Chain

### Phase 0 - Genesis Setup

Status: COMPLETED

Output: SDD+ lifecycle initialized, state snapshot, initial contract/governance foundation.

Product implementation: not authorized.

### Phase 1 - Discovery and Problem Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_1_DISCOVERY.yaml`

Purpose: define business problem, evidence requirements, source-of-truth boundaries, non-goals, and forbidden surface.

Product implementation: not authorized.

### Phase 2 - Solution Boundary Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_2_BOUNDARY.yaml`

Purpose: define allowed solution boundary, scope decisions, deferrals, and forbidden surface.

Product implementation: not authorized.

### Phase 3 - Architecture Readiness Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_3_READINESS.yaml`

Purpose: define evidence needed before architecture can be designed.

Product implementation: not authorized.

### Phase 4 - Minimal Architecture Authorization

Status: COMPLETED

Output: `sdd/artifacts/PHASE_4_ARCHITECTURE.yaml`

Purpose: authorize bounded/minimal architecture decisions and conceptual responsibility framing.

Product implementation: not authorized.

### Phase 5 - Bounded Implementation Planning Authorization

Status: COMPLETED

Outputs:

- `sdd/artifacts/PHASE_5_CONTRACT.yaml`
- `sdd/artifacts/PHASE_5_IMPLEMENTATION_PLAN.yaml`

Purpose: define governance-only implementation-planning authorization boundaries and readiness criteria without authorizing product build.

Product implementation: not authorized.

Product build: not authorized.

## Framework Closure Additions

After Phase 5, the following framework-level additions were made:

- `docs/sdd-plus/SDD_PLUS_LIFECYCLE.md`
- `docs/rakso/RAKSO_OS_OPERATING_MODEL.md`
- `docs/rakso/RAKSO_VELOCITY_MODE.md`
- `docs/rakso/REPOSITORY_BOUNDARY.md`
- `docs/phase-6b/DISCOVERY_TO_CONTRACT_BRIDGE.md`
- README role model examples

These additions clarify:

- RAKSO is tool-agnostic and capability-based.
- SDD+ is a rules engine, not a permanent production bottleneck.
- Velocity Mode limits planning loops.
- Vehicles must live outside the compiler repo.
- TaxPak is a vehicle, not the OS.

## Current Repository Boundary

This repository is for RAKSO OS / compiler framework only.

Vehicle-specific content is forbidden here.

Forbidden vehicle content includes:

- TaxPak discovery
- TaxPak product scope
- TaxPak MVP definition
- TaxPak build plans
- Bookkeeping AI discovery
- Any vehicle-specific implementation package

Vehicle work must happen in a separate vehicle repo or workspace.

Recommended first vehicle workspace:

```text
rakso-vehicle-taxpak
```

## Current Forbidden Surface

Unless a later committed SDD+ contract explicitly authorizes otherwise, this repo must not contain:

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
- product build authorization
- vehicle-specific discovery or product scope

## Known Gaps Not Blocking Vehicle Discovery

These remain open but do not block starting TaxPak in a separate vehicle workspace:

- `STATE_SNAPSHOT.yaml` needs a later refresh.
- CI enforcement is not implemented yet.
- Formal Phase 5 audit report is not committed yet.
- Standalone SDD+ repo synchronization is unresolved.

These are hardening tasks, not blockers for discovery-only vehicle processing.

## Next Action

Start TaxPak in a separate vehicle workspace or chat.

Recommended action:

```text
Open or continue TaxPak Discovery Investigation chat and create/use a separate TaxPak vehicle repo or workspace.
```

## Chat / Workspace Guidance

Use the existing TaxPak Discovery Investigation chat if it already contains discovery evidence and context.

Use a new chat only if the existing chat is too polluted or hard to navigate.

Do not continue TaxPak inside the RAKSO compiler chat except for framework-level decisions.

## Next Vehicle Rule

TaxPak must enter as vehicle input to RAKSO, not as part of RAKSO.

TaxPak discovery remains discovery-only until evidence answers the required pain questions.

No TaxPak product scope, MVP build, architecture, agents, workflows, integrations, schemas, code, or deployment should be created until the TaxPak vehicle repo has its own committed contract.

## Current Roadmap Interpretation

The compiler framework is ready enough to process the first vehicle.

The next workstream is not more compiler governance.

The next workstream is TaxPak discovery in a separate vehicle workspace.
