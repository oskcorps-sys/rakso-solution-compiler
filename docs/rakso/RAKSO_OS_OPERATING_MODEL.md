# RAKSO OS Operating Model

## Definition

RAKSO is a repo-native, model-agnostic, tool-agnostic, semi-automatic operating system operated by a human decision-maker to turn business chaos into evidence, decisions, contracts, offers, and controlled execution.

RAKSO is not a single AI model.
RAKSO is not a single coding tool.
RAKSO is not a single orchestration platform.
RAKSO is not a SaaS yet.
RAKSO is not TaxPak.
RAKSO is not a vendor-specific stack.

RAKSO is the operating system that coordinates roles, tools, contracts, evidence, decisions, execution, and audit.

## Where RAKSO Lives

The source of truth lives in:

```text
GitHub repo or equivalent versioned repository
versioned docs
contracts
state files
decision logs
audit trails
commits
```

A chat interface is a command surface, not the source of truth.

If any specific AI provider, coding assistant, orchestrator, or audit tool disappears, RAKSO must remain recoverable from the repo and transferable to equivalent tools.

## Capability Stack

RAKSO is defined by capabilities, not vendor names.

| Capability | Required Role |
|---|---|
| Command Brain | Strategy, synthesis, blindspots, adversarial thinking, decision framing |
| Primary Executor | Authorized repo work, implementation tasks, edits, commits, refactors when allowed |
| Secondary Executor | Supporting docs, tooling, scripts, cleanup, auxiliary implementation when allowed |
| Orchestration Layer | Multi-agent or multi-worker coordination when authorized |
| External Audit Layer | Independent review, research validation, red-team logic, second opinion |
| Rules Engine | SDD+ contracts, allowed scope, forbidden scope, acceptance criteria, lifecycle rules |
| Source of Truth | Version control, committed artifacts, audit trail, state recovery |
| Drift Guard | Lightweight state checks, stale wording checks, forbidden-surface checks, next-action checks |
| Human Operator | Final authority, priority, direction, approval, denial, override, stop |

## OZ Default Mapping

The following is OZ's current preferred mapping. It is not part of the permanent RAKSO dependency model.

| Capability | OZ Current Tool Choice |
|---|---|
| Command Brain | ChatGPT |
| Primary Executor | Codex |
| Secondary Executor | Jules |
| Orchestration Layer | Antigravity |
| External Audit Layer | Gemini, DeepSeek, Claude / Sonnet when useful |
| Rules Engine | SDD+ |
| Source of Truth | GitHub |
| Drift Guard | SDD Guard |
| Human Operator | OZ |

This mapping may change without changing RAKSO itself.

If Codex merges into another OpenAI interface, the Primary Executor role remains.
If Gemini disappears, another audit engine can fill the External Audit role.
If Antigravity becomes unavailable or too expensive, another orchestration layer can replace it.
If GitHub is replaced, the Source of Truth role must move to an equivalent versioned repository.

## Operating Principle

```text
The Command Brain frames.
The Human Operator decides.
The Rules Engine bounds.
The Primary Executor executes authorized work.
The Secondary Executor supports authorized work.
The Orchestration Layer coordinates only when authorized.
The External Audit Layer reviews when needed.
The Source of Truth stores the state.
The Drift Guard checks boundaries.
```

## What RAKSO Does

RAKSO turns raw business inputs into:

- Evidence summaries
- Pain maps
- Money logic
- Offer direction
- SDD+ contracts
- Execution scopes
- Audit reports
- Controlled build tasks when authorized

## What RAKSO Does Not Do By Default

RAKSO does not automatically:

- Build products
- Deploy systems
- Create agents
- Create workflows
- Create integrations
- Create schemas
- Modify source code
- Run tests
- Configure infrastructure
- Override the human operator
- Treat one tool as permanent truth

Those actions require an explicit committed contract.

## Vehicle Layer

Vehicles are business opportunities processed by RAKSO.

Examples:

- TaxPak
- Bookkeeping AI
- Credit tools
- Future verticals

Vehicles do not define RAKSO.

RAKSO processes vehicles.

TaxPak is the first validation and cashflow vehicle, not the operating system.

## Execution Flow

```text
Input
  -> Evidence
  -> Diagnosis
  -> Decision
  -> SDD+ Contract
  -> Authorized Execution
  -> Audit
  -> Next Action
```

## Authority Flow

1. The Human Operator sets direction.
2. The Command Brain frames strategy and blindspots.
3. The Rules Engine checks uncertainty and contract boundaries.
4. Executors execute only authorized work.
5. The Source of Truth records all artifacts and commits.
6. The Drift Guard audits drift and next action.
7. External auditors review when needed.

## Vendor Independence Rule

RAKSO must remain usable if any single provider disappears.

If the current command brain is unavailable, another model or a human operator must be able to continue from:

- repo state
- operating model
- contracts
- task files
- logs
- commits

## Interface Path

RAKSO may be used through:

1. Chat interface now
2. Repo workflow now
3. CLI later if needed
4. Private dashboard later if internal usage proves stable
5. SaaS only after internal OS value is proven

No interface is permanent.

The interface can change without changing the OS.

## Current Position

RAKSO is currently a private repo-native OS under construction.

It is not ready to become a SaaS.
It is not ready to be driven by TaxPak.
It must first prove that it can reduce internal decision and execution friction.

## Next Required Companion

RAKSO requires Velocity Mode to prevent planning loops and digital bureaucracy.
