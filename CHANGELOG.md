# Changelog

All notable changes to the AIROI Framework blueprint and specification.

## v0.11 — Tiers renamed: Pulse / Case / Launch

- Adoption tiers renamed to speak the value language — each tier is
  named for what the client buys: **Pulse** (a directional pulse check
  of return potential), **Case** (the full, defensible return case with
  a roadmap), **Launch** (the case plus realization readiness: business
  cases, architecture, backlog, 90-day plan). Blueprint open item 2
  resolved.

## v0.10 — AIROI confirmed as the definitive name

- "Working name" caveats removed across the blueprint, all specification
  documents, the proposal, and the repository description. Blueprint
  open item 1 resolved.

## v0.9 — EP-01 Value Engineering Extension Pack implemented

All four extensions from proposals/EP-01 are now part of the
specification:

- **E1 Stakes & Oversight** — Stakes Ladder (S0–S3) and Oversight Modes
  (O1–O4) as mandatory shortlist attributes with a proportionality rule
  enforced as a Decide gate; new **AI Register** handover artifact
  carrying the sunset discipline (review date + retirement criterion
  per entry). (D4 §3, D5, Spec 04 §9, Spec 06 §2.11)
- **E2 Acceptance Cards** — "no measurement, no approval": per approved
  opportunity a card with outcome metric, measured baseline, ranged
  target, eval method, quality bar, kill criteria, and review interval;
  Recalibrate now reads the cards and audits the register. Resolves the
  blueprint's return-measurement open item. (D5, Spec 02, Spec 06 §2.10)
- **E3 Adaptation Ladder** — implementation postures A0–A5 with ACM
  prerequisites and lock-in profiles replace the four-option decision
  tree; climb-on-evidence rule; unit-economics sizing (cost per
  outcome, quality-cost-latency triangle, cascade pattern) and
  value-class portfolio mix. (D4 §5, D5, Spec 04 §9)
- **E4 Flow & Absorption** — Delivery Flow States (F1–F4) from
  observable flow signals as D3's third lens; flow traces added to D1
  research; Absorption Rules (WIP limit, underwater rule, stakes–flow
  rule) validate the roadmap as a Decide gate; culture-texture probe.
  (D1, D3, D5, Spec 04 §9)
- **Red-Flag Catalog v2**: 12 new Decide-stage rules RF-31…RF-42
  (catalog now 42 rules). Lifecycle exit criteria and quality gates
  extended; adoption invariant now includes Acceptance Cards; glossary
  +16 terms.

## v0.8 — The AIROI Capacity Model (resolves blueprint open item 3)

- **AIROI Capacity Model (ACM)** — an original organizational AI capacity
  model replacing the previously adapted third-party maturity assessment.
  6 domains (Direction & Accountability · People & Adoption · Data
  Readiness · Delivery & Integration · Trust & Control · Operations &
  Learning) × 3 sub-capacities = 18 measurements, each with three
  original level statements (L1 Emerging / L2 Established / L3 Embedded)
  plus the uniform L0 / N/A semantics. Grounded in the public-domain
  NIST AI RMF via a function and trustworthiness-characteristics
  crosswalk. Spec: `spec/03-disciplines/ACM-capacity-model.md`.
- **Capacity Assessment instrument**
  (`reference-implementations/capacity-assessment.html`) — statement-pick
  capacity cards, honest per-domain scoring with L0/N-A/skip annotations,
  red flags RF-10…RF-20 with catalog IDs, Spec 04 envelope
  import/export, advisor/respondent modes, bilingual EN/SK. The spec
  document and the instrument are generated from a single model
  definition, so statements cannot drift apart.
- **Licensing consequence:** the framework now contains no adapted
  third-party content. Its CC-BY-SA license is a choice, no longer an
  obligation inherited from adaptation. ATTRIBUTIONS restructured
  (adapted-works section removed; NIST promoted to grounding framework);
  D3 lens 1 rewritten; README and Blueprint updated.

## v0.7 — First reference implementation

- **Ambition Calibration instrument** (`reference-implementations/
  ambition-calibration.html`) — a self-contained bilingual (EN default,
  SK toggle) single-page instrument for the Alignment Session,
  implementing Spec 03/D2 and conforming to Spec 04 and Spec 05:
  - linked-slider Ambition Vector (Sustain / Scale / Shift, sum-100
    embodied in the UI)
  - advisor / respondent dual rendering (Spec 04 §6): evidence-grade
    chips, editable rationale callouts, and per-section margin notes
    exist only in advisor mode
  - Hypothesis Pack envelope import and full envelope export (Spec 04
    §1–§2), plus Markdown export and clipboard copy
  - vector computation with posture/momentum signal adjustments and
    Realism Rules; red flags cite catalog IDs RF-01…RF-09 (Spec 05)
  - built fresh (new layout: sticky section rail + scrolling page; new
    palette) rather than ported, per the sources policy
- Verified: JS syntax check clean; structure counts (10 sections,
  9 margin notes) as designed

