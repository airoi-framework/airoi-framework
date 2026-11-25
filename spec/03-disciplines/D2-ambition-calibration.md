# AIROI Specification 03/D2 — Ambition Calibration

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Establish how much change the organization wants — honestly, with evidence, and with leadership's explicit sign-off — before any solution is designed.

**Chain activity:** Align · **Return Equation contribution:** calibrates the Ambition input to **Fit** — the reference every opportunity's ambition match is judged against (Spec 00 §4.1, D4 §4) and the shape the portfolio should follow. The vector is a distribution, never a multiplier.

## Core question

*How much change does this organization actually want — as shown by its capital, not its press releases?*

---

## The Ambition Vector

Three axes describing investment intent, expressed as a 100-point split:

| Axis | Intent | Typical signals |
|---|---|---|
| **Sustain** | keep the current business running well: stability, efficiency, compliance, cost control | flat CapEx, efficiency language, maintenance hiring, compliance programs |
| **Scale** | grow and improve the existing business: expansion, customer experience, operational excellence | customer-facing headcount growth, market-share language, CRM/operations investment, adjacent M&A |
| **Shift** | change the model: new products, new operating models, structural reinvention | new C-level transformation roles, aggressive tech/data hiring, M&A into new verticals, explicit capital reallocation |

**Invariants:** integers · sum exactly 100 · no axis 0 (every organization has at least a sliver of each).

The vector is conceptually related to the widely used run-grow-transform investment classification (see [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)); the axes, baselines, and calibration method are original AIROI work.

## Method

### 1. Baseline (prior)

Start from the sector baseline in the practitioner's calibration assets. Illustrative defaults:

| Sector | Sustain / Scale / Shift |
|---|---|
| Mature banking / insurance | 70 / 25 / 5 |
| Regulated utility | 75 / 20 / 5 |
| Established manufacturing | 65 / 30 / 5 |
| Retail / e-commerce | 50 / 35 / 15 |
| Mature tech / SaaS | 40 / 40 / 20 |
| Tech startup | 20 / 40 / 40 |
| Public sector | 80 / 18 / 2 |
| Professional services | 55 / 35 / 10 |

Baselines are priors; real signals override them. A practitioner's own recalibrated baselines (Spec 00 §7) supersede these defaults. **The defaults above have no published source** — they are illustrative, carry Grade C, and are a framework hypothesis to be replaced by recalibrated values (Spec 00 §1.3).

### 2. Evidence adjustment

Move points off the baseline only on evidence, weighted by tier (P2). Canonical judgments:

- **Compliance investment is Sustain**, regardless of how it is announced.
- **Core-system modernization is Sustain** (keeping the lights on with current-generation systems) — not Shift.
- **A new transformation-titled executive plus a handful of specialist hires** is a small, real Shift signal — points, not tens of points.
- **Language alone never moves more than a few points** (tier 3).

### 3. Hypothesis format

The dossier commits to a vector with per-axis evidence and grade, plus one dominant-mode sentence — *"a Sustain-dominant organization with an emerging Shift pocket"* beats a table. The hypothesis is bounded to a stated horizon (default 12 months).

### 4. Session calibration

At the Alignment Session, leadership calibrates the vector on a **100-point instrument with linked sliders** (moving one axis redistributes the remainder — the sum constraint is embodied, not policed). The advisor's graded hypothesis stays advisor-side; participants start from a neutral position (P5), individually commit, then negotiate to a shared vector.

**Defense rules by grade:** A — defend; a >10-point shift requires new evidence surfaced in the room. B — expect 10–20 point movement. C — expect large movement; the hypothesis was directional.

**Divergence is signal:** a wide spread between individual leadership vectors is itself a finding — record it and address it before averaging it away.

### 5. Realism Rules

Declarative post-calibration checks; violations downgrade or strike recommendations (enforced again in D5):

| Rule | Trigger | Action |
|---|---|---|
| Uncertainty mismatch | Shift > 30 while tolerance for uncertainty is low | move Shift points to Scale; flag for session |
| Capacity mismatch | Scale + Shift high while capability assessment shows foundational gaps | foundation-first sequencing; flag |
| Investment mismatch | declared ambition exceeds any plausible budget signal | vector or budget is wrong — resolve before Decide |
| Leadership split | no shared vector achievable | stop condition (Spec 02 §6) |

## Outputs

- Validated Ambition Vector with leadership sign-off (Assessment Record)
- Divergence notes (who wanted what, and why)
- Realism flags for D5

## Rules

1. Sum 100, integers, no zeros — always.
2. Never present the advisor's vector before individual commitment (P5).
3. Tie every adjustment to evidence with a tier; discount language.
4. State the dominant mode in one sentence.
5. Bound the vector to a horizon; a vector without a horizon is not falsifiable.

## Anti-patterns

- **33/33/33** — not a hypothesis; giving up.
- **Ambition inflation** — vocabulary-driven Shift points (tier-3 evidence trap).
- **Modernization confusion** — classifying system replacement as Shift.
- **Baseline ignorance** — a 60/30/10 for a utility is a surprise worth interrogating; the same split for a startup is a red flag in the other direction.
- **Averaging away disagreement** — the mean of a polarized room is a fiction; the polarization is the finding.

---

*AIROI Framework · CC-BY-SA 4.0*
