# AIROI Specification 03/D4 — Opportunity Discovery

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../../ATTRIBUTIONS.md)

---

## Purpose

Convert observed pain into AI opportunities that have a name and an address: a specific pain, in a specific process step, with a specific owner. Value without an address is leak #2.

**Chain activity:** Shape · **Return Equation contribution:** shapes **Potential** and judges each opportunity's **Fit** (Spec 00 §4).

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
| `archetype` | automation / augmentation / analytics / generation / agent (multi-step action in systems through tools) |
| `action_level` | typical action level X0–X3 (§3) and the tools/systems the pattern needs to touch (`tool_reach`) |
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

### 3. Stakes, action & oversight classification

Every candidate carries three mandatory attributes (enum keys in Spec 04 §9). They answer three different questions — *how bad can it get* (stakes), *what can the AI do in systems* (action level), *how do humans stay in charge* (oversight) — and are classified separately:

- **`stakes`** (S0–S3) — the consequence class of a wrong or harmful AI output **or action**: S0 negligible (internal nuisance, instantly correctable) · S1 recoverable (visible impact, fully reversible by normal process) · S2 serious (customer, financial, or compliance impact; costly to repair) · S3 critical (irreversible impact on persons, or existential/regulatory impact on the organization).
- **`action_level`** (X0–X3) — what the AI is permitted to do in systems: X0 **Inform** (reads and returns output to a human; no write access) · X1 **Draft** (prepares an action — a draft, a proposed change — that a human executes) · X2 **Act with approval** (executes actions in systems through tools; each consequential action is approved by a human before it runs) · X3 **Act within bounds** (executes multi-step actions on its own within enumerated tools, limits, and tripwires; humans review after the fact).
- **`oversight_mode`** (O1–O4) — the human-oversight regime the opportunity will run under: O1 human decides (AI advises) · O2 human approves each output · O3 human monitors in aggregate · O4 autonomous with tripwires.

For X2+ candidates, two further attributes are recorded: **`action_reversibility`** (`reversible` / `compensable` / `irreversible`) and **`tool_reach`** (the tools, systems, and data the agent can touch). Action level is a design decision, independent of the Adaptation Ladder rung (D5): an agent built on a ready-made capability (A1/A2) can still act at X3.

**Classification rules:**

- **Stakes follow the worst plausible action, not only the worst output.** For X2+ candidates, stakes are classified on the most damaging action the agent's `tool_reach` permits — including actions triggered by manipulated input — not on the intended use. An `irreversible` action that reaches customers, money, or persons is at least S2 (RF-47).
- **Action and oversight must cohere:** X0/X1 → any oversight mode · X2 → O2 (the approval *is* the oversight) · X3 → O3 or O4.
- **Climb on evidence applies to action level too:** recommend the lowest action level that meets the quality bar; X3 only when operation at X2 has produced eval evidence that the agent meets the bar on the reference case set (RF-44). Autonomy is never set above demonstrated reliability.

The **proportionality rule** binds stakes to oversight (enforced as a Decide gate in D5): S0 → O4 allowed · S1 → O3 or stricter · S2 → O2 or stricter (O3 only with demonstrated monitoring capacity, ACM D6 ≥ 2) · S3 → O1/O2 (anything looser requires a formal Sponsor exception recorded in the Decision Report). Through the coherence rule it also caps the action level: an S2 opportunity runs at X2 or below unless the O3 exception holds; an S3 opportunity never runs at X3.

The oversight modes are comparable to published levels-of-autonomy scales for AI agents (e.g. operator → collaborator → consultant → approver → observer, Knight First Amendment Institute 2025); AIROI keeps its own four modes because they bind to stakes.

**Regulatory classification.** Stakes measure the consequence of failure; regulation classifies by *use case*. The two are recorded separately — an HR-screening opportunity can be S1 by consequence and still high-risk under the EU AI Act. Where the EU AI Act applies, every candidate carries **`ai_act_class`** (`prohibited` / `high_risk_annex_iii` / `high_risk_annex_i` / `transparency_art50` / `minimal`) and **`ai_act_role`** (`provider` / `deployer` / `both`). The classification is the advisor's working assessment for decision purposes, not legal advice; `high_risk_*` and `prohibited` entries are flagged for legal review. Consequences are gates in D5 Part 3 (RF-50…RF-52).

### 4. Fit judgment (ambition match × capacity)

Fit is judged **per candidate** (Spec 00 §4.1), in two parts:

**Ambition match.** Each candidate's `ambition_class` is compared with the validated Ambition Vector:

