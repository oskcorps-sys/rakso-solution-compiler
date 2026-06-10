# RAKSO Solution Compiler Blueprint v1

## Definition

RAKSO Solution Compiler is an internal system that converts raw business input into a sellable, scoped, validated, and executable solution package.

## System layers

```txt
RAKSO Solution Compiler
|
├── 1. Input Router
├── 2. Evidence Ledger
├── 3. Business Reality Diagnosis
├── 4. Pain-to-Profit Branch
├── 5. Offer Architecture Branch
├── 6. Solution Type Decision
├── 7. SDD+ Contract Builder
├── 8. SpellWriter / Artifact Compiler
├── 9. Execution Agent Profiles
├── 10. Deployment Package
└── 11. Market Expansion Loop
```

## Layer 1: Input Router

Accepts multiple types of business input.

Routes:

- Client transcript: Zoom, Teams, Google Meet, Fathom, Fireflies, manual notes
- Small business reality scanner: no website, WhatsApp-first, paper, Excel, memory, no CRM, no SOP
- Digital lead research: website, Google Business Profile, LinkedIn, reviews, directories, social media
- Screenshot / WhatsApp evidence: screenshots, process photos, document images, scattered notes
- Existing system audit: SOPs, spreadsheets, CRM, existing workflows, software stack

Rule:

```txt
If there is a website, research it.
If there is no website, interview.
If there is no structure, reconstruct.
If there is only chaos, organize.
```

## Layer 2: Evidence Ledger

Separates facts, assumptions, and unknowns.

Evidence levels:

- `client_stated`
- `transcript_confirmed`
- `document_confirmed`
- `public_verified`
- `sector_inferred`
- `assumption`
- `unknown`

Rule:

```txt
Do not mix evidence with hypothesis.
```

## Layer 3: Business Reality Diagnosis

Reconstructs how the business actually works.

Must identify:

- what the business sells
- how customers arrive
- how work enters the business
- who does what
- tools used
- bottlenecks
- repeated tasks
- forgotten tasks
- lost information
- owner dependency
- human approval points

Universal small business areas:

1. Lead / Customer Intake
2. Scheduling / Appointments
3. Job / Case Tracking
4. Documents / Photos / Notes
5. Payments / Invoices
6. Follow-up / Reviews / Retention

## Layer 4: Pain-to-Profit Branch

Converts operational pain into economic impact.

Outputs:

- pain
- who feels it
- frequency
- time lost per event
- monthly volume
- revenue leakage
- estimated monthly cost
- estimated annual cost
- urgency
- confidence
- missing data

Rule:

```txt
If the pain has no money, there is no project yet.
```

## Layer 5: Offer Architecture Branch

Packages the solution as something sellable.

Outputs:

- offer diagnosis
- value proposition
- offer name
- simple explanation
- offer stack
- pricing hypothesis
- micro-ad
- outreach angle
- sales brief
- risk reversal
- scope boundary

Rule:

```txt
Offer architecture does not invent pain. It packages validated pain or clearly marked hypotheses.
```

## Layer 6: Solution Type Decision

Chooses the simplest solution that captures value.

Options:

0. No project
1. SOP / checklist
2. Template pack
3. Form + spreadsheet
4. CRM-lite setup
5. Automation workflow
6. AI-assisted workflow
7. Agentic workflow
8. Custom app

Rule:

```txt
The simplest solution that captures value wins.
```

## Layer 7: SDD+ Contract Builder

Formalizes the solution into a closed contract.

Outputs:

- project name
- client context
- problem statement
- evidence sources
- business case
- offer reference
- actors
- inputs
- outputs
- constraints
- success criteria
- test cases
- forbidden actions
- human approval points
- out of scope
- deployment target
- acceptance criteria

## Layer 8: SpellWriter / Artifact Compiler

Converts the SDD+ contract into executable artifacts.

Targets:

- Claude
- Codex
- Antigravity
- OpenAI API
- n8n
- Make/Zapier
- Ollama
- custom app
- Hermes/ModelRack

## Layer 9: Execution Agent Profiles

Defines who executes what.

Technical profiles:

- Researcher Agent
- Coder Agent
- DevOps Agent

Business profiles:

- Discovery Analyst
- Business Case Analyst
- Offer Architect
- SDD+ Contract Builder
- Critical Lens

## Layer 10: Deployment Package

Produces a complete implementation folder.

Example:

```txt
/client-name/
├── 01_evidence_report.md
├── 02_operational_diagnosis.md
├── 03_pain_to_profit.yaml
├── 04_offer_brief.md
├── 05_micro_ad.md
├── 06_solution_options.md
├── 07_sdd_contract.yaml
├── 08_implementation_brief.md
├── 09_agent_profiles/
└── 10_deployment_package/
```

## Layer 11: Market Expansion Loop

Uses validated pain patterns to find similar leads.

Flow:

```txt
Validated Pain -> Pain Pattern Library -> Similar Business Finder -> Lead Research -> Outreach Angle -> Discovery Call -> New Client Input
```

Rule:

```txt
Lead research generates hypotheses, not truths.
```
