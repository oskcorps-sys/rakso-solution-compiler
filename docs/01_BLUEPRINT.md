# RAKSO Solution Compiler Blueprint

## Definition

RAKSO Solution Compiler is the framework layer of RAKSO OS.

It turns messy business reality into governed evidence, diagnosis, money logic, offer direction, SDD+ contracts, and controlled execution scopes when authorized.

This repository is not a vehicle repository.

It must remain reusable across vehicles such as TaxPak, Bookkeeping AI, Credit tools, and future verticals.

## Repository Boundary

`rakso-solution-compiler` contains the RAKSO framework only:

- RAKSO OS doctrine
- Operating model
- Velocity mode
- SDD+ lifecycle rules
- SDD Guard governance
- Generic discovery-to-contract bridge
- Generic compiler rules
- Generic decision and audit patterns

Vehicle-specific work must live outside this repository.

TaxPak discovery, TaxPak product scope, TaxPak MVP definition, customer evidence, and TaxPak implementation work must not be stored here.

Vehicle work belongs in a separate vehicle repository or workspace, such as:

```text
rakso-vehicle-taxpak
rakso-vehicle-bookkeeping
rakso-vehicle-credit
```

Names may change. The separation rule does not.

## Operating Model

RAKSO is repo-native, model-agnostic, tool-agnostic, and semi-automatic.

It is defined by capabilities, not vendor names:

- Command Brain
- Primary Executor
- Secondary Executor
- Orchestration Layer
- External Audit Layer
- Rules Engine
- Source of Truth
- Drift Guard
- Human Operator

Specific tools may fill these roles, but no tool is permanent. Vendor changes must not break RAKSO.

## Operating Governance

SDD+ is the rules engine and contract system for this repository.

SDD+ must govern uncertainty, close scope, define allowed and forbidden surfaces, and protect against hallucination and scope creep.

Once a committed contract authorizes work, SDD+ must stop acting as a step-by-step production gatekeeper and become the contract oracle and audit layer.

Core rule:

```text
SDD+ governs uncertainty.
Contracts govern execution.
Tests govern behavior.
Audits govern drift.
The human operator governs direction.
```

## Velocity Mode

Velocity Mode is active for the compiler framework.

Normal cycle:

```text
1. Decide target
2. Produce artifact or decision
3. Audit once and move on
```

Velocity Mode exists to prevent planning loops, repeated permission loops, and digital bureaucracy.

## Current SDD+ Phase Chain

Phase 0: Genesis / governance setup - COMPLETED

Phase 1: Discovery and problem definition - COMPLETED

Phase 2: Solution boundary definition - COMPLETED

Phase 3: Architecture readiness definition - COMPLETED

Phase 4: Minimal architecture authorization - COMPLETED

Phase 5: Bounded implementation planning authorization - COMPLETED

Phase 5 did not authorize product build, product implementation, executable schemas, modules, runtime integrations, workflows, prompts, tools, agents, deployment, APIs, data models, infrastructure, or source code.

## Current Framework Components

The compiler framework now includes:

- `README.md`
- `docs/00_DOCTRINE.md`
- `docs/01_BLUEPRINT.md`
- `docs/02_ROADMAP.md`
- `docs/03_CRITICAL_LENS.md`
- `docs/04_SDD_PLUS_INTEGRATION.md`
- `docs/rakso/RAKSO_OS_OPERATING_MODEL.md`
- `docs/rakso/RAKSO_VELOCITY_MODE.md`
- `docs/rakso/REPOSITORY_BOUNDARY.md`
- `docs/sdd-plus/SDD_PLUS_LIFECYCLE.md`
- `docs/sdd-guard/*`
- `docs/phase-6b/DISCOVERY_TO_CONTRACT_BRIDGE.md`
- `sdd/artifacts/*`

## Current System Shape

```text
RAKSO OS / Compiler Framework
  -> Operating Model
  -> Repository Boundary
  -> SDD+ Lifecycle
  -> Velocity Mode
  -> SDD Guard
  -> Generic Discovery-to-Contract Bridge
  -> Vehicle Repos / Workspaces
```

The compiler processes vehicles, but vehicles do not live inside the compiler repo.

## Current Forbidden Surface In This Repo

Unless explicitly authorized by a later committed SDD+ contract, this repo must not contain:

- vehicle-specific discovery
- vehicle-specific product scope
- vehicle-specific MVP definition
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

## Current Known Gaps

These gaps are known but do not block starting TaxPak discovery in a separate vehicle workspace:

- `STATE_SNAPSHOT.yaml` still needs a later state refresh.
- CI enforcement is not implemented yet.
- Formal Phase 5 audit report is not committed yet.
- Standalone SDD+ repo synchronization is unresolved.

These are framework hardening tasks, not blockers for vehicle discovery.

## Next System Action

Do not put TaxPak discovery in this repo.

Start TaxPak in a separate chat/workspace/repo using the compiler framework as the method source.

Recommended target:

```text
rakso-vehicle-taxpak
```

## Non-Negotiable Rule

RAKSO must survive independently from any vehicle.

If TaxPak disappears, RAKSO must still function.

If RAKSO needs TaxPak to make sense, the boundary has failed.
