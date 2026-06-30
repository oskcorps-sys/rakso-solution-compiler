# SDD+ Lifecycle Roles

## Core Doctrine

SDD+ goes hand in hand with product and architecture creation.

SDD+ must not act as the gatekeeper for every production step after the product, architecture, scope, and guardrails are already contractually defined.

## Why SDD+ Exists

SDD+ exists to:

- Prevent LLM hallucination
- Prevent scope creep
- Force explicit contracts
- Separate allowed work from forbidden work
- Protect the repo from unauthorized changes
- Keep architecture and execution aligned with evidence and decisions

## Lifecycle Modes

### 1. Discovery Mode

SDD+ governs strongly.

Use when:

- The problem is unclear
- The product is not defined
- Evidence is incomplete
- Scope is not closed
- Architecture would be premature

In this mode, SDD+ may block product design, architecture, implementation, and automation.

### 2. Contract Mode

SDD+ closes the scope.

Use when:

- Discovery is strong enough
- The target problem is selected
- Product boundaries are being written
- Architecture is being defined
- Acceptance criteria are being created

In this mode, SDD+ defines:

- Allowed scope
- Forbidden scope
- Inputs
- Outputs
- Acceptance criteria
- Exit criteria
- Rollback rules
- Human approval gates

### 3. Build Mode

SDD+ stops asking for permission on every micro-step.

Once a committed SDD+ contract explicitly authorizes work, the executor may perform that work inside the contract.

In this mode:

- Codex executes the authorized work
- Jules may support tooling, docs, or scripts if authorized
- Antigravity may coordinate multi-agent execution only if authorized
- SDD Guard audits against the contract
- SDD+ blocks only real contract violations

Rule:

```text
If the committed contract authorizes the action, execute it.
If the action exceeds the contract, block it.
If authorization is unclear, stop and escalate.
```

### 4. Audit Mode

SDD+ verifies execution.

Use after implementation or artifact creation.

SDD+ checks:

- Did the work stay inside the contract?
- Were forbidden surfaces touched?
- Were acceptance criteria met?
- Did scope drift occur?
- Did the executor create hidden assumptions?

In this mode, SDD+ is an auditor, not a production bottleneck.

### 5. Maintenance Mode

SDD+ controls drift.

Use after a product or system is already operating.

SDD+ should govern:

- Change requests
- Regression risk
- Security boundaries
- Contract drift
- New scope approvals
- Incident rollback

SDD+ should not govern normal authorized operation step by step.

## Operating Principle

```text
SDD+ governs uncertainty.
Contracts govern execution.
Tests govern behavior.
Audits govern drift.
The human operator governs direction.
```

## Production Rule

After a product is created with contracts and guardrails:

- SDD+ remains present
- SDD+ does not disappear
- SDD+ becomes the constitutional layer
- SDD+ stops being the daily gatekeeper
- SDD Guard performs lightweight checks
- Executors proceed inside approved contracts

## Role Separation

| Layer | Role |
|---|---|
| SDD+ | Rules engine and constitutional boundary |
| SDD Guard | Lightweight automation and drift checker |
| Codex | Primary executor |
| Jules | Secondary executor for tooling/docs/scripts when authorized |
| Antigravity | Multi-agent orchestration when authorized |
| GitHub | Source control and verification |
| Human Operator | Final authority and direction |

## Anti-Bureaucracy Rule

No approved production task should require repeated approval if:

1. The SDD+ contract already authorizes it.
2. The executor stays inside allowed files and actions.
3. The acceptance criteria are clear.
4. A post-execution audit is available.

## Block Conditions

SDD+ or SDD Guard should block only when:

- The action is outside the committed contract
- The executor touches forbidden surfaces
- The executor invents scope
- The executor changes architecture without approval
- The executor creates unauthorized runtime, agents, workflows, schemas, integrations, scripts, tests, deployment, source code, or infrastructure
- The system cannot determine authorization

## Final Rule

SDD+ is not the boss of every keystroke.

SDD+ is the contract system that lets execution move fast without losing control.
