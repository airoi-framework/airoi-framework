# AIROI Specification 04 — Data Standard

> **Status:** Draft · **Spec version:** 0.1 · **Schema version:** 1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

The machine-readable contract that connects artifacts and instruments: how hypotheses travel from the Evidence Dossier into session instruments, how answers travel out, and how everything stays lossless in between. Any tool that honors this standard is a valid AIROI instrument; the reference implementations are conveniences, not requirements.

---

## 1. The JSON envelope

Every instrument reads and writes the same envelope:

```json
{
  "_meta": {
    "schema_version": 1,
    "engagement": "<slug>",
    "instrument": "<instrument-id>",
    "stage": "<stage-id>",
    "generated": "<ISO-8601>",
    "note_to_authors": "<free text>"
  },
  "fields": {
    "<FIELD_CODE>": { }
  }
}
```

Rules:

1. `_meta.schema_version` is mandatory. Instruments refuse envelopes with a higher major version than they implement.
2. Field codes are UPPERCASE, case-sensitive, and defined by the instrument's published schema — never invented ad hoc.
3. Unknown field codes are ignored on import (forward compatibility) but never silently dropped on re-export.
4. The envelope carries **data and rationale**, never presentation. Rendering is the instrument's job.

---

## 2. Field types

### 2.1 Text

```json
"CLIENT_NAME": { "value": "…", "confidence": "B", "note": "…" }
```

### 2.2 Single-select (enum)

```json
"STRAT_DIRECTION": { "value": "organic_growth", "confidence": "B", "note": "…" }
```

`value` must be one of the schema's enum keys for that field. Free text in an enum field is a validation error.

### 2.3 Likert (integer scale)

```json
"CHANGE_TOLERANCE": { "value": 3, "confidence": "C", "note": "…" }
```

`value` is an integer within the schema-declared range — never a string, never a float.

### 2.4 Multi-select

```json
"REGULATORY_FRAMES": { "values": ["gdpr", "sectoral"], "confidence": "A", "note": "…" }
```

`values` is always an array of enum keys, even for a single selection. An optional `per_option` map may carry per-key confidence:

```json
"CRITICAL_PROCESSES": {
  "values": ["3.0", "7.0"],
  "per_option": { "3.0": "A", "7.0": "C" },
  "note": "…"
}
```

### 2.5 Vector (Ambition Vector)

```json
"AMBITION_VECTOR": {
  "sustain": 55, "scale": 35, "shift": 10,
  "confidence": "B", "note": "…"
}
```

Three integers, **sum exactly 100**, **no component 0** (see D2 discipline rules). Instruments must auto-normalize interactive input and refuse imports that violate the invariants.

### 2.6 Skips

A field the dossier could not address is either omitted or carried with `"confidence": "X"` and no `value`. Instruments render X-fields as open questions, never as empty answers.

---

## 3. Evidence Grades

The four-grade vocabulary is uniform across dossier, prefill, instruments, and facilitation:

| Grade | Meaning | Session behavior |
|---|---|---|
| **A** | strong, verifiable evidence (capital-allocation tier or better) | defend; demand counter-evidence before yielding |
| **B** | multi-source plausibility | present as starting point; expect adjustment |
| **C** | weak or single-source signal | present tentatively |
| **X** | no evidence | pure question — ask in session |

Grades attach to fields (`confidence`), to hypotheses (dossier lines), and to facilitation notes. Grade semantics must never be re-mapped per instrument.

---

## 4. The rationale contract

**Every graded hypothesis carries its reasoning, and the reasoning travels losslessly.**

1. In the MD artifact (dossier / hypothesis pack), each hypothesis line is followed by a `Rationale:` line.
2. On conversion to JSON, the rationale text becomes the field's `note` — verbatim, minus the label.
3. Instruments render `note` as an **advisor-visible, editable callout** attached to the field.
4. Edits made in-session export back into the JSON `note` — the MD and JSON twins must be reconcilable after the session.

The contract exists because the rationale *is* the hypothesis's audit trail: an unexplained prefill is indistinguishable from a guess.

---

## 5. Margin notes

Facilitator-facing free-text fields attached per instrument screen (not per data field). Purposes: session observations, follow-up prompts, disagreement records.

**Facilitation aggregation rule.** During prefill, the dossier's facilitation section is distributed into margin notes of the relevant screens, each item prefixed with one of three canonical markers:

| Marker | Meaning |
|---|---|
| `Pushback:` | where the room is expected to resist — prepare evidence |
| `Defend hardest:` | the hypothesis most worth defending — yielding it cheaply loses the session's value |
| `Hardest question:` | the question most likely to be dodged — ask it anyway |

