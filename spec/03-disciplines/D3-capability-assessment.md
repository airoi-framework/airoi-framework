# AIROI Specification 03/D3 — Capability Assessment

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Measure what the organization can actually absorb — at two zoom levels: the organization's AI practice maturity, and the operational reality of the processes where value will have to live.

**Chain activity:** Assess · **Return Equation contribution:** measures **Fit** (the Capacity component) and locates where Potential hides.

## Core question

*What is this organization actually capable of — organizationally, and in the processes that matter?*

---

## Two lenses

### Lens 1 — Organizational AI capacity (the AIROI Capacity Model)

The **AIROI Capacity Model (ACM)** — original AIROI work grounded in the NIST AI Risk Management Framework (public domain) — measures organizational AI capacity across **7 domains and 22 sub-capacities**. Full model definition, level statements, and NIST crosswalk: [ACM-capacity-model.md](ACM-capacity-model.md).

**Domains:** Direction & Accountability · People & Adoption · Data Readiness · Delivery & Integration · Trust & Control · Operations & Learning · Agency & Control (rated only where AI acts in systems — action level X2+; otherwise N/A).

**Organization vs. opportunity.** ACM describes the organization; Fit is judged per opportunity (Spec 00 §4). Data readiness in particular is use-case specific — an organization can be ready for one opportunity's data and not another's — so D4 checks each candidate's data requirement against the process record (lens 2), not against the D3 domain average.

**Rating scale per sub-capacity** (statement-pick — the respondent selects the level *description* that matches reality):

| Level | Meaning | Scoring treatment |
|---|---|---|
| **L0 — Not in place** | no practice or awareness | counts as 0 — a real gap honestly drags the average |
| **L1 — Emerging** | informal, individual-dependent | 1 |
| **L2 — Established** | defined, consistent, owned | 2 |
| **L3 — Embedded** | measured, continuously improved | 3 |
| **N/A** | outside the assessed scope | excluded from the average |
| *(no answer)* | not assessed | excluded; feeds the incomplete-assessment red flag |

The L0 / N/A / skip distinction is load-bearing: a missing capacity, an out-of-scope capacity, and an unassessed capacity are three different facts, and conflating them silently inflates Capacity (leak #3).

**Scoring:** per-domain average + overall average, always displayed with L0/N/A/skip counts inline so the score reads honestly. Cross-domain consistency is checked against the Red-Flag Catalog (e.g. Delivery & Integration far ahead of Direction & Accountability; data-protection gaps under privacy-regulated regimes).

### Lens 2 — Process deep-dive

For each scoped process (anchored on the process taxonomy — optimal granularity is the mid-level "process" tier; category-level is too broad and task-level too narrow to assess meaningfully):

**Context:** business criticality · frequency/volume · taxonomy anchor.

**Maturity dimensions** (statement-pick instrument — the respondent picks the level *description* that matches reality, not a number, which reduces self-scoring bias):

| Dimension | What it measures |
|---|---|
| Process design | is the process explicitly designed, documented, and does "as designed" match "as run" |
| Ownership | single accountable owner with mandate, metrics, review cadence |
| Standardization | is it done the same way everywhere; variants managed |
| People & capability | skills, training, key-person risk |
| Metrics | what is measured, and does it drive decisions |
| Continuous improvement | is improvement systematic or crisis-driven |

**Technology deep-dive** (its own block — technology is the highest-leverage dimension and the input to implementation options in D5):

- automation level (manual → digitally manual → system-assisted → orchestrated → autonomous)
- system landscape: count, age, integration method (re-keying → file → API → event-driven)
- data: entry method, quality, dashboards, process analytics
- current AI usage and **AI archetypes** (automation / augmentation / analytics / generation / none)
- UX reality: user satisfaction, workarounds and shadow tooling, self-service
- technical debt indicators and modernization status

**Pain & motivation** (positively framed per P6): improvement-potential areas, improvement levers, acceleration targets, who feels the pain, specific stories (free text — stories beat abstractions), motivations and the primary strategic motivator, success vision.

### Flow lens — Delivery Flow States

Capacity is not only practice (the ACM) — it is also **flow**. The teams that will carry realization are classified into four states:

| State | Name | Characteristic | Absorption capacity |
|---|---|---|---|
| **F1** | Underwater | firefighting; work arrives faster than it leaves | ~zero |
| **F2** | Steady | keeping up, no reserve | quick wins only |
| **F3** | Investing | paying down debt, building its own capacity | selective |
| **F4** | Compounding | improving at an accelerating rate | full |

**Flow evidence.** A team's state is determined from **observable flow signals** — behavioral-tier evidence resistant to self-scoring flattery — not from asking "how are you doing":

- how often the team actually delivers change (cadence),
- how long a change takes from decision to effect,
- what happens on failure (how fast recovery is, whether learning follows),
- the ratio of planned to forced work.

Signals are collected in D1 (public traces: release activity, firefighter hiring) and in the Field Sessions (directly from Process Experts). Flow states feed the **Absorption Rules** applied to the roadmap in D5 (WIP limit; F1 teams get flow recovery before any new opportunity; S2+ stakes require F3 or better).

**Culture texture (mini-probe).** A P6 companion: three Field Session questions about information flow — *what happens when someone brings bad news; how do you learn what other teams are doing; who is "to blame" after an incident.* The answers are not scored — they are a qualitative realization-risk signal for the Decision Report (a culture that punishes bad news will also kill Acceptance Card measurement).

## Outputs

- Organizational capacity record (per-domain ACM scores with honest annotations)
- Process records per scoped process (dimensions, technology, pain, motivations)
- **Flow states per realization team** with the observable signals behind each classification
- Culture-texture notes (qualitative, for the Decision Report's realization-risk section)
- Red flags raised for D5
- Potential locations: processes whose pain × criticality × data-readiness suggest concentrated opportunity

## Rules

1. Statement-pick over number-pick wherever a maturity level is elicited.
2. L0, N/A, and skip are distinct and never conflated.
3. Respondents see clean instruments (P5); positive framing per P6 with preserved code semantics.
4. Pain is ranked by the Process Expert, not by the advisor.
5. Every capability claim that will carry weight in the return case needs either instrument data or an explicit grade.

## Anti-patterns

- **Score theater** — reporting the maturity number without its L0/N/A/skip context.
- **Assessment sprawl** — assessing every process at full depth; scope discipline concentrates effort where Potential is (P1).
- **Self-scoring flattery** — number scales invite it; statement scales resist it.
- **Technology blindness** — assessing process maturity while ignoring the installed tooling reality that will carry any change.

---

*AIROI Framework · CC-BY-SA 4.0*
