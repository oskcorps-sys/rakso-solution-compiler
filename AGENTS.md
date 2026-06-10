# AGENTS.md

## Repository mission

This repository defines and builds RAKSO Solution Compiler: an internal system for converting business chaos into sellable, executable solutions.

## Core formula

```txt
Reality -> Evidence -> Diagnosis -> Money -> Offer -> Contract -> Execution
```

## Operating rules for agents

1. Do not start with technology.
2. Do not invent business pain.
3. Do not mix evidence with assumptions.
4. Do not recommend AI, agents, or custom apps when a simpler solution captures value.
5. Do not create implementation artifacts before an SDD+ contract exists.
6. Do not remove Critical Lens checkpoints.
7. Do not make the system Claude-only, Codex-only, Antigravity-only, or Hermes-only.
8. Prefer small, testable artifacts over broad documents without schemas.

## Required response behavior for repo tasks

When modifying this repo:

1. State what layer is affected.
2. State whether the change is doctrine, schema, module, profile, example, or implementation.
3. Preserve the core formula.
4. Add or update tests/golden outputs when changing schemas.
5. Flag assumptions explicitly.

## Architecture boundaries

### Business layer

- Input Router
- Evidence Ledger
- Business Reality Diagnosis
- Pain-to-Profit
- Offer Architecture
- Solution Type Decision
- SDD+ Contract Builder

### Compiler layer

- SpellWriter / Artifact Compiler
- Agent Profile Compiler
- Deployment Package Builder

### Execution layer

- Researcher Agent
- Coder Agent
- DevOps Agent
- Critical Lens

## Forbidden shortcuts

- Transcript -> solution without evidence ledger
- Pain -> app backlog without pain-to-profit
- Offer -> implementation without SDD+ contract
- Lead research -> truth claims without validation
- Agent execution -> production writes without approval policy

## MVP rule

Manual and clear first. Automation later.
