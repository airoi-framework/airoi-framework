# AIROI Specification 00 — The AI Value System

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

This is the root document of the AIROI specification. It defines the framework's top-level model — the **AI Value System** — and the concepts every other specification document builds on: the four value leaks, the AI Value Chain, the Return Equation, the value doctrine, the four dimensions, and the Recalibration Loop.

**Audience:** practitioners (advisors) delivering AI advisory engagements, and anyone adapting the framework. This document defines *what the system is and why it is shaped this way*. How to execute it lives in the lifecycle and discipline documents (see section 8).

**Reading order:** read this document first. Everything else in the specification is an elaboration of one of its parts.

---

## 1. The AI Value System

### 1.1 The model

```
                     ┌──────────────── AI VALUE SYSTEM ────────────────┐
                     │                                                 │
 Signals & Demand →  │   Guiding Principles          Governance        │  →  Realized Return
                     │                                                 │
                     │   AI Value Chain              Disciplines D1–D5 │
                     │                                                 │
                     │   Recalibration Loop                            │
                     │                                                 │
                     └─────────────────────────────────────────────────┘
```

The AI Value System (AVS) describes how an organization's **signals and demand** — public evidence, stated ambitions, process pain, market pressure — are converted into a **realized return** on AI investment. Everything inside the box exists to make that conversion reliable, honest, and repeatable.

The AVS makes one claim that shapes the entire framework: **most AI initiatives do not fail at the technology — they fail at the conversion.** Value leaks out between ambition and realization at four predictable points (section 2). The AVS is engineered as a sealing system for those four leaks.

### 1.2 Components

| Component | Role in the system | Specified in |
|---|---|---|
| **Guiding Principles** | seven decision rules that resolve trade-offs the same way every time | Spec 01 |
| **Governance** | who decides what, quality gates, sign-off discipline | Spec 02 |
| **AI Value Chain** | seven activities that convert signals into realized return | this document, §3 |
| **Disciplines D1–D5** | the five practice areas that execute the chain | Spec 03 |
| **Recalibration Loop** | how the system learns from each engagement | this document, §7 |

---

## 2. The four value leaks

Between an organization's AI ambition and a realized return, value escapes at four predictable points. Each leak has a name, a mechanism, and a seal.

### Leak #1 — Potential–fit mismatch

**Mechanism:** recommendations ignore how much change the organization wants and can absorb. A transformation program lands in an organization seeking stability; productivity tips land in an organization that needs to change its operating model. High-potential opportunities without fit become shelfware.

**Seal:** ambition is calibrated *before* any solution is designed (D2 — Ambition Calibration), and Realism Rules strike recommendations the organization cannot absorb.

### Leak #2 — Value without an owner

**Mechanism:** advice detached from operational reality. "Improve data governance" is not realizable value. Value is realized only in a specific process, with a specific owner, addressing a specific pain.

**Seal:** every opportunity must trace to a named pain, in a named process step, with a named owner (D4 — Opportunity Discovery, grounded in a standard process taxonomy).

### Leak #3 — Overestimated fit

**Mechanism:** unverified self-assessment. Respondents answer to look good; capacity gets overestimated; the return case is built on sand.

**Seal:** cross-check verification (D5 — the Red-Flag Catalog) plus two design principles: un-bias (respondents see clean forms) and psychological safety (questions phrased so the truth costs nothing).

### Leak #4 — The chain ends at the report

**Mechanism:** the engagement closes when the document is handed over. Realization is never measured; learning never returns. This is the largest leak — and the one the assessment industry has normalized.

**Seal:** the AI Value Chain does not close at *Decide*. It closes at *Realize* (owned by the client, prepared by the framework) and *Recalibrate* (measured by the practitioner). An engagement that ends with a score is, by AIROI's definition, unfinished.

---

## 3. The AI Value Chain

### 3.1 Overview

The AI Value Chain is a loop of seven activities. The first five run inside an advisory engagement; the last two extend beyond it — deliberately.

```
Sense → Align → Assess → Shape → Decide → Realize → Recalibrate ↺
```

The activities are universal verbs. Any engagement format (see adoption tiers, Spec 07) is an *operational instance* of the chain — stages and sessions map onto activities, never the other way around.

### 3.2 Activity definitions

#### Sense

- **Core question:** *What does the evidence say about this organization before anyone tells us anything?*
- **What happens:** signals are collected from public sources — financial trajectories, strategic behavior, technology footprint, talent movements, stated pain. Hypotheses are formed and graded (Evidence Grades A/B/C/X).
- **Output:** Evidence Dossier + Hypothesis Pack.
- **Value contribution:** cheap de-risking — evidence gathered before contact lowers the cost of every later error in Potential and Fit estimates.
- **Led by:** Lead Advisor with the AI Co-analyst running parallel research streams. Discipline: D1.

