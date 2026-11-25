# AIROI Specification 06 — Artifacts

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

Defines every artifact the framework produces: purpose, structure, format, quality criteria, and minimum sets per adoption tier. Artifacts are instruments of return, not deliverables for their own sake (P1) — each entry names its value function.

---

## 1. Artifact register

| Artifact | Stage | Format | Value function |
|---|---|---|---|
| Evidence Dossier | Groundwork | MD | de-risks the engagement before first contact |
| Hypothesis Pack | Groundwork | MD + JSON twin | carries evidence into sessions losslessly |
| Session Instruments | Stage 1–2 | interactive forms honoring Spec 04 | structured capture of Fit and Potential signals |
| Assessment Records | Stage 1–2 | MD/JSON exports | auditable trail of measurements |
| Analysis Artifacts | Interim / Synthesis | numbered MD series | intermediate products of the return case |
| Decision Report | Synthesis | gradient document | **the return case** — P × F argument with a realization path |
| Acceptance Cards | Synthesis / Decide | structured cards (per approved opportunity) | make the return provable: metric, baseline, kill criteria defined before deployment |
| AI Register | Decide (handover) | living inventory (client-kept) | carries the sunset discipline into Realize; what Recalibrate audits |
| Executive Pre-Read | before Stage 3 | short document | enables Decide without in-room first reading |
| Feedback Records | after each session | anonymous forms | process quality and steering |
| Retrospective Notes | close | MD | system calibration = future return |

---

## 2. Artifact definitions

### 2.1 Evidence Dossier

Graded, falsifiable hypotheses about the organization, structured in sections that map to instrument fields. Mandatory content:

1. Organization profile (facts — the only ungraded section)
2. Financial trajectory and capital-allocation signals
3. **Ambition Vector hypothesis** (sum-100, per-axis evidence and grade, dominant-mode sentence, horizon)
4. Process-pain hypothesis on the taxonomy (≥ 2 flagged areas, each with ≥ 2 sources for the strongest claims)
5. Technology footprint and pain signals
6. Stakeholder map and session dynamics
7. **3–5 falsifiable hypotheses** for session validation
8. Workshop facilitation section (feeds margin notes with canonical markers)

**Quality criteria:** every claim graded with rationale; passes the "what will I do differently" test; produced inside the time box.

### 2.2 Hypothesis Pack

The dossier's machine-readable twin for instrument prefill: MD for humans, JSON (Spec 04 envelope) for instruments, **lossless agreement between the two**. Advisor-side only (P5).

**Quality criteria:** every JSON `note` traces to an MD `Rationale:` line verbatim; validates against Spec 04 §7; facilitation items carry canonical markers.

### 2.3 Session Instruments

Interactive forms implementing Spec 04 — reference implementations exist, but any conforming tool qualifies. Required behaviors: dual rendering (advisor/respondent modes), local crash-safe persistence, full-envelope export, red-flag evaluation with rule IDs (Spec 05), honest score presentation (L0/N-A/skip annotations inline).

### 2.4 Assessment Records

Exports of completed instruments: scores with context, fired red flags, margin notes, divergence notes. The audit trail from raw session input to report claim runs through these records — they are retained, not overwritten.

### 2.5 Analysis Artifacts

A numbered working series (`01-…`, `02-…`) produced between sessions and during synthesis: generic domain knowledge, as-is syntheses, focus recommendations, capability evaluations, architecture snapshots, opportunity portfolios. Numbering makes the reasoning chain citable — report claims reference artifact numbers.

### 2.6 Decision Report

The return case. **Gradient structure** (each layer complete at its own depth):

1. **Executive summary** — the decision picture: ambition, top opportunities, recommended path, first steps
2. **Findings** — as-is, validated Ambition Vector with rationale, capability picture (honest scores), gap analysis
3. **Opportunity portfolio** — shortlist with owners, stakes, action levels, oversight modes, ambition match and portfolio shape, value-class mix, sizing ranges (unit economics), Adaptation Ladder rungs; parked list with reasons
4. **Roadmap** — 0–3 / 3–6 / 6–12 month horizons; quick wins first; every item has an owner with a known flow state; validated against the Absorption Rules
5. **Risks and dependencies** — carried red flags (by ID), regulatory exposure, delivery risks, culture-texture notes
6. **Next actions** — what happens in the first weeks, by whom
7. **Appendix** — Acceptance Cards, assessment records, methodology notes, evidence references

**Quality criteria:** every recommendation traces to instrument data or a graded hypothesis; no unresolved 🚩 flag ships silently; "no AI" recommendations appear where warranted; ends with actions and owners, never with a score.

