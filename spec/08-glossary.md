# AIROI Specification 08 — Glossary

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

Canonical definitions. Where a term is specified in depth elsewhere, the entry cites the spec.

| Term | Definition |
|---|---|
| **Absorption Rules** | Roadmap constraints derived from flow states: WIP limit (concurrent opportunities ≤ F3/F4 owners), the underwater rule (F1 teams get flow recovery first), and the stakes–flow rule (S2+ needs F3+). (D3, D5) |
| **Acceptance Card** | Per-opportunity measurement contract agreed at Decide: outcome metric, measured baseline, ranged target, eval method, quality bar, kill criteria, review interval. No measurement, no approval. (Spec 06 §2.10, D5) |
| **Action Levels (X0–X3)** | What an AI is permitted to do in systems: Inform / Draft / Act with approval / Act within bounds. Orthogonal to the Adaptation Ladder; X2+ carries ACM prerequisites (D5–D7 ≥ 2) and stakes classified on the worst plausible action. (D4 §3, D5) |
| **Adaptation Ladder** | Implementation postures A0–A5 (No AI / Use / Instruct / Ground / Specialize / Own) ordered by depth of capability ownership, each with ACM prerequisites and a lock-in profile. Says nothing about what the AI may do — see Action Levels. (D5) |
| **Agent** | An opportunity archetype in which AI takes multi-step actions in systems through tools (action level X2+). (D4) |
| **Agency & Control (ACM D7)** | The ACM domain for AI that acts: agent identity & privilege, action bounds & interruption, action traceability. N/A only when nothing in scope acts. (ACM) |
| **AI Act class / role** | Per-opportunity EU AI Act classification (prohibited / high-risk Annex III / high-risk Annex I / transparency Art. 50 / minimal) and the organization's role (provider / deployer). Recorded separately from stakes. (D4 §3) |
| **AI Co-analyst** | The AI tooling actor: parallel research, prefill, mechanical drafting, consistency checks. A formal lane in the process, defined by capability, never by product. (Spec 00, 02; P7) |
| **AI Register** | The client-kept inventory of approved AI handed over at Decide: stakes, action level, oversight mode, owner, rung, model/vendor/version with vendor retirement date, agent identity (X2+), review date, retirement criterion per entry. Carries the sunset discipline and the model-change rule. (Spec 06 §2.11) |
| **AI Value Chain** | Seven looped activities converting signals into realized return: Sense → Align → Assess → Shape → Decide → Realize → Recalibrate. Closes at realized return, not at the report. (Spec 00 §3) |
| **AI Value System (AVS)** | The framework's top-level model: signals & demand in, realized return out; contains principles, governance, the value chain, disciplines, and the Recalibration Loop. (Spec 00 §1) |
| **Ambition** | Where the organization wants change, expressed as the Ambition Vector — a distribution, not a magnitude. Enters Fit through the ambition match of each opportunity. (Spec 00 §4, D2) |
| **Ambition match** | How well an opportunity's ambition class matches the validated vector: strong / partial / none. A filter and discount, never arithmetic on the vector. (D4 §4) |
| **Ambition Vector** | Sustain / Scale / Shift as a 100-point integer split; no zero components; bounded to a horizon. (D2) |
| **Analysis Artifacts** | Numbered working MD series produced between sessions; makes the reasoning chain citable. (Spec 06 §2.5) |
| **Assessment Record** | Export of a completed instrument: scores with context, fired red flags, notes. The audit trail. (Spec 06 §2.4) |
| **Baseline** | The pre-deployment measured value of an Acceptance Card's success metric; without it, the return is unprovable. (Spec 06 §2.10) |
| **Capacity** | How much of a given change the organization can absorb: ACM prerequisites for the opportunity's rung and action level, data readiness for its data requirement, owner flow state, change leadership. Measured by D3, judged per opportunity in D4. |
| **Cost of change** | The cost of changing the work — redesign, enablement, owner time, transition — estimated alongside build and operate. (D4 §5, D5) |
| **Climb on evidence** | The Adaptation Ladder rule: recommend a higher rung only when a lower rung demonstrably fails the quality bar per eval — never for technological appeal. (D5) |
| **Cost per outcome** | Unit-economics measure: the cost of one unit of result, never the technical cost of a call. (D4 §5) |
| **Culture texture** | A qualitative Field Session probe of information flow (bad news, cross-team learning, blame) used as a realization-risk signal. (D3) |
| **Decision Report** | The return case: gradient-structured document ending in decisions, owners, and horizons — never in a score. (Spec 06 §2.6) |
| **Decision Session** | Stage 3: pre-read, discussion, decisions, sign-off. (Spec 02) |
| **Disciplines (D1–D5)** | The five practice areas: Evidence & Hypotheses, Ambition Calibration, Capability Assessment, Opportunity Discovery, Decision Enablement. (Spec 03) |
| **Evidence Dossier** | Graded, falsifiable hypotheses about the organization from public evidence; produced in Groundwork inside a time box. (Spec 06 §2.1, D1) |
| **Evidence Grades** | A (strong verifiable) / B (multi-source plausible) / C (weak signal) / X (no evidence — ask). Uniform across all artifacts. (Spec 04 §3) |
| **Evidence tiers** | Weighting hierarchy: capital allocation > strategic behavior > language. (P2) |
| **Executive Pre-Read** | TL;DR distributed before the Decision Session so the session is discussion, not first reading. (Spec 06 §2.7) |
| **Field Sessions** | Stage 2: structured per-process interviews with Process Experts. (Spec 02) |
| **Fit** | Per opportunity: ambition match × capacity for that opportunity — the organization-side multiplier of the Return Equation. (Spec 00 §4) |
| **Flow States (F1–F4)** | Team delivery-flow classification — Underwater / Steady / Investing / Compounding — determined from observable flow signals; governs absorption capacity. (D3) |
| **Four dimensions** | People & Judgment · Evidence & Data · Processes & Value Streams · Technology & Partners — lenses applied by every discipline. (Spec 00 §6) |
| **Gradient structure** | Report layering where each depth level is complete on its own: pre-read → findings → support → appendix. (Spec 06 §2.6) |
| **Groundwork** | Stage 0: intake, parallel research, dossier synthesis, prefill. (Spec 02) |
| **Hypothesis Pack** | The dossier's MD + JSON twin that prefills advisor-side instruments losslessly. (Spec 06 §2.2, Spec 04) |
| **Kill criteria** | The pre-agreed condition under which an approved opportunity is stopped or rolled back; set at Decide while heads are cool. (Spec 06 §2.10) |
| **Lead Advisor** | The human running the engagement; owns judgment, synthesis, and every claim in the report. (Spec 02 §1) |
| **Margin notes** | Facilitator-facing per-screen note fields; receive aggregated facilitation guidance with canonical markers (`Pushback:` / `Defend hardest:` / `Hardest question:`). (Spec 04 §5) |
| **Opportunity pool** | The practitioner's curated catalog of AI opportunity patterns; format defined by the framework (D4), content is the practitioner's asset. |
| **Oversight Modes (O1–O4)** | Human-oversight regimes: human decides / human approves / human monitors / autonomous with tripwires. Bound to stakes by the proportionality rule. (D4 §3) |
| **Parked list** | Real opportunities that failed the ambition or capacity filter, recorded with reasons. (D4) |
| **Portfolio shape** | The mix of shortlisted opportunities across Sustain / Scale / Shift classes, compared against the Ambition Vector (RF-48). (D4 §6) |
| **Potential** | The value an opportunity creates if realized; always anchored to a process and an owner. (Spec 00 §4) |
| **Process Expert** | Client-side domain expert for a specific process; anchors Potential in reality. (Spec 02 §1) |
| **Proportionality rule** | The minimum oversight mode required per stakes level; exceptions require a recorded Sponsor decision. (D4 §3, D5) |
| **Realism Rules** | Declarative checks that strike or downgrade recommendations exceeding absorption capacity. (D2 §5) |
| **Realize** | The chain activity owned by the Sponsor in which value actually materializes; prepared and measured, not delivered, by the practitioner. (Spec 00 §3.2) |
| **Recalibrate** | Post-engagement measurement of realized return against the return case; feeds the Recalibration Loop. (Spec 00 §3.2) |
| **Recalibration Loop** | The system's learning cycle: sector baselines, Red-Flag Catalog, and opportunity pool update from measured outcomes. (Spec 00 §7) |
| **Red-Flag Catalog** | Declarative cross-check rules (RF-nn) guarding input honesty; instruments implement it, the spec defines it. (Spec 05) |
| **Refusal condition** | A defined point where stopping the engagement is the correct, cheap outcome. (Spec 00 §3.3, Spec 02 §6) |
| **Return** | The realized outcome of the engagement: Potential × Fit per opportunity, materialized and summed. The only deliverable that counts. (Spec 00 §4) |
| **Return case** | The Decision Report's argument: evidence-graded P × F reasoning with a realization path. (D5) |
| **Return Equation** | Return = Potential × Fit; a reasoning discipline, not arithmetic. (Spec 00 §4) |
| **Sponsor** | The client-side owner of the engagement and of Realize. (Spec 02 §1) |
| **Stakes Ladder (S0–S3)** | Consequence classification of a wrong or harmful AI output or action: negligible / recoverable / serious / critical. For X2+ opportunities, classified on the worst plausible action. Mandatory per shortlisted opportunity. (D4 §3) |
| **Sunset discipline** | The AI Register rule that every entry carries a review date and a retirement criterion — no immortal AI systems. (Spec 06 §2.11) |
| **Sustain / Scale / Shift** | The Ambition Vector axes: operate well / grow the existing / change the model. (D2) |
| **Tier (Pulse / Case / Launch)** | Return-confidence levels sizing the engagement — named for what the client buys: a pulse check, a defensible return case, launch readiness. (Spec 07) |
| **Time box** | Fixed synthesis budget for the dossier; prevents research sprawl. (D1) |
| **Un-bias** | Respondents see clean instruments; graded prefill exists only advisor-side. (P5, Spec 04 §6) |
| **Value class** | Opportunity classification by value type: efficiency (saves) / revenue (earns) / risk (protects); the portfolio mix is surfaced to the Sponsor. (D4 §5) |
| **Value leaks** | The four predictable points where value escapes between ambition and realization; the framework is their sealing system. (Spec 00 §2) |
| **WIP rule** | The absorption limit: concurrent roadmap opportunities per horizon must not exceed owners in flow state F3/F4. (D5) |

---

*AIROI Framework · CC-BY-SA 4.0*
