# AIROI Specification 01 — Guiding Principles

> **Status:** Draft · **Spec version:** 0.1 · **Framework:** AIROI
> **License:** CC-BY-SA 4.0 — see [LICENSE.md](../LICENSE.md) · Attributions: [ATTRIBUTIONS.md](../ATTRIBUTIONS.md)

---

## 0. About this document

Seven decision rules that resolve trade-offs the same way every time. When two courses of action both seem defensible, the principles decide. They are ordered: when principles conflict, the lower-numbered one wins.

Each principle is specified as: **statement → rationale → in practice → anti-patterns**.

---

## P1 — Focus on return

**Statement.** Every activity, question, and artifact must trace to a realized return. If a step does not improve the accuracy of Potential, the accuracy of Fit, or the likelihood of realization — cut it.

**Rationale.** Scores, documents, and meetings are costs, not value. The Return Equation (Spec 00 §4) defines the only outcome that counts; everything else is instrumentation. Without this principle, engagements accumulate ritual: assessments for their own sake, reports optimized for thoroughness instead of decisions.

**In practice.**
- Before adding a question to any instrument, name which Return Equation variable it sharpens.
- Before adding a section to any report, name which decision it enables.
- The Decision Report's final section is always *actions with owners*, never a score summary.

**Anti-patterns.**
- *Score worship* — presenting a maturity score as the finding.
- *Completeness theater* — assessing all domains at full depth regardless of relevance.
- *Deliverable inflation* — page count as a proxy for value.

---

## P2 — Evidence over opinion

**Statement.** Weight evidence in three tiers: **capital allocation** (heaviest — CapEx, M&A, key hires) > **strategic behavior** (restructurings, product launches, new organizational units) > **language** (leadership statements, PR — lightest, aspirational).

**Rationale.** Words are cheap; capital is not. Organizations describe themselves aspirationally, and advisors who calibrate on language systematically overestimate the Shift component of ambition. The tier hierarchy is the correction.

**In practice.**
- Every hypothesis in the Evidence Dossier cites its evidence tier alongside its grade.
- When tiers conflict — the CEO announces transformation while CapEx is flat — the higher tier wins and the conflict itself becomes a session question.
- Compliance investment is Sustain evidence, not Shift evidence, no matter how it is announced.

**Anti-patterns.**
- *Ambition inflation* — taking transformation language at face value.
- *Press-release calibration* — building the Ambition Vector hypothesis from marketing copy.
- *Tier flattening* — citing three weak language signals as if they outweighed one capital signal.

---

## P3 — Hypotheses, not summaries

**Statement.** Every claim carries an Evidence Grade — **A** (strong verifiable evidence), **B** (multi-source plausibility), **C** (weak or single-source signal), **X** (no evidence — ask in session) — and must be falsifiable.

**Rationale.** A summary tells the advisor what is known; a hypothesis tells the advisor what to *do*. The test of every dossier line is: *what will I do differently in the session if this is confirmed — or killed?* Claims that fail this test are encyclopedia content, not advisory material.

**In practice.**
- The Evidence Dossier is structured as graded hypotheses, each with a rationale line.
- Grade drives session behavior: **A** — defend, demand counter-evidence before yielding; **B** — present as starting point, expect adjustment; **C** — present tentatively; **X** — pure question.
- Killed hypotheses are recorded, not deleted — a killed hypothesis is calibration data.

**Anti-patterns.**
- *Neutral encyclopedia* — a dossier that describes the organization without committing to anything.
- *Low confidence everywhere* — grading everything C/X to avoid being wrong; commitment is the job.
- *Unfalsifiable claims* — "the organization has digital potential" cannot be killed and therefore teaches nothing.

---

## P4 — Realism before ambition

**Statement.** Calibrate how much change the organization wants and can absorb (Ambition Vector + Realism Rules) *before* designing anything. Fit is the most expensive variable to get wrong.

**Rationale.** The Return Equation multiplies Potential by Fit. An error in Fit invalidates every downstream estimate at once — a roadmap built on overestimated absorption capacity fails wholesale, not marginally. Fit is also cheaper to estimate than Potential (a leadership conversation vs. weeks of field work), so estimating it first is both risk management and economics.

**In practice.**
- *Align* precedes *Assess* and *Shape* in the value chain — always.
- Realism Rules strike or downgrade recommendations that exceed absorption capacity, even when the opportunity is real.
- A Sustain-dominant organization gets a Sustain-compatible roadmap; the advisor does not smuggle Shift items in because they are exciting.

