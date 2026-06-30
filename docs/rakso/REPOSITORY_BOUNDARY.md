# RAKSO Repository Boundary

## Core Rule

RAKSO must survive independently from any single product, vehicle, vertical, client, or market experiment.

RAKSO is the operating system.
Vehicles are processed by the operating system.
Vehicles must not become part of the operating system's source of truth unless the content is generic framework doctrine.

## What This Repository Is

`rakso-solution-compiler` contains the framework layer:

- RAKSO OS doctrine
- Operating model
- Velocity mode
- SDD+ lifecycle rules
- SDD Guard governance
- Generic discovery-to-contract bridge
- Generic compiler rules
- Generic decision and audit patterns

This repository must remain reusable across vehicles.

## What This Repository Is Not

This repository is not the home for vehicle-specific discovery, product scope, build plans, customer research, MVP definition, or implementation details.

Vehicle-specific work must not live here.

Examples of vehicle-specific work:

- TaxPak discovery notes
- TaxPak product scope
- TaxPak MVP definition
- TaxPak build plans
- TaxPak customer evidence files
- Bookkeeping AI discovery notes
- Bookkeeping AI product scope
- Any vertical-specific implementation package

## Vehicle Repository Rule

Each vehicle should live in its own repository or project workspace.

Examples:

```text
rakso-solution-compiler        -> RAKSO OS / framework / compiler
rakso-vehicle-taxpak           -> TaxPak discovery, contracts, product work
rakso-vehicle-bookkeeping      -> Bookkeeping discovery, contracts, product work
rakso-vehicle-credit           -> Credit vehicle discovery, contracts, product work
```

Names may change. The separation rule does not.

## Allowed Cross-References

The RAKSO compiler may reference vehicles only as examples, not as source-of-truth content.

Allowed:

- Mentioning TaxPak as an example vehicle
- Explaining that vehicles are processed by RAKSO
- Defining generic bridge templates that a vehicle repo can use
- Defining generic contract format used by all vehicles

Forbidden:

- Storing TaxPak discovery inside the compiler repo
- Storing TaxPak product scope inside the compiler repo
- Storing TaxPak MVP or implementation plan inside the compiler repo
- Letting TaxPak requirements modify RAKSO OS doctrine directly
- Letting one vehicle define the architecture of RAKSO

## Generic Bridge Rule

Generic bridge files may live in the compiler repo only if they are vehicle-neutral.

A valid bridge describes:

```text
Raw discovery
  -> evidence
  -> pain map
  -> money logic
  -> offer direction
  -> contract draft
```

An invalid bridge contains vehicle-specific evidence, conclusions, scope, MVP, or build direction.

## Source of Truth Rule

RAKSO source of truth:

```text
RAKSO OS docs
SDD+ rules
compiler framework docs
generic templates
generic audit and guard rules
```

Vehicle source of truth:

```text
vehicle repo
vehicle discovery
vehicle contract
vehicle build scope
vehicle audit trail
```

## Import / Export Rule

RAKSO may export templates and processes to vehicle repos.

Vehicle repos may import the compiler's generic templates.

Vehicle repos may return findings back to RAKSO only when they reveal a generic improvement to the framework.

Vehicle-specific details stay in the vehicle repo.

## TaxPak Rule

TaxPak is the first validation and cashflow vehicle.

TaxPak is not RAKSO.
TaxPak does not define RAKSO.
TaxPak must not be stored inside the compiler repo as discovery or product scope.

TaxPak work must happen in a separate TaxPak vehicle repo or workspace.

## Final Boundary

RAKSO must remain product-agnostic.

If every vehicle disappears, RAKSO should still exist.

If RAKSO needs TaxPak to make sense, the boundary has failed.
