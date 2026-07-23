# AIROI Specification 03/D1 — Evidence & Hypotheses

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Build a graded, falsifiable picture of the organization from public evidence **before anyone tells us anything** — so that every later conversation starts from hypotheses to validate rather than blank pages to fill.

**Chain activity:** Sense · **Return Equation contribution:** input accuracy — quality evidence lowers the uncertainty of both Potential and Fit estimates.

## Core question

*What does the evidence say about this organization — and what will we do differently in the sessions because of it?*

---

## Inputs

- Public sources: financial reports, registries, press, job postings, review sites, leadership interviews, technology footprints
- Sector baselines from the practitioner's calibration assets (Spec 00 §7)
- Engagement scope (tier, geography, sector)

## Method

### 1. Parallel research streams

The AI Co-analyst runs four streams concurrently; each writes a raw findings file:

| Stream | Looks at | Typical Fit/Potential signal |
|---|---|---|
| **Financial** | revenue trajectory, CapEx pattern, ownership, funding | capital allocation = tier-1 ambition evidence |
| **Strategic** | announcements, M&A, new units, leadership changes | strategic behavior = tier-2 evidence |
| **Technology & pain** | job postings, tech stack traces, employee reviews, delivery-flow traces (release activity, firefighter-role hiring) | *job postings reveal what is actually broken*; flow traces seed the D3 flow-state hypothesis |
| **Stakeholder** | who leads what, board composition, public personas | session dynamics, sponsor identification |

Stream depth scales with tier (Pulse: two streams; Case: all four; Launch: all four plus vertical deep-dives).

### 2. Time-boxed synthesis

The Lead Advisor synthesizes raw findings into the **Evidence Dossier** within a fixed time box. The box is a feature: synthesis expands to fill available time, and the dossier is a hypothesis set, not a monograph.

### 3. Grading and falsifiability

Every claim gets an Evidence Grade (A/B/C/X) and a `Rationale:` line (Spec 04 §4). Every section passes the falsifiability test: *what happens in the session if this is wrong?*

Mandatory dossier commitments:

- an **Ambition Vector hypothesis** (three integers, sum 100 — see D2)
- a **process-pain hypothesis** flagging at least two areas on the process taxonomy
- **3–5 explicitly falsifiable hypotheses** for session validation

### 4. Prefill

Dossier sections map to instrument fields (Spec 04); facilitation guidance aggregates into margin notes with the canonical markers (`Pushback:` / `Defend hardest:` / `Hardest question:`). The prefill is advisor-side only (P5).

## Outputs

- **Evidence Dossier** (MD) — graded hypotheses with rationale
- **Hypothesis Pack** (MD + JSON twin, lossless) — instrument prefill
- Raw stream files (working material, not client-facing)

## Rules

1. Evidence tiers are weighted per P2: capital allocation > strategic behavior > language.
2. Every hypothesis is graded; every grade has a rationale.
3. The synthesis time box is fixed at engagement start and honored.
4. Killed hypotheses are recorded, not deleted — they are calibration data.
5. The dossier commits: no section may hide behind "insufficient data" when a graded C/X hypothesis is possible.

## Anti-patterns

- **Neutral encyclopedia** — description without commitment; fails the "what will I do differently" test.
- **Low confidence everywhere** — grading everything C/X to stay safe; commitment is the deliverable.
- **Rabbit hole** — one stream consuming the time box; depth balance is the advisor's responsibility.
- **Wrong frame** — researching the company the advisor expected instead of the company the evidence shows.

---

*AIROI Framework · CC-BY-SA 4.0*