## v0.6 — Full specification draft

Complete draft of the remaining specification (all in English):

- **Spec 01 — Guiding Principles**: seven ordered decision rules (Focus on
  return · Evidence over opinion · Hypotheses not summaries · Realism
  before ambition · Un-bias by design · Psychological safety · Advisor in
  the loop), each with rationale, practice guidance, and anti-patterns;
  conflict-resolution rule (lower number wins)
- **Spec 02 — Lifecycle**: four actors in three lanes, stage map with
  chain mapping and return contributions, full stage definitions with
  exit criteria, feedback discipline, 11 quality gates, refusal and stop
  conditions
- **Spec 03 — Disciplines D1–D5** (one document each): purpose, core
  question, method, outputs, rules, anti-patterns, Return Equation
  contribution. D2 carries sector baselines for the Ambition Vector and
  Realism Rules; D3 carries both capability lenses (organizational
  maturity adapted from OWASP AIMA, and the process deep-dive incl. AI
  archetypes); D4 defines the opportunity-pool entry format; D5 the
  implementation decision tree with "No AI" as a first-class option
- **Spec 04 — Data Standard**: JSON envelope, five field types incl. the
  Ambition Vector invariants, Evidence Grades, the rationale contract,
  margin notes with canonical facilitation markers, mechanical un-bias
  enforcement (advisor/respondent render modes), validation rules,
  schema versioning
- **Spec 05 — Red-Flag Catalog**: rule format + initial catalog of 30
  rules (RF-01…RF-30) across ambition consistency, capability
  consistency, and pain–motivation alignment; catalog governance via the
  Recalibration Loop
- **Spec 06 — Artifacts**: register, full definitions with quality
  criteria, Decision Report gradient structure, minimum artifact sets
  per tier
- **Spec 07 — Adoption**: tiers as return-confidence levels, client
  commitments, per-tier quality-gate deltas, conformance rules for
  adaptations
- **Spec 08 — Glossary**: canonical definitions of all framework terms

## v0.5 — First specification document

- **Spec 00 — The AI Value System** (`spec/00-ai-value-system.md`, English,
  draft): the root specification. Defines the AVS model, the four value
  leaks with their seals, the AI Value Chain with full activity
  definitions (core question, outputs, value contribution, leadership,
  refusal conditions), the Return Equation as a reasoning discipline
  (with anti-patterns), the value doctrine (Return ≠ Score,
  co-realization, honesty as load-bearing), the four dimensions, the
  Recalibration Loop, and the document map for specs 01–08

## v0.4 — Value-first rewrite

- Purpose reframed around **value leaks**: four points where value escapes
  between AI ambition and realized return (potential–fit mismatch, value
  without an owner, overestimated fit, chain ending at the report) — the
  framework is the sealing system for these leaks
- New guiding principle #1: **Focus on return** (7 principles total);
  remaining principles annotated with their Return Equation role
- Lifecycle stages, disciplines, roles, and artifacts each gained an
  explicit value column (contribution to return / Return Equation)
- "Scoring systems" renamed to **Measurement systems** — measurements are
  Return Equation inputs, never deliverables
- Adoption tiers reframed as **return-confidence** levels
- "What the framework is NOT" now opens with "not a maturity scorecard"
- New open item: how to measure realized return in Recalibrate
  (follow-up interval, metrics, ownership) — key for the leak #4 claim

## v0.3 — AI Value System (mythology layer)

- Added the **AI Value System (AVS)** as the framework's top-level model: signals & demand in, realized return out
- Added the **AI Value Chain** — 7 activities (Sense → Align → Assess → Shape → Decide → Realize → Recalibrate) forming a loop; engagement stages are their operational instance
- Added the **Return Equation** (Return = Potential × Fit, Fit = ambition × capacity) and the **Return ≠ Score** distinction
- Added **four dimensions** (People & Judgment · Evidence & Data · Processes & Value Streams · Technology & Partners)
- Added the **Recalibration Loop** (retrospectives update baselines, catalogs, and the opportunity pool)
- Authoring roadmap: new `spec/00-ai-value-system.md` as the first document
- Red line added: structural inspiration from other frameworks never borrows their text, terminology, or brand

## v0.2 — Vocabulary and structural divergence

- Ambition Vector with **Sustain / Scale / Shift** axes
- **Evidence Grades A/B/C/X** replace bracket confidence markers
- Staged lifecycle naming (Groundwork → Alignment → Field → Decision → Retrospective)
- Roles: Sponsor / Lead Advisor / AI Co-analyst / Process Expert
- Seven practices regrouped into **five disciplines (D1–D5)**
- Artifacts renamed (Evidence Dossier, Hypothesis Pack, Decision Report, Executive Pre-Read); tiers Pulse / Core / Deep
- Component inventory moved out of the repository; sources policy added

## v0.1 — Founding

- Blueprint, README, LICENSE (CC-BY-SA 4.0), ATTRIBUTIONS
- Working name AIROI (AI + ROI); prior working name AMBIT recorded in alternatives
