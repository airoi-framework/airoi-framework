# Attributions & Licensing Map

AIROI Framework builds on external works in two distinct ways. This document is the authoritative map of what is **referenced** and what is **original**. The framework currently contains **no adapted third-party content** — all instruments and models are original AIROI work.

## 1. Grounding framework

### NIST AI Risk Management Framework (AI RMF 1.0)

- **How we use it:** The **AIROI Capacity Model (ACM)** — the framework's organizational AI capacity model — is original AIROI work *grounded in* the AI RMF: its coverage is cross-walked to the AI RMF functions (GOVERN / MAP / MEASURE / MANAGE) and trustworthiness characteristics so that an ACM assessment supports AI RMF-aligned conversations. No AI RMF text is reproduced; NIST publications are U.S. public domain in any case.
- **Source:** <https://www.nist.gov/itl/ai-risk-management-framework>
- **Note:** Mention of NIST is grounding, not endorsement.

### NIST AI 600-1 — Generative AI Profile

- **How we use it:** As the AI RMF companion profile for generative AI; opportunities of the `generation` and `agent` archetypes are cross-checked against its risk list. No text reproduced (U.S. public domain).
- **Source:** <https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence>

### Agentic AI references (grounding for ACM D7 and the action axis)

- **OWASP Top 10 for Agentic Applications (2026)** and **OWASP Top 10 for LLM Applications (2026)** — external risk catalogs referenced for security assessment of AI that acts (RF-45, RF-46). Not reproduced. <https://genai.owasp.org/>
- **MITRE ATLAS** — adversarial threat landscape for AI systems, incl. agentic techniques; referenced, not reproduced. <https://atlas.mitre.org/>
- **Singapore Model AI Governance Framework for Agentic AI (2026)** — referenced for bounding agent risk through tool access, permissions, and action scope.
- **NIST CAISI AI Agent Standards Initiative (2026)** — tracked for future alignment of agent identity and authorization; no standard published at the time of writing.
- **Note:** Mention is grounding, not endorsement. Versions move quickly; practitioners use the current edition.

## 2. Referenced works (used as external originals — NOT repackaged)

### APQC Process Classification Framework (PCF)

- **How we use it:** As the process taxonomy for process identification, heat-mapping, and deep-dive scoping. AIROI *references* PCF category/process IDs (e.g., "3.0 Market and Sell Products and Services"); it does **not** redistribute or repackage the PCF itself. Practitioners should obtain the PCF directly from APQC.
- **Source:** <https://www.apqc.org/process-frameworks>
- **Rights:** APQC PCF is available from APQC under its own terms (free with registration for internal use). All PCF content remains © APQC.

### Run / Grow / Transform investment classification (concept)

- **How we use it:** AIROI's **Ambition Vector** (Sustain / Scale / Shift) is conceptually related to the run-grow-transform classification of investment intent that is widely used in IT portfolio management. AIROI uses only the generic three-way concept; the axes naming and the entire calibration method built on top (sector baselines, evidence tiers, realism rules, the 100-point session instrument) are original AIROI work.
- **Note:** No proprietary analyst-firm material is included.

### EU AI Act (Regulation (EU) 2024/1689, as amended by Regulation (EU) 2026/1744)

- **How we use it:** As the regulatory frame behind `ai_act_class` / `ai_act_role` (D4 §3), the related Decide gates (D5, RF-50…RF-53), AI literacy (ACM LITERACY_SKILLS), and dated roadmap constraints (D5 Part 4). AIROI's classification is a working assessment for decision purposes, not legal advice. No legal text reproduced.

### ISO/IEC 42001, ISO/IEC 42005, ISO/IEC 42006, EN 18286

- **How we use them:** As referenced standards, not mapped in detail: **ISO/IEC 42001:2023** (AI management system), **ISO/IEC 42005:2025** (AI system impact assessment — relevant where D4/D5 call for impact or fundamental-rights assessment), **ISO/IEC 42006:2025** (requirements for bodies certifying against 42001). **EN 18286** is the first harmonised standard under the EU AI Act (quality management system for providers, Art. 17); it — not ISO/IEC 42001 — gives presumption of conformity for that obligation. No standard text is reproduced. A detailed crosswalk is a post-v1.0 item (BLUEPRINT open item 10).

## 3. Original AIROI Framework work

Everything not listed above is original work by the AIROI Framework contributors, licensed CC BY-SA 4.0, including:

- The staged engagement lifecycle (Groundwork → Alignment → Field → Decision → Retrospective) and its process model
- The Evidence & Hypotheses discipline (hypothesis-driven dossiers, parallel research streams, the Evidence Grade vocabulary `A/B/C/X`)
- The Ambition Vector (Sustain / Scale / Shift) inference method: sector baselines, 3-tier evidence weighting (capital allocation > strategic behavior > language), realism and discipline rules
- The un-bias principle (clean respondent forms; graded prefill on the advisor side only)
- Psychologically safe question design guidelines
- The form data standard: JSON envelope, enum-keyed field schema, rationale contract, facilitator margin notes
- The Red-Flag Catalog (cross-check rules across ambition, capability, investment, and maturity signals)
- The advisor ∥ AI co-analyst parallel report-drafting pattern and its operating rules
- The Return Equation with per-opportunity Fit (ambition match × capacity), the Adaptation Ladder (A0–A5), the action axis (X0–X3), the Stakes Ladder and Oversight Modes with the proportionality rule, Acceptance Cards, and the AI Register
- The AIROI Capacity Model (ACM), including domain D7 Agency & Control
- The process deep-dive instrument (maturity dimensions + technology deep-dive, pain points, motivations)
- Adoption tiers and quality gates