| Match | Default condition (heuristic) | Treatment |
|---|---|---|
| **strong** | the vector puts ≥ 25 points on the candidate's class | carry forward |
| **partial** | 10–24 points | reframe to a smaller slice that fits a stronger axis, or carry with an explicit Sponsor note |
| **none** | < 10 points | park with reasons — never smuggled into the shortlist (P4) |

Thresholds are illustrative defaults (Grade C) — practitioners recalibrate them from realized outcomes (Spec 00 §7). The match is categorical; the vector is never multiplied.

**Capacity for this opportunity.** Checked against what *this* candidate needs, not the organization's average: ACM prerequisites for its proposed rung and action level (D5 Part 2), its data requirement against the D3 record for its process, the flow state of the owning team (D3 flow lens), and change leadership behind it (ACM CHANGE_LEADERSHIP; a named Sponsor-level backer). Capacity is graded `sufficient` / `gap — closable within the horizon` / `insufficient`; an insufficient candidate is parked or re-cut to a lower rung or action level.

### 5. Sizing (advisor ∥ co-analyst)

The co-analyst drafts rough sizing per candidate — value range, complexity, data readiness check against D3 findings, risk notes. Ranges, not point estimates (precision theater is an anti-pattern; Spec 00 §4.4). The advisor reviews and adjusts with client context.

Sizing follows the **unit-economics discipline**:

- **Cost per outcome** — the cost of one unit of result (a resolved case, a produced document), never the technical cost of a call. Ranges.
- **Quality × cost × latency triangle** — each candidate declares which corner is fixed and which two trade off.
- **Cascade pattern** — where volume × price bites, sizing assumes a cheap path for common cases with escalation to a costlier path for the remainder; designed at sizing time, not discovered in production.
- **`value_class`** — each candidate is classed `efficiency` (saves) / `revenue` (earns) / `risk` (protects). The Decision Report shows the portfolio mix; a single-class portfolio is a signal for the Sponsor (RF-39).
- **Productivity evidence rule** — self-reported time savings are not evidence for Potential. Without a measured baseline in the target process, a productivity estimate carries at most Grade C (RF-49). Default ranges include null and negative outcomes: published measurements span from a slowdown (about −19 % for experienced developers in a randomized trial) to gains of roughly +15–50 % in narrow tasks, while firm-level effects are typically single-digit (see Spec 00 §1.3). Freed time is not value until its redeployment is named.
- **Cost of change** — sizing covers the cost of *changing the work*, not only build and operate: workflow redesign, training and enablement, owner and expert time, and transition (double running). Process redesign is the strongest observed differentiator of organizations that realize value; a cost estimate without it understates cost and overstates return (RF-55).

### 6. Shortlisting

Candidates are ranked by the multiplication logic — Potential × this candidate's Fit — not by novelty or vendor enthusiasm. The shortlist is small by design: a handful of opportunities with owners beats a catalog of forty.

**Portfolio shape.** The Ambition Vector also shapes the shortlist as a whole: the mix of candidates across Sustain / Scale / Shift classes should roughly mirror the vector. A Sustain-dominant organization with a Shift-heavy shortlist has a portfolio–vector mismatch (RF-48) — surface it to the Sponsor rather than letting single candidates' matches hide it.

## Outputs

- **Opportunity shortlist** — each entry: pain anchor, process step, owner, archetype, **stakes, action level, oversight mode, value class**, ambition match and capacity grade, sizing range with unit economics, data/regulatory notes (incl. `ai_act_class` / `ai_act_role` where applicable)
- Parked list — real opportunities that failed the ambition or capacity filter, with reasons (these matter at Recalibrate: parked ≠ forgotten)
- Pool feedback — new patterns or contradicting evidence for the practitioner's pool

## Rules

1. No owner, no opportunity.
2. No process anchor, no opportunity.
3. No stakes, action-level, and oversight classification, no shortlist entry (RF-32); oversight mode must satisfy the proportionality rule (RF-31); for X2+ candidates, stakes follow the worst plausible action.
4. Fit judgment is not optional and is made per candidate; parked items are recorded with reasons.
5. Sizing in ranges with grades — never two-decimal ROI arithmetic; cost per outcome, not cost per call.
6. Every shortlisted item names its data requirement, its regulatory sensitivity, and its value class.

## Anti-patterns

- **Orphan value** — opportunity lists with no anchor or owner.
- **Catalog dumping** — presenting the whole pool instead of a fitted shortlist.
- **Novelty bias** — ranking by technological excitement instead of pain × fit.
- **Data wishful thinking** — shortlisting opportunities whose data requirement the D3 record already disproves.

---

*AIROI Framework · CC-BY-SA 4.0*
