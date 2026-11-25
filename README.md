# AIROI Framework

**An open methodology for evidence-based AI advisory engagements** — structured discovery, ambition calibration, capability assessment, and decision reports with a defensible return.

> Status: **draft specification**. The framework is being extracted and generalized from the authors' consulting practice. See [BLUEPRINT.md](BLUEPRINT.md) for the founding document (Slovak; the English core specification follows per the authoring roadmap).

## Why AIROI?

**AI + ROI.** The framework exists to answer the question most AI assessments dodge: *where does AI actually return value for this organization — and how much change can it absorb to get there?* Most AI assessments fail not because the scoring is wrong, but because the recommendation ignores the organization's real ambition, capacity, and economics.

## The AI Value System

At the top of the framework sits the **AI Value System (AVS)**: signals and demand flow in, a **realized return** flows out. Inside: guiding principles, governance, five disciplines, and the **AI Value Chain** — seven activities that form a loop:

```
Sense → Align → Assess → Shape → Decide → Realize → Recalibrate ↺
```

Two ideas make the methodology bite:

- **The chain doesn't close at the report — it closes at the realized return.** *Realize* belongs to the client; the framework prepares it (decisions with owners, Acceptance Cards with measured baselines and kill criteria, an AI Register) and measures it (*Recalibrate*).
- **Return = Potential × Fit**, judged per opportunity — where Fit is how well the opportunity matches the organization's Ambition Vector times the capacity to absorb *that* change. The vector is a distribution, never a multiplier. High potential without fit is shelfware; fit without potential is busywork. That's why ambition calibration always precedes opportunity discovery — and why a maturity **score is an output, never the outcome**.

Every discipline looks at the organization through **four dimensions**: People & Judgment · Evidence & Data · Processes & Value Streams · Technology & Partners.

## What is this?

AIROI packages a field-tested AI advisory methodology into a named, versioned, open framework — structured like the major practice frameworks, but open (CC-BY-SA) and focused on one job: **turning scattered AI experiments into a defensible investment path.**

Five disciplines:

- **D1 · Evidence & Hypotheses** — pre-engagement research from public sources; every claim carries an evidence grade (`A/B/C/X`) and must be falsifiable
- **D2 · Ambition Calibration** — the Ambition Vector (**Sustain / Scale / Shift**, 100 points) with sector baselines, evidence-tier weighting (capital allocation > strategic behavior > language), and realism rules
- **D3 · Capability Assessment** — organizational AI capacity via the original **AIROI Capacity Model** (7 domains, 22 sub-capacities — including Agency & Control for AI that acts — grounded in the public-domain [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework)) plus process-level deep-dives grounded in the [APQC Process Classification Framework](https://www.apqc.org/process-frameworks) (referenced as the external original, not repackaged)
- **D4 · Opportunity Discovery** — AI opportunities traced to specific pain in specific process steps with specific owners, each classified by stakes, **action level** (inform → draft → act with approval → act within bounds), and oversight
- **D5 · Decision Enablement** — red-flag consistency verification, advisor ∥ AI co-analyst parallel drafting, gradient-structured decision reports

## Where value leaks — and how the system seals it

Between an organization's AI ambition and a realized return, value leaks at four points: **potential–fit mismatch** (recommendations the organization can't absorb), **value without an owner** (advice detached from processes), **overestimated fit** (unverified self-assessment), and **the chain ending at the report** (nobody measures realization). The framework is built as a sealing system for exactly these four leaks.

## Guiding principles (preview)

1. **Focus on return** — every activity must trace to a realized return; scores, documents, and meetings are costs, not value
2. **Evidence over opinion** — capital allocation beats strategic behavior beats language
3. **Hypotheses, not summaries** — every claim carries an evidence grade and must be falsifiable
4. **Realism before ambition** — fit is the most expensive variable to get wrong; calibrate it first
5. **Un-bias by design** — respondents see clean forms; prefills exist only on the advisor's side
6. **Psychological safety** — the truth about capacity is a Return Equation input; defensiveness distorts it
7. **Advisor in the loop** — the AI co-analyst drafts mechanical parts in parallel; judgment stays human

## Repository layout

| Path | Content |
|---|---|
| [BLUEPRINT.md](BLUEPRINT.md) | Founding document: framework anatomy, sources policy, authoring roadmap |
| [spec/00-ai-value-system.md](spec/00-ai-value-system.md) | **Spec 00 — The AI Value System** — the root document: value leaks, value chain, Return Equation, dimensions, Recalibration Loop |
| [spec/01-principles.md](spec/01-principles.md) | **Spec 01 — Guiding Principles** — seven ordered decision rules with rationale and anti-patterns |
| [spec/02-lifecycle.md](spec/02-lifecycle.md) | **Spec 02 — Lifecycle** — stages, actors, quality gates, feedback loops, refusal conditions |
| [spec/03-disciplines/](spec/03-disciplines/) | **Spec 03 — Disciplines D1–D5** — Evidence & Hypotheses · Ambition Calibration · Capability Assessment · Opportunity Discovery · Decision Enablement |
| [spec/04-data-standard.md](spec/04-data-standard.md) | **Spec 04 — Data Standard** — JSON envelope, field types, Evidence Grades, rationale contract, margin notes, un-bias enforcement |
| [spec/05-red-flag-catalog.md](spec/05-red-flag-catalog.md) | **Spec 05 — Red-Flag Catalog** — 57 declarative cross-check rules (RF-01…RF-57) |
| [spec/06-artifacts.md](spec/06-artifacts.md) | **Spec 06 — Artifacts** — artifact register, definitions, quality criteria, minimum sets per tier |
| [spec/07-adoption.md](spec/07-adoption.md) | **Spec 07 — Adoption** — tiers as return-confidence, client commitments, conformance rules |
| [spec/08-glossary.md](spec/08-glossary.md) | **Spec 08 — Glossary** — canonical definitions |
| [ATTRIBUTIONS.md](ATTRIBUTIONS.md) | Licensing map for adapted and referenced external works |
| [LICENSE.md](LICENSE.md) | CC-BY-SA 4.0 |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [spec/03-disciplines/ACM-capacity-model.md](spec/03-disciplines/ACM-capacity-model.md) | **The AIROI Capacity Model (ACM)** — original 7-domain organizational AI capacity model with 66 level statements and a NIST AI RMF crosswalk |
| [reference-implementations/ambition-calibration.html](reference-implementations/ambition-calibration.html) | **Ambition Calibration instrument** (D2) — linked-slider Ambition Vector, advisor/respondent modes, envelope import/export, red flags with RF-IDs |
| [reference-implementations/capacity-assessment.html](reference-implementations/capacity-assessment.html) | **Capacity Assessment instrument** (D3/ACM) — statement-pick capacity cards across 7 domains, honest L0/N-A/skip scoring, red flags RF-10…RF-20, RF-43, RF-53 |
| `reference-implementations/` | *(coming)* Process deep-dive instrument |
| `translations/` | *(coming)* Slovak and other language derivatives |

## License

[CC-BY-SA 4.0](LICENSE.md). Free for commercial use with attribution; derivatives must carry the same license.
