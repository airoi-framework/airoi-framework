# AIROI Specification 03/D5 — Decision Enablement

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Protect the return case from inconsistency, assemble it, and convert it into decisions with ownership — then set up measurement of what gets realized.

**Chain activities:** Decide (+ preparing Realize and Recalibrate) · **Return Equation contribution:** protects **R** from dishonest inputs (leak #3) and from the report-shelf death (leak #4).

## Core question

*Will this organization actually decide — and will we know whether the return materialized?*

---

## Part 1 — Red-flag verification

Before synthesis, all instrument data passes the **Red-Flag Catalog** (Spec 05): declarative cross-check rules that detect inconsistent or unrealistic self-assessment across instruments and dimensions.

- Every triggered flag is resolved (explained by context), validated (raised in session), or carried into the report as an explicit open risk.
- Flags are never silently dropped: an unresolved flag in a shipped report is a defect.

## Part 2 — Synthesis (advisor ∥ co-analyst)

The parallel drafting pattern (Spec 02 §3-Synthesis). The advisor owns judgment; the co-analyst owns mechanics; the advisor owns the merge.

**Report gradient.** The Decision Report is structured so each layer serves a different reader depth:

```
Executive Pre-Read (TL;DR)  →  Findings  →  Supporting analysis  →  Appendix
```

A reader who stops after any layer still leaves with a correct picture — just less detail.

**The Adaptation Ladder.** Per shortlisted opportunity, the co-analyst drafts an implementation rung, reviewed by the advisor. The ladder orders implementation postures by the depth of the organization's relationship to the AI capability — each rung has capability prerequisites (ACM domains, Spec 03/ACM) and a lock-in profile:

| Rung | Name | Meaning | Prerequisites (ACM) | Lock-in |
|---|---|---|---|---|
| **A0** | No AI | process redesign or standard software solves it | — | — |
| **A1** | Use | a ready-made AI capability, as is | D2 ≥ 1 | low |
| **A2** | Instruct | adapting behavior through instructions and configuration | D2 ≥ 1, D4 ≥ 1 | low |
| **A3** | Ground | connecting the capability to own data and knowledge | D3 ≥ 2, D4 ≥ 2 | moderate |
| **A4** | Specialize | adjusting the capability's behavior on own data | D3 ≥ 2, D4 ≥ 3, D5 ≥ 2 | high |
| **A5** | Own | owning the AI capability end to end | D3 ≥ 3, D4 ≥ 3, D6 ≥ 2 | highest |

A0 is load-bearing: a framework that can say *"you don't need AI here"* is credible when it says the opposite.

**Climb on evidence.** Recommendations start at the lowest rung whose evaluation (per the opportunity's Acceptance Card) meets the quality bar. A higher rung is recommended **only** when a lower rung demonstrably fails the bar — never for technological appeal (RF-38). A rung above the organization's ACM prerequisites is a red flag, not an aspiration (RF-37).

**Cost discipline:** build/operate estimates in ranges tied to the rung — never point estimates; expressed as cost per outcome (D4 §5).

## Part 3 — Decide gates

Before the Decision Session, every opportunity entering the approval list must pass three gates:

1. **Proportionality gate** — `stakes` and `oversight_mode` are set and satisfy the proportionality rule (D4 §3). An S3 opportunity proposed for loose oversight requires a formal Sponsor exception recorded in the report (RF-31/RF-32).
2. **Acceptance gate** — an **Acceptance Card** exists (Spec 06 §2.10): success metric (an outcome, not an activity), **measured baseline**, ranged target, eval method, quality bar, **kill criteria**, and review interval. *No measurement, no approval* (RF-34) — a return that was never defined can never be proven. The baseline is measured before deployment (RF-35); kill criteria are agreed while heads are cool, at Decide, not after a year of sunk cost.
3. **Absorption gate** — the roadmap respects the Absorption Rules (D3 flow lens): concurrent opportunities per horizon ≤ owners in flow state F3/F4 (RF-40); no new opportunity lands on an F1 team — its first roadmap item is flow recovery itself (RF-41); S2+ opportunities are carried only by teams at F3 or better (RF-42).

## Part 4 — The Decision Session

- **Pre-read distributed ahead** — the session is for discussion, not first reading.
- Contested recommendations are pre-positioned with the Sponsor before the session.
- The session walks: findings → opportunity portfolio (with stakes, oversight, value-class mix) → roadmap (0–3 / 3–6 / 6–12 months) → **decisions**: proceed / park / reject per opportunity, with reasons; internal-vs-external execution split.
- **Sign-off** closes the controllable phase. A decision to wait is valid; an undecided report is not.

## Part 5 — Preparing Realize and Recalibrate

The engagement's last controllable acts:

1. **Realization handoff** — every approved opportunity leaves the room with a named owner, a horizon, and a first step small enough to start within weeks (quick-win sequencing).
2. **AI Register handover** (Spec 06 §2.11) — the inventory of approved AI the client keeps going forward: opportunity → stakes → oversight mode → owner → review date → retirement criterion. The register carries the **sunset discipline**: every entry has a review date and a retirement condition, so Realize stops being a black box — the register is what Recalibrate audits.
3. **Measurement agreement** — Recalibrate reads the Acceptance Cards: the follow-up interval(s) and metrics are already defined per opportunity, baseline included. Without cards, the leak #4 seal is rhetoric.
4. **Retrospective** — engagement lessons update the three calibration assets (Spec 00 §7).

## Outputs

- Verified, red-flag-clean (or explicitly flagged) return case
- **Decision Report** (gradient structure) + **Executive Pre-Read**
- Signed-off decisions with owners, horizons, stakes, oversight modes, and Acceptance Cards
- **AI Register** handed to the Sponsor
- Recalibrate schedule reading from the Acceptance Cards

## Rules

1. No unresolved red flag ships silently.
2. The advisor owns every claim in the report — co-analyst output is draft material until reviewed (P7).
3. Every recommendation traces to instrument data or a graded hypothesis; the chain of evidence is auditable.
4. "No AI" (rung A0) is a first-class recommendation.
5. No approval without an Acceptance Card; no deployment without a measured baseline.
6. No sign-off without the AI Register handed over and a Recalibrate agreement in place.

## Anti-patterns

- **Score worship** — the report's climax is a maturity number instead of decisions.
- **Consistency skip** — shipping without the red-flag pass because time ran short (this is precisely when it matters).
- **Rung romance** — climbing the Adaptation Ladder for technological appeal instead of eval evidence.
- **Vendor default** — implementation recommendations that always land on the same answer regardless of stakes, data sensitivity, and volume.
- **Activity theater** — Acceptance Cards whose success metric measures usage instead of outcome (RF-36).
- **Handoff and vanish** — closing the engagement without cards, register, and measurement agreement; the chain dies at Decide.

---

*AIROI Framework · CC-BY-SA 4.0*