**Anti-patterns.**
- *Fit-blind roadmaps* — sequencing purely by opportunity value.
- *One-size ambition* — recommending the same target state to every client.
- *Ambition flattery* — accepting an inflated self-declared ambition because challenging it is uncomfortable.

---

## P5 — Un-bias by design

**Statement.** Respondents always see clean, unprefilled instruments. Prefilled hypotheses with Evidence Grades exist only on the advisor's side — as material to validate, never as suggestion.

**Rationale.** A prefilled answer anchors the respondent; an anchored respondent confirms rather than reports. Since respondent input feeds Fit, anchoring manufactures the exact defect the framework exists to prevent (leak #3). The same data has two renderings: clean for the room, graded for the advisor.

**In practice.**
- Session instruments render blank for participants; the advisor's copy carries hypotheses, grades, and rationale callouts.
- Presentation materials generated from instruments must not leak hypothesis content.
- The Hypothesis Pack (MD + JSON) is an advisor-side artifact by definition.

**Anti-patterns.**
- *Leading the room* — projecting the advisor's expected answer before the discussion.
- *Prefill leakage* — sending participants "for convenience" a document containing graded hypotheses.
- *Confirmation harvesting* — structuring the session so that agreeing is easier than correcting.

---

## P6 — Psychological safety

**Statement.** Phrase questions so people can tell the truth without losing face. Positive reframing is applied to the wording; the analytical meaning of the underlying codes is preserved.

**Rationale.** The truth about capacity is a Return Equation input; defensiveness distorts it. Respondents in group settings — especially with leadership present — will not volunteer weakness when the question frames weakness as failure. Asking "what would help you accelerate?" retrieves the same information as "what is blocking you?" without triggering defense.

**In practice.**
- Negative framings ("what's failing?", "what will you lose?") are rewritten as opportunity framings ("where is the biggest improvement potential?", "what shouldn't be left unexploited?").
- Internal answer codes keep their analytical meaning — the reframe is presentational, not semantic.
- Feedback after every session is anonymous.

**Anti-patterns.**
- *Interrogation framing* — questions that make honesty feel like confession.
- *Euphemism drift* — softening wording so far the analytical signal is lost (the reframe must preserve the code semantics).
- *Public scoring* — displaying individual maturity answers to the room in a way that shames the low scorer.

---

## P7 — Advisor in the loop

**Statement.** The AI Co-analyst drafts mechanical parts in parallel — research, prefill, scoring, sizing, consistency checks. Judgment, synthesis, and the return narrative stay human.

**Rationale.** The co-analyst makes depth affordable: a sharper return case in the same calendar time. But every mechanism in the framework protects the honesty of judgments, and judgment cannot be delegated to a system with no accountability to the client. The co-analyst is a formal actor with its own lane — visible, auditable, and bounded.

**In practice.**
- The co-analyst runs parallel research streams in *Sense* and drafts the mechanical report sections in *Synthesis* (scoring aggregation, sizing tables, implementation options).
- The Lead Advisor reviews all co-analyst output and owns every claim in the Decision Report.
- Co-analyst capability is defined functionally (research, prefill, parallel drafting, consistency) — never as a specific product.
- The co-analyst runs under explicit operating rules — confidentiality of client data, human verification of sources before Grade A/B, provenance of drafted parts, disclosure to the client (Spec 02 §1).
- The claim that the pattern buys depth without extra time is a hypothesis to measure, not a felt speed-up (Spec 00 §1.3).

**Anti-patterns.**
- *Autopilot advisory* — shipping co-analyst output without advisor judgment.
- *Hidden machine* — using AI assistance while presenting the work as purely human (the lane is formal and disclosed).
- *Tool lock-in* — specifying the co-analyst as a particular vendor's product inside the framework.
- *Laundered citations* — co-analyst-found sources entering the dossier at Grade A/B without a human having opened them.

---

## Conflict resolution

When principles collide, the lower number wins. Two frequent collisions:

- **P1 vs P3:** a hypothesis is interesting but changes no session behavior → P1 cuts it.
- **P6 vs P3:** a falsifiable question is confrontational as phrased → P6 governs the *wording*, P3 governs the *substance*; reframe without losing the code.

---

*AIROI Framework · CC-BY-SA 4.0*
