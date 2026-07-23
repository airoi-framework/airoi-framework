# AIROI Specification 05 — Red-Flag Catalog

> **Status:** Draft · **Spec version:** 0.2 · **Catalog version:** 2 (42 rules) · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

The declarative catalog of cross-check rules that guards the honesty of Return Equation inputs (leak #3). Rules fire on instrument data; instruments implement the catalog, never define it.

**Rule format:**

| Field | Content |
|---|---|
| `id` | stable identifier `RF-nn` |
| `name` | short memorable name |
| `trigger` | declarative condition over instrument fields |
| `severity` | 🚩 critical (must be resolved or explicitly carried) / ⚠ advisory (validate) / ℹ scope (methodological) |
| `action` | what the advisor does in session or synthesis |

Severity semantics: a 🚩 rule that ships unresolved and unflagged makes the report defective (D5 rule 1). The catalog grows through the Recalibration Loop — rules that never predicted anything real get demoted; recurring failure patterns get promoted into rules.

---

## 1. Ambition consistency (Alignment-stage rules)

| id | name | trigger | sev | action |
|---|---|---|---|---|
| RF-01 | **Ambition × uncertainty mismatch** | Shift > 30 while tolerance for uncertainty is low | 🚩 | validate readiness to operate under uncertainty; apply Realism Rule (move Shift → Scale) if unresolved |
| RF-02 | **Ambition × leadership split** | high Shift while leadership direction is actively contested | 🚩 | clarify agenda ownership; polarization itself is a finding — do not average it away |
| RF-03 | **Ambition × momentum mismatch** | high Shift in a self-declared stable, no-pressure situation | 🚩 | interrogate the rationale; ambition without pressure rarely gets funded |
| RF-04 | **Ambition × capacity mismatch** | Scale + Shift high while foundational capability (data readiness, governance) is low | 🚩 | foundation-first sequencing; re-cut the roadmap |
| RF-05 | **Horizon mismatch** | high Shift with expectation of measurable results within a quarter | 🚩 | reset expectations or reduce Shift; structural change has structural timelines |
| RF-06 | **Track-record mismatch** | high Shift while the last major change initiative visibly under-delivered | ⚠ | strengthen delivery capability before structural ambition |
| RF-07 | **Investment × ambition mismatch** | combined change ambition high while investment willingness is minimal | 🚩 | one of the two is wrong — resolve before Decide |
| RF-08 | **Posture × ambition mismatch** | protect-the-base budget posture with high Scale/Shift ambition | 🚩 | reconcile posture and ambition with the Sponsor |
| RF-09 | **Existential signal without Shift** | leadership flags existential/strategic threat while Shift is low | ⚠ | probe: threat unowned, or threat overstated? |

## 2. Capability consistency (Assess-stage rules)

| id | name | trigger | sev | action |
|---|---|---|---|---|
| RF-10 | **Governance gap** | implementation/deployment maturity substantially ahead of governance maturity | 🚩 | shipping without policy — governance catch-up enters the roadmap's first horizon |
| RF-11 | **Deploy without verification** | implementation maturity substantially ahead of verification/testing maturity | 🚩 | untested production AI — verification enters the first horizon |
| RF-12 | **Privacy gap under privacy regime** | privacy maturity low while privacy regulation applies | 🚩 | compliance risk — legal exposure precedes any new AI initiative |
| RF-13 | **Responsibility gap under AI regulation** | responsible-AI maturity low while AI-specific regulation applies | 🚩 | same treatment as RF-12 |
| RF-14 | **Operations gap at scale** | operations maturity low while AI is already deployed organization-wide | 🚩 | incident exposure — operational controls before expansion |
| RF-15 | **Lopsided maturity** | high variance across maturity domains | ⚠ | roadmap must coordinate progression, not only fix the weakest domain |
| RF-16 | **Foundational maturity** | overall maturity very low across most domains | ⚠ | a strategic program is needed, not point fixes — reflect in tier/scope conversation |
| RF-17 | **Inconsistent self-image** | high self-assessed maturity while no AI is actually in use | ⚠ | validate answers; instrument may have measured aspiration |
| RF-18 | **Cherry-picked maturity** | top-level maturity coexisting with "not in place" within one domain | ⚠ | interrelated sub-practices rarely span L3 and L0 — validate both ends |
| RF-19 | **Incomplete assessment** | large share of sub-practices left unassessed | ⚠ | complete or explicitly scope-limit before the results carry weight |
| RF-20 | **Scope misfit** | large share of sub-practices marked not-applicable | ℹ | verify the instrument fits the organization; consider a scoped subset |

## 3. Pain–motivation alignment (Field-stage rules)

| id | name | trigger | sev | action |
|---|---|---|---|---|
| RF-21 | **Distress signal** | very many pain points selected at once | ⚠ | prioritize top 3 before proceeding — "solve everything" paralyzes shaping |
| RF-22 | **Pain without vision** | pains recorded, no motivations | 🚩 | articulate the to-be picture before opportunities — pain alone doesn't fund change |
| RF-23 | **Vision without pain** | motivations recorded, no concrete pains | ⚠ | generic motivation won't survive prioritization — anchor in stories |
| RF-24 | **AI motivation × data reality** | "add AI" motivation while assessed data quality is poor | 🚩 | data foundation precedes AI — sequence accordingly |
| RF-25 | **Automation × standardization** | "automate" motivation while process standardization is low | 🚩 | automating chaos yields faster chaos — standardize first |
| RF-26 | **Compliance blind spot** | compliance named as pain while no compliance metric is tracked | ⚠ | measurement gap — cheap fix, high signal |
| RF-27 | **Single-point dependency** | business-critical process executable by one person | 🚩 | key-person risk enters the risk register regardless of AI plans |
| RF-28 | **End-of-life foundation** | critical process runs on an unsupported/end-of-life system | 🚩 | continuity risk precedes enhancement investment |
| RF-29 | **Automated but unmeasured** | high automation with no performance metrics | ⚠ | invisible degradation — instrument the process |
| RF-30 | **Fragmented integration** | many systems in one process integrated by manual re-keying | 🚩 | highest-leverage improvement area; often beats any AI candidate |

## 4. Decision & realization rules (Decide-stage rules — EP-01)

| id | name | trigger | sev | action |
|---|---|---|---|---|
| RF-31 | **Stakes–oversight mismatch** | S2/S3 opportunity with an oversight mode below the proportionality rule | 🚩 | tighten oversight or record a formal Sponsor exception in the report |
| RF-32 | **Unclassified stakes** | shortlisted opportunity without `stakes` / `oversight_mode` | 🚩 | classify before the opportunity may enter the approval list |
| RF-33 | **Autonomy without monitoring** | O3/O4 oversight while operations capacity (ACM D6) < 2 | 🚩 | either build monitoring capacity first or tighten the mode |
| RF-34 | **Approval without acceptance card** | opportunity entering Decide without an Acceptance Card | 🚩 | no measurement, no approval — write the card or park the opportunity |
| RF-35 | **Deployment without baseline** | approved opportunity whose baseline was never measured | 🚩 | measure before deployment; an unproven baseline makes the return unprovable |
| RF-36 | **Activity metric as success** | Acceptance Card success metric measures usage, not outcome | ⚠ | rewrite the metric as an outcome (time, cost, quality, revenue, risk) |
| RF-37 | **Rung above capacity** | Adaptation Ladder rung above the organization's ACM prerequisites | 🚩 | drop to the highest supported rung or add the capability gap to the roadmap first |
| RF-38 | **Rung above evidence** | higher rung recommended without eval evidence that a lower rung fails the bar | ⚠ | run the lower-rung eval first; climb on evidence, not appeal |
| RF-39 | **Single-class portfolio** | all shortlisted opportunities share one value class | ℹ | surface the mix to the Sponsor — a one-sided portfolio is a strategic signal, not necessarily an error |
| RF-40 | **Roadmap overcommitment** | concurrent opportunities in a horizon exceed owners in flow state F3/F4 | 🚩 | sequence, don't shrink — respect the WIP limit |
| RF-41 | **Underwater assignment** | new opportunity assigned to a team in flow state F1 | 🚩 | first roadmap item for that team is flow recovery itself |
| RF-42 | **Stakes–flow mismatch** | S2+ opportunity carried by a team below F3 | 🚩 | reassign, delay, or reduce stakes exposure |

## 5. Catalog governance

- Rules are added/demoted through the Recalibration Loop with evidence.
- Instruments cite rule IDs when they fire; the Decision Report references IDs for carried flags.
- Practitioners may maintain private extensions (`RFX-nn`); promotion to the shared catalog requires cross-engagement evidence.

---

*AIROI Framework · CC-BY-SA 4.0*
