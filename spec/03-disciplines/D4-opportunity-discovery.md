# AIROI Specification 03/D4 — Opportunity Discovery

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Convert observed pain into AI opportunities that have a name and an address: a specific pain, in a specific process step, with a specific owner. Value without an address is leak #2.

**Chain activity:** Shape · **Return Equation contribution:** shapes **Potential**.

## Core question

*Where exactly can AI create value here — and who owns that value?*

---

## Inputs

- Process records from D3 (pain ranked by experts, volumes, data flows, technology reality)
- Validated Ambition Vector from D2 (opportunities must fit the ambition — P4)
- The practitioner's **opportunity pool** (calibration asset)

## The opportunity pool

A curated catalog of AI opportunity patterns from prior engagements and public evidence. The framework defines the pool's **format**; its content is the practitioner's competitive asset (Spec 00 §7).

**Pool entry format:**

| Attribute | Content |
|---|---|
| `id` | stable identifier |
| `pattern` | what the opportunity does (one sentence) |
| `taxonomy_anchor` | process taxonomy ID(s) where the pattern applies |
| `archetype` | automation / augmentation / analytics / generation |
| `ambition_class` | which Ambition Vector profile it suits (Sustain-safe / Scale / Shift) |
| `complexity` | implementation tier (light / moderate / heavy) |
| `data_requirement` | what data must exist and at what quality |
| `regulatory_sensitivity` | none / moderate / high (privacy, sectoral, AI-regulation exposure) |
| `evidence` | realization track record: where the pattern worked or failed, with measured outcomes |

## Method

### 1. Matching

For each ranked pain in each process record, search the pool by taxonomy anchor and archetype. Matching is concrete: a candidate that cannot be tied to a specific pain in a specific process step is not carried forward.

### 2. Anchoring

Every candidate records: pain reference → process step → **named owner** (usually the Process Expert or their delegate). No owner, no candidate.

### 3. Stakes & oversight classification

Every candidate carries two mandatory attributes (enum keys in Spec 04 §9):

- **`stakes`** (S0–S3) — the consequence class of a wrong or harmful AI output: S0 negligible (internal nuisance, instantly correctable) · S1 recoverable (visible impact, fully reversible by normal process) · S2 serious (customer, financial, or compliance impact; costly to repair) · S3 critical (irreversible impact on persons, or existential/regulatory impact on the organization).
- **`oversight_mode`** (O1–O4) — the human-oversight regime the opportunity will run under: O1 human decides (AI advises) · O2 human approves each output · O3 human monitors in aggregate · O4 autonomous with tripwires.

The **proportionality rule** binds them (enforced as a Decide gate in D5): S0 → O4 allowed · S1 → O3 or stricter · S2 → O2 or stricter (O3 only with demonstrated monitoring capacity, ACM D6 ≥ 2) · S3 → O1/O2 (anything looser requires a formal Sponsor exception recorded in the Decision Report).

### 4. Ambition filter

Candidates are classified against the validated Ambition Vector. A Shift-class opportunity in a Sustain-dominant organization is either reframed (a smaller Sustain-safe slice) or parked with an explicit note — never smuggled into the shortlist (P4).

### 5. Sizing (advisor ∥ co-analyst)

The co-analyst drafts rough sizing per candidate — value range, complexity, data readiness check against D3 findings, risk notes. Ranges, not point estimates (precision theater is an anti-pattern; Spec 00 §4.4). The advisor reviews and adjusts with client context.

Sizing follows the **unit-economics discipline**:

- **Cost per outcome** — the cost of one unit of result (a resolved case, a produced document), never the technical cost of a call. Ranges.
- **Quality × cost × latency triangle** — each candidate declares which corner is fixed and which two trade off.
- **Cascade pattern** — where volume × price bites, sizing assumes a cheap path for common cases with escalation to a costlier path for the remainder; designed at sizing time, not discovered in production.
- **`value_class`** — each candidate is classed `efficiency` (saves) / `revenue` (earns) / `risk` (protects). The Decision Report shows the portfolio mix; a single-class portfolio is a signal for the Sponsor (RF-39).

### 6. Shortlisting

Candidates are ranked by the multiplication logic — value potential × fit — not by novelty or vendor enthusiasm. The shortlist is small by design: a handful of opportunities with owners beats a catalog of forty.

## Outputs

- **Opportunity shortlist** — each entry: pain anchor, process step, owner, archetype, **stakes, oversight mode, value class**, sizing range with unit economics, ambition class, data/regulatory notes
- Parked list — real opportunities that failed the ambition or capacity filter, with reasons (these matter at Recalibrate: parked ≠ forgotten)
- Pool feedback — new patterns or contradicting evidence for the practitioner's pool

## Rules

1. No owner, no opportunity.
2. No process anchor, no opportunity.
3. No stakes classification, no shortlist entry (RF-32); oversight mode must satisfy the proportionality rule (RF-31).
4. Ambition filter is not optional; parked items are recorded with reasons.
5. Sizing in ranges with grades — never two-decimal ROI arithmetic; cost per outcome, not cost per call.
6. Every shortlisted item names its data requirement, its regulatory sensitivity, and its value class.

## Anti-patterns

- **Orphan value** — opportunity lists with no anchor or owner.
- **Catalog dumping** — presenting the whole pool instead of a fitted shortlist.
- **Novelty bias** — ranking by technological excitement instead of pain × fit.
- **Data wishful thinking** — shortlisting opportunities whose data requirement the D3 record already disproves.

---

*AIROI Framework · CC-BY-SA 4.0*
