# RAKSO Velocity Mode

## Purpose

Velocity Mode exists to prevent RAKSO from dying in planning loops, permission loops, and digital bureaucracy.

RAKSO must produce useful artifacts and decisions faster than the friction it creates.

## Core Rule

Every work cycle must produce at least one of:

- A committed artifact
- A closed decision
- A verified audit result
- A clear stop reason

If a cycle produces none of these, the cycle failed.

## Maximum Cycle Length

A normal cycle has only three moves:

```text
1. Decide the target
2. Produce the artifact or decision
3. Audit once and move on
```

## Anti-Bureaucracy Limits

Velocity Mode limits:

- Max 1 primary artifact per cycle
- Max 1 governance scan per artifact
- Max 1 follow-up patch unless a real contradiction exists
- No repeated approval loops when a committed contract already authorizes the action
- No governance-only chains longer than one cycle unless explicitly justified
- No TaxPak work before RAKSO framework work is closed
- No product build unless explicitly authorized by contract

## SDD+ Interaction

SDD+ is not removed.

SDD+ changes intensity based on lifecycle mode:

- Heavy in Discovery Mode
- Strong in Contract Mode
- Verifying in Build Mode
- Auditing in Audit Mode
- Drift-checking in Maintenance Mode

Velocity Mode follows this rule:

```text
If the committed contract authorizes the action, execute it.
If the action exceeds the contract, block it.
If authorization is unclear, stop and escalate.
```

## SDD Guard Interaction

SDD Guard should be lightweight.

It should check:

- current state
- allowed files
- forbidden drift
- next action

It should not become a second bureaucracy layer.

## Allowed Fast Path

When a task is governance/docs-only and already authorized, the fast path is:

```text
create artifact
verify delta
report next action
```

No repeated permission packet is required.

## Build Fast Path

When a future product/build task is explicitly authorized by contract, the fast path becomes:

```text
execute authorized task
run required checks
audit against contract
commit result
```

No repeated permission loop is allowed if the executor stays inside the contract.

## Human Operator Authority

OZ can interrupt Velocity Mode at any time.

OZ can:

- approve
- deny
- redirect
- pause
- force execution
- request audit
- request rollback

The system must obey direction without adding unnecessary ceremony.

## Stop Conditions

Stop only when:

- the action is outside authorized scope
- authorization is unclear
- a forbidden surface would be touched
- source truth is missing
- the requested action contradicts current contract
- the task requires a decision only OZ can make

## What Velocity Mode Kills

Velocity Mode kills:

- endless planning
- repeated gatekeeping
- extra scans without findings
- permission loops
- document chains with no artifact value
- premature product jumps
- pretending strategy equals execution

## What Velocity Mode Protects

Velocity Mode protects:

- speed
- focus
- source of truth
- contract boundaries
- human authority
- actual output

## Session Rule

At the end of each session, report only:

```text
What changed
Latest commit
Current state
Next action
Blocked items
```

No long courtroom brief unless requested.

## Current Use

Velocity Mode is active for closing the RAKSO compiler framework.

Next after framework closure:

```text
Begin TaxPak Discovery processing through the compiler bridge.
```
