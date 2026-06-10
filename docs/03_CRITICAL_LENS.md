# Critical Lens

Critical Lens is the transversal audit layer of RAKSO Solution Compiler.

Its job is to prevent hype, weak evidence, overengineering, vendor lock-in, scope creep, and commercially dead solutions.

## Activation points

Critical Lens must be applied:

1. after Evidence Ledger
2. after Business Reality Diagnosis
3. after Pain-to-Profit
4. after Offer Architecture
5. after SDD+ Contract
6. after Artifact Compiler
7. before Deployment Package

## Mandatory questions

### Evidence check

- What evidence supports this?
- Is this confirmed, inferred, assumed, or unknown?
- What source proves it?
- What data is missing?

### Business check

- Who feels the pain?
- How often does it happen?
- What does it cost in time, money, risk, or lost capacity?
- Is there enough economic impact to justify a paid solution?
- Is the buyer likely able and willing to pay?

### Simplicity check

- What is the simplest solution that captures value?
- Does this need AI?
- Does this need agents?
- Does this need a custom app?
- Could a form, checklist, spreadsheet, or reminder workflow solve the first version?

### Scope check

- What is included?
- What is explicitly out of scope?
- What could create scope creep?
- What requires human approval?
- What must never be automated?

### Technical check

- What can fail?
- What is the blast radius?
- What runtime or vendor is this locked to?
- What are the rollback paths?
- Are secrets, client data, or production systems involved?

### Offer check

- Can the offer be explained in 15 seconds?
- Is the value proposition specific?
- Is pricing connected to economic pain?
- Is the micro-ad grounded in the real pain?
- Is the offer selling relief, not technology?

## Stop conditions

Critical Lens must block progression when:

- evidence is mostly assumptions
- pain has no clear economic impact
- solution type is overbuilt for the problem
- scope boundaries are missing
- success criteria are vague
- human approval points are undefined
- deployment target is vendor-locked without reason
- generated artifacts cannot be executed or tested

## Output format

```yaml
critical_lens_review:
  verdict: pass | needs_revision | blocked
  reason:
  evidence_risks:
  business_risks:
  technical_risks:
  scope_risks:
  recommended_fix:
  next_action:
```
