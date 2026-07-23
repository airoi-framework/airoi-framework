# AIROI Specification 03/ACM — The AIROI Capacity Model

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## 0. About this document

The AIROI Capacity Model (ACM) is the framework's original instrument model for measuring **organizational AI capacity** — the Capacity component of Fit in the Return Equation (Spec 00 §4). It is used by discipline D3 (Capability Assessment, lens 1).

The ACM is **original AIROI work grounded in the NIST AI Risk Management Framework (AI RMF 1.0)** — a U.S. public-domain publication. Grounding means: the ACM's coverage is cross-walked to the AI RMF functions and trustworthiness characteristics so that an ACM assessment supports AI RMF-aligned conversations; the domains, sub-capacities, and every level statement are authored for AIROI's value-first purpose.

## 1. Model shape

**6 domains × 3 sub-capacities = 18 measurements.** Each sub-capacity is rated by picking the *statement* that best matches reality (statement-pick beats number-pick — it resists self-scoring flattery):

| Level | Name | Meaning | Scoring |
|---|---|---|---|
| **L0** | Not in place | no practice or awareness | 0 — counts in the average |
| **L1** | Emerging | informal, individual-dependent | 1 |
| **L2** | Established | defined, consistent, owned | 2 |
| **L3** | Embedded | measured, continuously improved | 3 |
| **N/A** | Not applicable | outside the assessed scope | excluded from average |
| *(skip)* | Not assessed | — | excluded; feeds RF-19 |

The L0 / N/A / skip distinction is load-bearing (see D3): a missing capacity, an out-of-scope capacity, and an unassessed capacity are three different facts.

## 2. Domains

| # | Domain | Asks | AIROI dimension | NIST AI RMF grounding |
|---|---|---|---|---|
| D1 | **Direction & Accountability** | who owns AI value and risk, and does strategy steer it? | People & Judgment | GOVERN (policies, accountability, oversight) |
| D2 | **People & Adoption** | can the people carry the change — skills, adoption, honesty? | People & Judgment | GOVERN (culture, workforce) + MANAGE (human oversight) |
| D3 | **Data Readiness** | will the data feed what the ambition orders? | Evidence & Data | MAP (context, data) + MEASURE (privacy-enhanced) |
| D4 | **Delivery & Integration** | can ideas reach production and live inside processes? | Processes & Value Streams · Technology & Partners | MAP (system context) + MANAGE (deployment) |
| D5 | **Trust & Control** | are stakes known, outputs validated, and people protected? | cross-cutting | MAP (risk identification) + MEASURE (trustworthiness evaluation) |
| D6 | **Operations & Learning** | does production AI stay healthy, and does the organization learn? | Technology & Partners | MANAGE (monitoring, third parties, decommissioning) + GOVERN (supply-chain policy) |

## 3. Sub-capacities and level statements

Level statements are the instrument's answer cards. L0 and N/A are uniform across all sub-capacities:

> **L0:** Not in place — no practice or awareness in this area.
> **N/A:** Not applicable to the assessed scope.


### D1 — Direction & Accountability

#### VALUE_OWNERSHIP · Value ownership

| Level | Statement |
|---|---|
| **L1 Emerging** | Someone informally champions AI topics; decisions about AI value and risk are made case by case without defined rights. |
| **L2 Established** | A named owner holds the AI value-and-risk mandate, with defined decision rights and a regular review rhythm. |
| **L3 Embedded** | Ownership is embedded across the portfolio: value and risk decisions are traceable, reviewed against outcomes, and adjusted. |

#### POLICY_GUARDRAILS · Policy & guardrails

| Level | Statement |
|---|---|
| **L1 Emerging** | Expectations for acceptable AI use circulate informally; approvals happen ad hoc. |
| **L2 Established** | A published AI policy defines acceptable use, approval paths, and escalation; exceptions are recorded. |
| **L3 Embedded** | Policy is a living system: measured for compliance and friction, revised on evidence, and understood across roles. |

#### STRATEGY_LINKAGE · Strategy linkage

