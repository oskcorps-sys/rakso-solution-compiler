# Critical Lens

Critical Lens is the transversal audit layer of RAKSO Solution Compiler.

Its job is to prevent hype, weak evidence, overengineering, vendor lock-in, scope creep, commercially dead solutions, and repository-boundary violations.

## Activation Points

Critical Lens must be applied after each major framework or vehicle artifact, including:

1. Evidence Ledger
2. Business Reality Diagnosis
3. Pain-to-Profit Map
4. Offer Direction
5. SDD+ Contract
6. Authorized execution scope when a later contract permits it
7. Audit report
8. Vehicle handoff or import/export boundary

Future artifact compiler, deployment package, agent, workflow, schema, runtime, or product-build reviews apply only if a later committed SDD+ contract explicitly authorizes those surfaces.

## Mandatory Questions

### Evidence Check

- What evidence supports this?
- Is this confirmed, inferred, assumed, or unknown?
- What source proves it?
- What data is missing?
- Is any vehicle-specific evidence being stored in the compiler repo by mistake?

### Business Check

- Who feels the pain?
- How often does it happen?
- What does it cost in time, money, risk, or lost capacity?
- Is there enough economic impact to justify a paid solution?
- Is the buyer likely able and willing to pay?

### Simplicity Check

- What is the simplest solution that captures value?
- Does this need AI?
- Does this need agents?
- Does this need a custom app?
- Could a form, checklist, spreadsheet, or reminder workflow solve the first version?

### Scope Check

- What is included?
- What is explicitly out of scope?
- What could create scope creep?
- What requires human approval?
- What must never be automated?
- Is this framework-generic or vehicle-specific?
- Does this belong in the compiler repo or in a vehicle repo?

### Technical Check

- What can fail?
- What is the blast radius?
- What vendor, runtime, tool, model, or repo host is this locked to?
- What are the rollback paths?
- Are secrets, client data, or production systems involved?
- Is any product, runtime, schema, workflow, agent, integration, code, script, test, or deployment being implied without authorization?

### Offer Check

- Can the offer be explained in 15 seconds?
- Is the value proposition specific?
- Is pricing connected to economic pain?
- Is the micro-ad grounded in the real pain?
- Is the offer selling relief, not technology?

### Velocity Check

- Did this cycle produce a useful artifact, closed decision, audit result, or clear stop reason?
- Are we adding ceremony without reducing risk?
- Is SDD+ governing uncertainty or blocking already-authorized execution?
- Is another scan needed, or are we looping?

## Stop Conditions

Critical Lens must block progression when:

- evidence is mostly assumptions
- pain has no clear economic impact
- solution type is overbuilt for the problem
- scope boundaries are missing
- success criteria are vague
- human approval points are undefined
- vendor lock-in exists without reason
- generated artifacts cannot be executed or tested when execution is actually authorized
- vehicle-specific material is being placed inside the compiler repo
- product/build/runtime/code surfaces are being implied without a committed contract
- the process is creating bureaucracy without reducing risk

## Output Format

```yaml
critical_lens_review:
  verdict: pass | needs_revision | blocked
  reason:
  evidence_risks:
  business_risks:
  technical_risks:
  scope_risks:
  velocity_risks:
  repository_boundary_risks:
  recommended_fix:
  next_action:
```