### 2.7 Executive Pre-Read

The TL;DR distributed before the Decision Session: one to few pages — ambition profile, top findings, shortlist, the decisions being asked for. Written so a reader who reads nothing else can still decide responsibly.

### 2.8 Feedback Records

Anonymous, short, after every session. Standard core: pacing, comprehensibility, safety to speak, one open field. Aggregated only; never attributed.

### 2.9 Retrospective Notes

What the engagement taught the system: hypothesis hit-rate (dossier vs. validated reality), fired-flag precision, pool feedback, baseline deltas — the raw material of the Recalibration Loop.

### 2.10 Acceptance Cards

One card per approved opportunity, written at Synthesis and agreed at Decide. **No measurement, no approval** — the card is what makes the return provable rather than asserted.

| Field | Content |
|---|---|
| `success_metric` | what is measured — an **outcome** (time, cost, quality, revenue, risk), never an activity (RF-36) |
| `baseline` | the value **before** deployment — measured, not estimated (RF-35) |
| `target` | expected value, in ranges (no false precision) |
| `eval_method` | how it is measured: reference case set / A-B comparison / operational metric |
| `quality_bar` | minimum output quality for the opportunity's stakes level |
| `kill_criteria` | the condition under which the opportunity is stopped or rolled back |
| `review_interval` | when Recalibrate measures |
| `reeval_trigger` | events that force a re-run of the eval before they reach production — at minimum any change of model, model version, or (X2+) `tool_reach` |
| `cost_of_change` | ranged estimate of redesign, enablement, owner time, and transition cost (RF-55); re-estimated with cost per outcome at each review |

Rules: the baseline is measured before deployment; kill criteria are agreed at Decide while heads are cool — not after a year of sunk cost. For S1+ stakes, the preferred `eval_method` is a **reference case set** (real cases with expected outputs), built cheaply during the Field Sessions from the Process Experts' own examples. Cards appear in the Decision Report appendix and travel into the AI Register.

### 2.11 AI Register

The handover inventory of approved AI, delivered to the Sponsor at Decide and **kept by the client** from then on. One row per approved opportunity:

| Field | Content |
|---|---|
| `opportunity` | reference to the shortlist entry and its Acceptance Card |
| `stakes` / `action_level` / `oversight_mode` | S0–S3 / X0–X3 / O1–O4 as approved (with any recorded Sponsor exceptions) |
| `ai_act_class` / `ai_act_role` | where the EU AI Act applies (D4 §3) |
| `owner` | the named realization owner |
| `adaptation_rung` | A0–A5 as approved |
| `model` | model, vendor, and version in production |
| `vendor_retirement_date` | the vendor's announced deprecation or retirement date for that version ("none announced" is a valid, dated entry) |
| `agent_identity` | X2+ only: the agent's own identity, `tool_reach` with permissions, log owner, and stop mechanism |
| `review_date` | when the entry is next reviewed — never later than `vendor_retirement_date` |
| `retirement_criterion` | the condition under which the system is retired |

The register carries the **sunset discipline**: no entry without a review date and a retirement condition. It also carries the **model lifecycle**: vendor retirement windows can be a few months — shorter than a typical Recalibrate interval — so the register, not the next engagement, is where a forced model change is caught and the eval re-run (RF-54, RF-56). The AI Register is the client's internal inventory; it is distinct from, and does not replace, registration in the EU database for high-risk systems (EU AI Act Art. 49/71) where that applies. Realize stops being a black box — the register is the object Recalibrate audits, and the client's living record of what AI runs where, under whose oversight, at what stakes.

---

## 3. Minimum artifact sets per tier

| Artifact | Pulse | Case | Launch |
|---|---|---|---|
| Evidence Dossier | reduced (2 streams) | full | full + vertical deep-dives |
| Hypothesis Pack | ✓ | ✓ | ✓ |
| Assessment Records | Stage 1 only | ✓ | ✓ |
| Analysis Artifacts | minimal | ✓ | ✓ extended |
| Decision Report | short form | full gradient | full + business cases, architecture, backlog, 90-day plan |
| Acceptance Cards | ✓ (short form) | ✓ | ✓ |
| AI Register | merged into report | ✓ | ✓ |
| Executive Pre-Read | merged into report | ✓ | ✓ |
| Feedback Records | ✓ | ✓ | ✓ |
| Retrospective Notes | ✓ | ✓ | ✓ |

Feedback and retrospective are never cut — the Recalibration Loop runs at every tier.

---

*AIROI Framework · CC-BY-SA 4.0*