Aggregated facilitation notes carry grade `A` by convention (they are advisor instructions, not hypotheses). Margin note numbering is defined by each instrument's schema, not by this standard.

---

## 6. Un-bias enforcement (P5, mechanical form)

The standard encodes the principle: an envelope containing `confidence`, `note`, or facilitation content is an **advisor-side artifact**. Instruments must implement two rendering modes:

- **Advisor mode** — full render: values, grades, callouts, margin notes.
- **Respondent mode** — clean render: no prefilled values, no grades, no callouts. Fields start empty.

Any export intended for participants must pass through respondent mode. Publishing an advisor-mode render to the room is a P5 violation, not a formatting choice.

---

## 7. Validation rules

1. Enum values only from the schema's key list; unknown keys are import errors.
2. Likert values are integers in range.
3. Multi-select `values` is always an array; `per_option` keys must be a subset of `values`.
4. Ambition Vector: integers, sum 100, no zero component.
5. Field codes uppercase, case-sensitive.
6. `confidence` only from {A, B, C, X}.
7. `note` is plain text (no markup contract) and survives round-trips verbatim unless deliberately edited.
8. Instruments must persist in-session state locally (crash-safe) and export the full envelope on demand.

---

## 8. Schema versioning

- The **standard** (this document) and each **instrument schema** version independently; instruments declare both.
- Additive changes (new fields, new enum keys) are minor; anything that changes the meaning or validation of existing data is major.
- Envelopes always record the schema version they were written under; migration on import is explicit, never silent.

## 9. Framework enumerations

Shared enum sets used across instruments and artifacts. Semantics are defined in the owning specs; this section is the authoritative key list.

| Enum | Keys | Owning spec |
|---|---|---|
| **Stakes Ladder** | `S0` negligible · `S1` recoverable · `S2` serious · `S3` critical | D4/D5 (EP-01/E1) |
| **Oversight Modes** | `O1` human decides · `O2` human approves · `O3` human monitors · `O4` autonomous with tripwires | D4/D5 (EP-01/E1) |
| **Action Levels** | `X0` inform · `X1` draft · `X2` act with approval · `X3` act within bounds | D4 §3, D5 Part 2 |
| **Action reversibility** | `reversible` · `compensable` · `irreversible` | D4 §3 |
| **Opportunity archetype** | `automation` · `augmentation` · `analytics` · `generation` · `agent` | D4 pool |
| **Ambition match** | `strong` · `partial` · `none` | D4 §4 |
| **Capacity grade** | `sufficient` · `gap_closable` · `insufficient` | D4 §4 |
| **AI Act class** | `prohibited` · `high_risk_annex_iii` · `high_risk_annex_i` · `transparency_art50` · `minimal` · `not_applicable` | D4 §3 |
| **AI Act role** | `provider` · `deployer` · `both` · `not_applicable` | D4 §3 |
| **Regulatory frames** (`REGULATORY_FRAMES`, multi) | `privacy` · `eu_ai_act_high_risk` · `eu_ai_act_general` · `ai_regulation_other` · `cyber` · `sectoral` · `esg` · `contractual` · `none` | instruments; RF-12, RF-13, RF-53 |
| **Adaptation Ladder** | `A0` no AI · `A1` use · `A2` instruct · `A3` ground · `A4` specialize · `A5` own | D5 (EP-01/E3) |
| **Value class** | `efficiency` · `revenue` · `risk` | D4 (EP-01/E3) |
| **Flow States** | `F1` underwater · `F2` steady · `F3` investing · `F4` compounding | D3 (EP-01/E4) |

Validation additions:

9. `stakes`, `action_level`, `oversight_mode`, `adaptation_rung`, `value_class`, `flow_state`, `ambition_match`, `capacity_grade`, `ai_act_class`, and `ai_act_role` values must come from the enum sets above.
10. Every shortlisted opportunity in an envelope must carry `stakes`, `action_level`, and `oversight_mode`; instruments must refuse a Decide-stage export where any is missing (RF-32 fires otherwise). X2+ opportunities must also carry `action_reversibility` and `tool_reach`.
11. Where `REGULATORY_FRAMES` includes an EU AI Act key (`eu_ai_act_high_risk` / `eu_ai_act_general`), every shortlisted opportunity must carry `ai_act_class` and `ai_act_role` (RF-52 fires otherwise).

---

*AIROI Framework · CC-BY-SA 4.0*
