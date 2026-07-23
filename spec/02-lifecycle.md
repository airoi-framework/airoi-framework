# AIROI Specification 02 — Lifecycle

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

The operational instance of the AI Value Chain (Spec 00 §3): stages, actors, governance, quality gates, and feedback loops. The chain defines *what must have happened*; this document defines *how an engagement makes it happen*.

---

## 1. Actors

Four roles, three lanes. The engagement process runs across a Client lane, an Advisor lane, and a Co-analyst lane; the Process Expert participates within the Client lane.

| Actor | Lane | Responsibility | Relationship to return |
|---|---|---|---|
| **Sponsor** | Client | provides access and information, attends sessions, decides at Stage 3, signs off | owns **Realize** — the return materializes in their organization |
| **Lead Advisor** | Advisor | runs the engagement end-to-end, owns judgment and synthesis, facilitates sessions | owns the return case — its accuracy and defensibility |
| **AI Co-analyst** | Co-analyst | parallel research, prefill, mechanical drafting, consistency checks | lowers the cost of the return case |
| **Process Expert** | Client | domain expert for a specific process; joins their Field Session block | anchors Potential in process reality |

The Co-analyst lane is formal: its work is visible, auditable, and reviewed by the Lead Advisor before anything reaches the client (P7).

---

## 2. Stage map

```
Stage 0 Groundwork → Stage 1 Alignment Session → Interim Analysis
      → Stage 2 Field Sessions → Synthesis (advisor ∥ co-analyst)
      → Stage 3 Decision Session → Retrospective
```

| Stage | Chain activity | Duration (Case tier) | Contribution to return |
|---|---|---|---|
| 0 — Groundwork | Sense | 1–2 weeks elapsed, time-boxed effort | cheap de-risking of every later estimate |
| 1 — Alignment Session | Align (+ Assess start) | half day | fixes Fit — the most expensive variable to get wrong |
| Interim Analysis | Assess / Shape prep | days | concentrates capacity on highest-Potential processes |
| 2 — Field Sessions | Assess + Shape | half to full day | quantifies Potential in process reality |
| Synthesis | Shape + Decide prep | 1–2 weeks | assembles the return case |
| 3 — Decision Session | Decide | half day | converts the case into decisions with ownership |
| Retrospective | Recalibrate | hours + follow-up intervals | measures realized return; learning = future return |

---

## 3. Stage definitions

### Stage 0 — Groundwork

**Intake.** The engagement starts with client demand. Before committing, the Lead Advisor runs an execution decision: scope fit, capacity, regulatory comfort. Declining is a valid outcome (refusal conditions, §6).

**Research.** With the engagement open, the co-analyst runs parallel research streams over public sources (financial, strategic, technology-pain, stakeholder — see Spec 03/D1). The Lead Advisor synthesizes into the **Evidence Dossier**: graded, falsifiable hypotheses. Synthesis is time-boxed — the dossier is a working hypothesis set, not a research report.

**Prefill.** Dossier content maps into the **Hypothesis Pack** (MD + JSON, Spec 04) that prefills the advisor's copy of the Stage 1 instruments. Participants receive a clean pre-session questionnaire; the graded prefill never leaves the advisor's side (P5).

**Exit criteria:** dossier complete with graded hypotheses in every mandatory section; ambition hypothesis committed (vector summing to 100); 3–5 falsifiable hypotheses explicitly listed; session logistics confirmed with named attendees.

### Stage 1 — Alignment Session

Half a day with leadership; up to the tier's stakeholder cap. Recommended block structure:

| Block | Purpose |
|---|---|
| Hypothesis validation | walk graded hypotheses — confirm, correct, or kill |
| Ambition calibration | 100-point Ambition Vector exercise with leadership (Spec 03/D2) |
| Shared deep-dive | one process examined with all respondents present — establishes shared language before parallel field work |
| Process heat map | identify top pain areas on the process taxonomy |
| Expert nomination | name Process Experts per selected process area |

**Why one shared deep-dive:** running a single process discussion with everyone present prevents Stage 2 sessions from diverging into incompatible vocabularies.

**Exit criteria:** Ambition Vector validated with leadership sign-off; heat map with priorities; named experts; Stage 2 scope agreed (2–4 processes).

### Interim Analysis

Consolidate Stage 1 outputs, prepare per-process interview structures, distribute light prep to experts (process map + a few questions, not a questionnaire battery). Scope discipline: the field stage examines the *agreed* processes; scope creep here dilutes Potential quantification everywhere.

### Stage 2 — Field Sessions

Structured per-process interviews, not a round-table: typically several back-to-back focused blocks in one day, each with the relevant Process Expert. Per process, the advisor maps: flow (trigger → outcome), volume, cost, error rate, manual vs. systemic steps, tribal-knowledge dependencies, data flows, ranked pain, and improvement motivations.