| Level | Statement |
|---|---|
| **L1 Emerging** | AI initiatives start opportunistically; links to business goals are asserted, not traced. |
| **L2 Established** | Every funded AI initiative names the business goal it serves and its expected contribution; a portfolio view exists. |
| **L3 Embedded** | The AI portfolio is steered by realized contribution: funding follows measured value, and misaligned initiatives are stopped. |


### D2 — People & Adoption

#### LITERACY_SKILLS · Literacy & skills

| Level | Statement |
|---|---|
| **L1 Emerging** | AI competence is concentrated in a few self-taught individuals. |
| **L2 Established** | Role-appropriate AI training exists, and required skill profiles are defined for affected roles. |
| **L3 Embedded** | Skills are measured and renewed continuously; competence development anticipates upcoming AI use rather than trailing it. |

#### ADOPTION_INCENTIVES · Adoption & incentives

| Level | Statement |
|---|---|
| **L1 Emerging** | Available AI tools are used unevenly; adoption depends on personal enthusiasm. |
| **L2 Established** | Adoption is tracked, champions are named, and incentives do not punish honest use (such as disclosing AI assistance). |
| **L3 Embedded** | Adoption data drives enablement: friction is measured and removed, and the value of usage is visible to users themselves. |

#### SAFE_USE_CULTURE · Safe-use culture

| Level | Statement |
|---|---|
| **L1 Emerging** | People experiment quietly; problems with AI outputs are handled privately or not raised. |
| **L2 Established** | Clear reporting paths exist for AI issues and near-misses; raising them carries no penalty. |
| **L3 Embedded** | Surfacing AI limitations is rewarded and routine; lessons circulate openly and change practice. |


### D3 — Data Readiness

#### DATA_ACCESS · Availability & access

| Level | Statement |
|---|---|
| **L1 Emerging** | Data for AI purposes is obtained through personal contacts and one-off extracts. |
| **L2 Established** | Governed access paths exist for the data AI work needs, with defined roles and turnaround. |
| **L3 Embedded** | Data products are discoverable and reusable; access is fast, audited, and fit for production AI. |

#### DATA_STEWARDSHIP · Quality & stewardship

| Level | Statement |
|---|---|
| **L1 Emerging** | Data quality is discovered at the point of failure; no named stewards exist. |
| **L2 Established** | Critical data sets have named stewards, measured quality, and known lineage. |
| **L3 Embedded** | Quality management is preventive: measured continuously, improved at the source, and trusted by AI consumers. |

#### DATA_PROTECTION · Protection & privacy

| Level | Statement |
|---|---|
| **L1 Emerging** | Handling of personal and sensitive data in AI work relies on individual judgment. |
| **L2 Established** | Defined rules govern sensitive data in AI contexts: minimization, retention, and approved processing paths. |
| **L3 Embedded** | Privacy-enhancing practice is built into AI data flows and verified, not asserted. |


### D4 — Delivery & Integration

#### DEV_PRACTICE · Development practice

| Level | Statement |
|---|---|
| **L1 Emerging** | AI solutions are built as experiments that grow into production by accretion. |
| **L2 Established** | AI development follows an engineered path: versioning, evaluation before release, reproducible builds. |
| **L3 Embedded** | Delivery practice is measured and improving: evaluation harnesses, regression suites, and reuse across teams. |

#### DEPLOYMENT_RELEASE · Deployment & release

| Level | Statement |
|---|---|
| **L1 Emerging** | AI changes reach users without a defined release step or rollback plan. |
| **L2 Established** | Controlled release paths exist: approval, staged rollout, rollback, and a record of what changed. |
| **L3 Embedded** | Releases are routine and low-drama: automated checks, monitored rollouts, and rehearsed reversal. |

#### PROCESS_INTEGRATION · Process integration

| Level | Statement |
|---|---|
| **L1 Emerging** | AI tools sit beside the process; usage is optional and outcomes are untracked. |
| **L2 Established** | AI is embedded in defined process steps with owners; the process description reflects it. |
| **L3 Embedded** | Process and AI evolve together: process metrics capture AI contribution, and process owners steer further integration. |


### D5 — Trust & Control

#### RISK_IDENTIFICATION · Risk identification