#### Align

- **Core question:** *How much change does this organization want — and how much can it absorb?*
- **What happens:** leadership calibrates the Ambition Vector (Sustain / Scale / Shift) against the advisor's evidence-graded hypothesis. Disagreement is signal, not friction.
- **Output:** validated Ambition Vector, process heat map, named Process Experts.
- **Value contribution:** fixes **Fit** — the most expensive variable to get wrong.
- **Led by:** Lead Advisor with the Sponsor and leadership. Discipline: D2.

#### Assess

- **Core question:** *What is this organization actually capable of — organizationally and in the processes that matter?*
- **What happens:** organizational AI maturity is measured; selected processes get a deep-dive (maturity dimensions, technology reality, pain points, motivations).
- **Output:** Assessment Records with scores, gaps, and red flags.
- **Value contribution:** measures **Capacity** (the second component of Fit) and locates where Potential hides.
- **Led by:** Lead Advisor with Process Experts. Discipline: D3.

#### Shape

- **Core question:** *Where exactly can AI create value here — and who owns that value?*
- **What happens:** observed pain is matched against an opportunity pool; every candidate is anchored to a process step and an owner; sizing is drafted (advisor ∥ co-analyst).
- **Output:** opportunity shortlist with owners, sizing, and implementation options.
- **Value contribution:** shapes **Potential** — value with a name and an address.
- **Led by:** Lead Advisor with the AI Co-analyst. Discipline: D4.

#### Decide

- **Core question:** *What will this organization actually do — and who commits to it?*
- **What happens:** the return case (Decision Report) is pre-read, discussed, challenged, and adjusted; leadership decides which opportunities proceed, which don't, and why; internal-vs-external execution split is agreed; the report is signed off.
- **Output:** approved Decision Report with a 0–3 / 3–6 / 6–12 month roadmap and named ownership.
- **Value contribution:** converts the return case into decisions with ownership. A decision to *wait* is a valid outcome; an undecided report is not.
- **Led by:** Sponsor decides; Lead Advisor enables. Discipline: D5.

#### Realize

- **Core question:** *Is the value actually being created?*
- **What happens:** the client executes the roadmap. The framework does not deliver this activity — it prepares it: owners named at Decide, quick wins sequenced first, implementation options resolved (provider app / custom software / own model / no AI).
- **Output:** realized changes in the client's processes and economics.
- **Value contribution:** this *is* the return. Everything before it was cost.
- **Led by:** Sponsor. The practitioner's role is preparation (before) and measurement (after).

#### Recalibrate

- **Core question:** *Did the return materialize — and what does that teach the system?*
- **What happens:** at agreed intervals after the engagement, realized return is compared against the return case. Deviations feed back: sector baselines shift, Red-Flag Catalog gains rules, the opportunity pool gains evidence.
- **Output:** measured return delta + updated calibration assets.
- **Value contribution:** converts every engagement into calibration for the next one. A practitioner with N engagements runs a measurably sharper system than at their first.
- **Led by:** Lead Advisor with the Sponsor.

### 3.3 Chain properties

1. **The chain is a loop, not a line.** Recalibrate feeds Sense: what was learned about this sector, this size of organization, this class of opportunity, improves the next engagement's starting hypotheses.
2. **The chain closes at realized return, not at the report.** Decide is the last activity the practitioner controls; it is not the last activity of the chain. This property is the framework's structural answer to leak #4.
3. **Activities are not phases.** They can overlap and iterate (Assess and Shape interleave in practice). The chain defines *what must have happened*, not a calendar.
4. **Every activity has a refusal condition.** If Align cannot produce an honest Ambition Vector, the chain should stop — proceeding with a false Fit manufactures a false return case. Stopping early is a legitimate, cheap outcome.

---

## 4. The Return Equation

### 4.1 Definition

```
Return = Potential × Fit          where Fit = Ambition × Capacity
```

