# Current SDD+ Roadmap Status

## Phase 0 - Genesis Setup

Status: COMPLETED

Output: SDD+ lifecycle initialized, state snapshot, initial contract/governance foundation.

Product implementation: not authorized.

## Phase 1 - Discovery and Problem Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_1_DISCOVERY.yaml`

Purpose: define business problem, evidence requirements, source-of-truth boundaries, non-goals, and forbidden surface.

Product implementation: not authorized.

## Phase 2 - Solution Boundary Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_2_BOUNDARY.yaml`

Purpose: define allowed solution boundary, scope decisions, deferrals, and forbidden surface.

Product implementation: not authorized.

## Phase 3 - Architecture Readiness Definition

Status: COMPLETED

Output: `sdd/artifacts/PHASE_3_READINESS.yaml`

Purpose: define evidence needed before architecture can be designed.

Product implementation: not authorized.

## Phase 4 - Minimal Architecture Authorization

Status: COMPLETED

Output: `sdd/artifacts/PHASE_4_ARCHITECTURE.yaml`

Purpose: authorize bounded/minimal architecture decisions and conceptual responsibility framing.

Product implementation: not authorized.

Implementation planning: not authorized.

Product build: not authorized.

## Next Likely Phase

Phase 5 - Implementation Planning Authorization

Status: FUTURE / NOT STARTED

Purpose: may authorize implementation planning only if a committed Phase 5 contract allows it.

This phase must not assume product build is authorized.

## Future Build Phase

Phase 6 or later - Product Build Authorization

Status: FUTURE / NOT STARTED

Product code only begins if explicitly authorized by a committed SDD+ contract.

## Hard Rules Learned

- No hardcoded lifecycle-state wording in contracts.
- `STATE_SNAPSHOT.yaml` is the lifecycle source of truth.
- Contract acceptance tests should reference the active SDD+ gate instead of hardcoding lifecycle states.
- External blind audits are required before completion.
- Self-approval is not allowed.
- No implementation planning without committed contract authorization.
- No build without committed contract authorization.

## Current Forbidden Surface

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

## Current Artifact Chain

```txt
sdd/artifacts/STATE_SNAPSHOT.yaml
sdd/artifacts/PHASE_1_DISCOVERY.yaml
sdd/artifacts/PHASE_2_BOUNDARY.yaml
sdd/artifacts/PHASE_3_READINESS.yaml
sdd/artifacts/PHASE_4_ARCHITECTURE.yaml
```

## Current Roadmap Interpretation

Phases 0 through 4 are completed. The repository is governed by SDD+ and has reached bounded/minimal architecture authorization only.

The next phase may consider implementation planning authorization, but only through a new committed SDD+ contract. Product build remains unauthorized until a later committed contract explicitly permits it.