Candidate opportunities are matched against the opportunity pool (Spec 03/D4) — concretely: each candidate ties to a specific pain in a specific process step owned by a specific person.

**Exit criteria:** process records complete per scoped process; pain ranked by the expert (not the advisor); opportunity candidates each carry an owner and a process anchor.

### Synthesis

The parallel pattern — the engagement's quiet engine:

- **Advisor stream (judgment):** executive narrative, as-is/to-be reasoning, ambition rationale, opportunity prioritization logic, roadmap sequencing, risks and change-readiness commentary, next actions with owners.
- **Co-analyst stream (mechanics):** maturity scoring aggregation, opportunity sizing tables, architecture impact estimation, cost ranges (build/operate), implementation option per opportunity (provider app / custom software / own model / no AI), consistency checks.

Both streams converge before Stage 3; the Lead Advisor reviews, integrates, and owns the result. Without the parallel pattern, the advisor either skips consistency work or spends an extra unpaid week on it.

**Exit criteria:** Decision Report draft in gradient structure; every opportunity carries owner, sizing, implementation option; red flags resolved or explicitly carried as open questions.

### Stage 3 — Decision Session

**Pre-read discipline:** the **Executive Pre-Read** (TL;DR) is distributed ahead. The session is for discussion and decisions, not first reading.

In session: findings (maturity, ambition, gaps) → opportunity portfolio → roadmap (0–3 / 3–6 / 6–12 months) → decisions: which opportunities proceed, which don't, why; internal-vs-external execution split; adjustments captured.

**Sign-off** by the Sponsor closes the engagement's controllable phase. A decision to wait is valid; an undecided report is not (Spec 00 §3.2 — Decide).

**Exit criteria:** signed-off report; every approved opportunity has a named owner, a horizon, classified stakes with a proportionate oversight mode, and an Acceptance Card with a measured baseline; the AI Register is handed to the Sponsor; the Recalibrate schedule reads from the cards.

### Retrospective

Two loops close here:

1. **Engagement loop:** anonymous feedback from each session is reviewed; lessons extracted.
2. **System loop (Recalibrate):** at the interval(s) defined in each opportunity's Acceptance Card, realized values are compared against the card's baseline and target; kill criteria are checked; the client's AI Register is audited (review dates, retirement conditions). Deviations update the three calibration assets: sector baselines, Red-Flag Catalog, opportunity pool (Spec 00 §7).

---

## 4. Feedback discipline

An anonymous feedback form follows **every** session. Purpose is dual: steering (issues surfaced after Stage 1 get fixed before Stage 2) and system calibration (across engagements, feedback tells the practitioner which questions work, which sessions run long, where experts felt rushed). Feedback is never attributed to individuals.

---

## 5. Quality gates

Before an engagement is declared complete:

- [ ] All stages ran with the agreed attendees
- [ ] Evidence Dossier existed before Stage 1 and prefilled the advisor's instruments
- [ ] Ambition Vector validated and signed off by leadership at Stage 1
- [ ] Process heat map produced at Stage 1, refined at Stage 2
- [ ] Every priority opportunity traces to a specific pain named by a specific expert
- [ ] Every shortlisted opportunity carries stakes and a proportionate oversight mode (RF-31/32)
- [ ] Every approved opportunity has an Acceptance Card with a measured baseline (RF-34/35)
- [ ] Roadmap validated against the Absorption Rules (RF-40/41/42)
- [ ] Executive Pre-Read distributed before Stage 3
- [ ] Decision Report uses gradient structure (pre-read → findings → support → appendix)
- [ ] Sponsor signed off; AI Register handed over
- [ ] Feedback collected after every session
- [ ] Retrospective held; calibration assets updated
- [ ] Recalibrate follow-up scheduled (reading from the Acceptance Cards)

A failed gate is fixed before close — sign-off on an incomplete engagement converts a controllable defect into a client-side failure.

---

## 6. Refusal and stop conditions

Stopping early is a legitimate, cheap outcome (Spec 00 §3.3). Canonical stop points:

| Point | Condition | Action |
|---|---|---|
| Intake | scope misfit, no sponsor, regulatory discomfort | decline the engagement |
| Stage 1 | leadership cannot or will not produce an honest Ambition Vector | pause; escalate to Sponsor; proceeding manufactures a false return case |
| Stage 2 | experts unavailable or scoped processes inaccessible | reduce scope and re-price confidence, or pause |
| Stage 3 | Sponsor unwilling to decide anything | deliver with an explicit "no decision" flag — and record it as a realization risk |

---

*AIROI Framework · CC-BY-SA 4.0*