- **Potential** — the value an opportunity creates *if realized*: efficiency gained, revenue enabled, risk reduced, capacity freed. Always anchored to a specific process and owner (leak #2).
- **Ambition** — how much change the organization *wants*, expressed as the Ambition Vector (Sustain / Scale / Shift, 100 points).
- **Capacity** — how much change the organization *can absorb*: skills, data readiness, governance, change track record, sponsorship.
- **Fit** — the product of ambition and capacity. An organization that wants change it cannot absorb has low fit; so does one that can absorb change it does not want.

### 4.2 The equation is a reasoning discipline, not arithmetic

The Return Equation structures judgment; it does not replace it. The framework deliberately refuses false precision: Potential is estimated in ranges with evidence grades, Fit is calibrated qualitatively against baselines and realism rules. What the equation enforces is the *multiplication logic*:

- **High Potential × low Fit ≈ zero.** Shelfware. No amount of opportunity value survives an organization that won't or can't absorb it.
- **High Fit × low Potential ≈ zero.** Busywork. Eager, capable organizations can still spend a year automating things that don't matter.
- **Nothing in the equation rewards a high maturity score.** Maturity is one input into Capacity — never the goal.

### 4.3 Consequences for sequencing

Because Return multiplies Potential by Fit, and Fit is cheaper to estimate than Potential (leadership conversation vs. field work), **the chain always calibrates Fit before investing in Potential**: Align precedes Assess and Shape. This is the framework's core sequencing rule and the reason D2 exists as a separate discipline.

### 4.4 Anti-patterns

| Anti-pattern | What it looks like | Which leak it feeds |
|---|---|---|
| **Score worship** | maturity score presented as the finding | #4 |
| **Ambition inflation** | taking leadership's transformation language at face value (language is the weakest evidence tier) | #1, #3 |
| **Orphan value** | opportunity lists with no process anchor or owner | #2 |
| **Precision theater** | Return computed to two decimal places from graded estimates | #3 |
| **Fit-blind roadmaps** | sequencing by opportunity value alone, ignoring absorption capacity | #1 |

---

## 5. Value doctrine

### 5.1 Return ≠ Score

A maturity score is an **output** — an intermediate measurement. Return is the **outcome**. The framework measures scores exclusively as inputs to a return decision, never as deliverables. Any artifact whose final line is a score has stopped one activity short of its purpose.

### 5.2 Return is co-realized

Return is not "delivered" by the practitioner. It is co-realized: the practitioner supplies evidence, calibration, and an honest return case; the Sponsor supplies decisions, capacity, and execution. An engagement without client decisions produces a research artifact, not a return. This is why *Decide* requires named ownership and why *Realize* belongs to the Sponsor.

### 5.3 Honesty is load-bearing

Every mechanism in the system — evidence grades, un-bias, psychological safety, red flags, realism rules — exists to keep one thing intact: **the honesty of the inputs to the Return Equation.** A flattering Fit estimate is not a kindness to the client; it is a defect that surfaces later as a failed roadmap.

---

## 6. The four dimensions

Every discipline examines the organization through four dimensions. No finding is complete until it has been checked against all four; the Red-Flag Catalog (Spec 05) encodes cross-dimension consistency rules.

| Dimension | What it covers | Typical failure when ignored |
|---|---|---|
| **People & Judgment** | sponsorship, skills, change capacity, psychological safety | perfect tooling, no adoption |
| **Evidence & Data** | signals, evidence grades, data readiness | AI on a foundation that can't feed it |
| **Processes & Value Streams** | process anchoring (taxonomy-based), pain, value streams | value with no address (leak #2) |
| **Technology & Partners** | tooling landscape, vendors, build/buy/own decisions | strategy that ignores what's already installed |

The dimensions are lenses, not silos: a single opportunity is examined through all four before it enters the return case.

---

## 7. The Recalibration Loop

The system learns. After each engagement, three calibration assets are updated from measured outcomes:

| Asset | What updates it | What it improves |
|---|---|---|
| **Sector baselines** | validated Ambition Vectors per sector and size | sharper starting hypotheses in *Sense* / *Align* |
| **Red-Flag Catalog** | inconsistencies that turned out to matter (or not) | earlier detection of leaks #1 and #3 |
| **Opportunity pool** | opportunities that realized (or failed) with evidence | better matching and sizing in *Shape* |

The loop is what makes the framework a *system* rather than a checklist: the same practitioner, running the same chain, produces measurably better-calibrated return cases over time. Calibration assets are defined by the framework as **formats**; their accumulated content is the practitioner's own asset and competitive advantage.

---

## 8. Document map

| Spec | Title | Elaborates |
|---|---|---|
| **00** | The AI Value System | *(this document)* |
| 01 | Guiding Principles | the seven decision rules |
| 02 | Lifecycle | stages, actors, governance, quality gates; mapping stages → chain activities |
| 03 | Disciplines D1–D5 | execution detail per discipline, incl. Return Equation contribution |
| 03/ACM | The AIROI Capacity Model | 6-domain organizational AI capacity model used by D3 (NIST AI RMF-grounded) |
| 04 | Data Standard | JSON envelope, field schema, Evidence Grades, rationale contract, margin notes |
| 05 | Red-Flag Catalog | declarative cross-check rules (trigger, severity, session action) |
| 06 | Artifacts | templates, minimum sets per tier, report gradient |
| 07 | Adoption | tiers as return-confidence levels, client commitments, quality gates |
| 08 | Glossary | canonical definitions |

Documents 01–08 are planned; this document is the root they attach to.

---

*AIROI Framework · CC-BY-SA 4.0*