| Level | Statement |
|---|---|
| **L1 Emerging** | Risks of AI use cases are considered informally, if at all, at build time. |
| **L2 Established** | Each AI use case is risk-assessed in its context before deployment, with stakes classified. |
| **L3 Embedded** | Risk pictures stay current across the lifecycle and drive proportionate controls per use case. |

#### VALIDATION_TESTING · Validation & testing

| Level | Statement |
|---|---|
| **L1 Emerging** | AI outputs are checked by trying things out; there is no systematic pre-deployment evaluation. |
| **L2 Established** | Pre-deployment validation is defined and applied: performance, robustness, and bias appropriate to stakes. |
| **L3 Embedded** | Validation is continuous and evidence-based; results gate releases and feed improvement. |

#### TRANSPARENCY_RECOURSE · Transparency & recourse

| Level | Statement |
|---|---|
| **L1 Emerging** | How AI systems reach outputs is not documented; affected people have no defined recourse. |
| **L2 Established** | Documentation matches stakes; affected users know when AI is involved and how to contest outcomes. |
| **L3 Embedded** | Transparency is verified in practice: explanations are usable, and recourse paths are exercised and measured. |


### D6 — Operations & Learning

#### MONITORING_INCIDENTS · Monitoring & incidents

| Level | Statement |
|---|---|
| **L1 Emerging** | Production AI issues surface through user complaints. |
| **L2 Established** | AI systems in production are monitored (quality, drift, cost) with a defined incident path. |
| **L3 Embedded** | Operational signals predict issues before impact; incidents are exercised, and post-mortems change practice. |

#### THIRD_PARTIES · Third parties

| Level | Statement |
|---|---|
| **L1 Emerging** | AI vendors and models are adopted individually without shared oversight. |
| **L2 Established** | Third-party AI (vendors, models, APIs) is inventoried and assessed against defined criteria. |
| **L3 Embedded** | Supply-chain posture is actively managed: dependencies monitored, exit paths defined, terms renegotiated on evidence. |

#### CONTINUOUS_LEARNING · Continuous learning

| Level | Statement |
|---|---|
| **L1 Emerging** | What is learned from operating AI stays with the operators. |
| **L2 Established** | Feedback loops from operation to improvement are defined; retiring underperforming AI is a decision, not an accident. |
| **L3 Embedded** | The organization learns as a system: operating evidence reshapes the portfolio, practices, and skills on a rhythm. |

## 4. Trustworthiness crosswalk

How the NIST AI RMF trustworthiness characteristics are covered:

| Characteristic | Primary ACM coverage |
|---|---|
| Valid & reliable | VALIDATION_TESTING · MONITORING_INCIDENTS |
| Safe | RISK_IDENTIFICATION · VALIDATION_TESTING |
| Secure & resilient | RISK_IDENTIFICATION · MONITORING_INCIDENTS · THIRD_PARTIES |
| Accountable & transparent | VALUE_OWNERSHIP · TRANSPARENCY_RECOURSE |
| Explainable & interpretable | TRANSPARENCY_RECOURSE |
| Privacy-enhanced | DATA_PROTECTION |
| Fair — harmful bias managed | VALIDATION_TESTING · SAFE_USE_CULTURE |

## 5. Scoring and red flags

- Per-domain average over answered sub-capacities (L0 included as 0; N/A and skips excluded), overall average across domains with data.
- Scores are **Measurement-system outputs** (Blueprint §4.7): inputs to the Return Equation, never deliverables.
- Presentation must annotate L0/N-A/skip counts inline — an unannotated score overstates capacity.
- Cross-checks fire per the Red-Flag Catalog (Spec 05): RF-10…RF-20 map onto ACM domains (e.g. RF-10 Delivery & Integration ahead of Direction & Accountability; RF-11 Delivery ahead of VALIDATION_TESTING; RF-12 DATA_PROTECTION low under a privacy regime).

## 6. Reference implementation

`reference-implementations/capacity-assessment.html` implements this model with the Spec 04 envelope, advisor/respondent modes, and RF-ID-cited red flags. The instrument is generated from the same model definition as this document — the statements cannot drift apart.

---

*AIROI Framework · CC-BY-SA 4.0 · NIST AI RMF is a publication of the U.S. National Institute of Standards and Technology (public domain); its mention here is grounding, not endorsement.*
