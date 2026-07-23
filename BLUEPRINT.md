# AIROI Framework — Blueprint (podklad pre tvorbu frameworku)

> **Verzia:** 0.4 · **Jazyk podkladu:** slovenčina (kanonická špecifikácia frameworku bude v angličtine, viď sekcia 8)
> **Status:** založený dokument — z tohto podkladu sa píše framework. Nie je to framework samotný.

---

## 1. Účel a positioning

### Prečo vlastný framework: hodnota uniká, skóre ju nezachráni

AI maturity assessmenty sú komodita. Väčšina končí ako skóre v PDF — a skóre nie je hodnota. Medzi AI ambíciou organizácie a realizovaným returnom je reťazec, v ktorom hodnota uniká na štyroch miestach (**value leaks**):

1. **Leak #1 — nesúlad potenciálu a fitu.** Odporúčania ignorujú, koľko zmeny organizácia chce a unesie: transformačný program pre organizáciu hľadajúcu stabilitu, produktivity-tipy pre organizáciu potrebujúcu zmenu modelu. Potenciál bez fitu = shelfware.
2. **Leak #2 — hodnota bez vlastníka.** "Zlepšite data governance" nie je realizovateľná hodnota. Hodnota sa realizuje len v konkrétnom procese s konkrétnym vlastníkom a konkrétnou bolesťou.
3. **Leak #3 — nadhodnotený fit.** Sebahodnotenie bez verifikácie: respondenti odpovedajú tak, aby dobre vyzerali. Nadhodnotená kapacita = return case postavený na piesku.
4. **Leak #4 — reťazec končí reportom.** Engagement sa uzavrie odovzdaním dokumentu; realizácia sa nemeria, učenie sa nevracia. Najväčší leak zo všetkých.

AIROI je systém na utesnenie týchto štyroch únikov: **kalibrácia ambície pred návrhom** (leak #1), **procesné ukotvenie hodnoty** (leak #2), **red-flag verifikácia fitu** (leak #3), **value chain uzavretý až realizovaným returnom** (leak #4). K tomu pridáva delivery ekonomiku: **advisor ∥ AI co-analyst paralelný pattern** — hlbší return case nestojí viac kalendárneho času.

### Pre koho framework je

**Primárne publikum: poradcovia (advisors)** vedúci AI advisory engagementy. Nie klienti — klient konzumuje realizovaný return, nie framework.

Sekundárne publikum: interné strategy/transformation tímy, ktoré chcú robiť AI value discovery in-house so štruktúrou.

### Vzťah framework ↔ produkt

Framework je **metodika** (hodnotový systém, disciplíny, dátové štandardy, pravidlá). Konkrétny komerčný engagement postavený na frameworku je **produkt** — ten si každý practitioner brandí po svojom. Framework je zámerne brand-neutrálny a nezávislý od akéhokoľvek dodávateľa.

### Jedna veta

> AIROI je otvorený AI Value System: od signálov cez kalibrovanú ambíciu a zmeraný fit až po realizovaný return — s reťazcom, ktorý sa neuzatvára reportom, ale hodnotou.

---

## 2. Naming & branding

### Meno: AIROI (definitívne)

**AI + ROI.** Framework existuje na zodpovedanie otázky, ktorej sa väčšina AI assessmentov vyhýba: *kde AI reálne vracia hodnotu tejto organizácii — a koľko zmeny organizácia unesie, aby sa k nej dostala?* Meno nesie ekonomický záväzok: výstupom nie je skóre, ale obhájiteľný return.

Meno potvrdené ako definitívne (v0.10).

### Naming konvencie komponentov

- **Systémová vrstva** — *AI Value System (AVS)*, *AI Value Chain* (7 aktivít: Sense / Align / Assess / Shape / Decide / Realize / Recalibrate), *Recalibration Loop*, *Return Equation*, *Value Leaks*
- **Disciplíny** — `D1…D5`, menované anglicky: *Evidence & Hypotheses*, *Ambition Calibration*, …
- **Artifacts** — menované výstupom: *Evidence Dossier*, *Hypothesis Pack*, *Decision Report*, *Executive Pre-Read*
- **Pravidlá / katalógy** — *Red-Flag Catalog*, *Evidence Grades*, *Realism Rules*
- Framework dokumenty číslované `NN-nazov.md` (viď sekcia 8)

---

## 3. IP a licenčná mapa

Tri vrstvy, každá s iným režimom. Autoritatívne detaily v [ATTRIBUTIONS.md](ATTRIBUTIONS.md).

### 3a. Vlastné IP frameworku (CC-BY-SA 4.0)

| Komponent | Obsah |
|---|---|
| AI Value System + Value Chain | vrcholový model, 7 aktivít, Return Equation, value leaks, 4 dimenzie, Recalibration Loop |
| Engagement lifecycle | stages, aktéri, quality gates, procesný model |
| Evidence & Hypotheses disciplína | hypotézy s evidence grades, paralelné research streams, časový box syntézy |
| Ambition Vector + inference | Sustain/Scale/Shift kalibrácia, sektorové baselines, 3-tier evidence weighting, discipline rules |
| Realism Rules | penalizačné pravidlá pri nesúlade ambícia × kapacita × investícia |
| Red-Flag Catalog | cross-check pravidlá konzistencie naprieč nástrojmi a dimenziami |
| Un-bias princíp | čistý formulár pre respondenta, prefill len pre poradcu |
| Psychological safety | pravidlá formulácie otázok (pozitívny reframe bez straty analytickej hodnoty) |
| Form data standard | JSON envelope, enum-keyed schéma, rationale kontrakt, margin notes |
| Advisor ∥ co-analyst pattern | paralelné draftovanie return case, implementačný decision tree |
| Process deep-dive instrument | maturity dimenzie + technology deep-dive + pain points + motivations |
| Adoption tiers | odstupňovanie return-confidence engagementu |

### 3b. Adaptované diela

**Žiadne.** Framework aktuálne neobsahuje adaptovaný obsah tretích strán — organizačný capacity assessment v D3 je **AIROI Capacity Model (ACM)**: originálny model ukotvený v NIST AI RMF (public domain), s vlastnými doménami, sub-kapacitami a level statements. CC-BY-SA licencia frameworku je od tohto bodu **voľba autorov**, nie povinnosť zdedená z adaptácie.

### 3c. Referencované externé diela (nezabaľujeme)

- **APQC PCF** — procesná taxonómia. Framework odkazuje na PCF ID-čka, nikdy neredistribuuje obsah PCF. Practitioner si PCF obstará priamo od APQC.
- **Run/Grow/Transform klasifikácia investičného zámeru** — všeobecne rozšírený koncept IT portfólio managementu; Ambition Vector je ním konceptuálne inšpirovaný, osi a kalibračná metóda sú vlastné IP.
- **NIST AI RMF, ISO/IEC 42001, EU AI Act** — referenčné compliance / target-state rámce, budúce mapping targets.

### Červené čiary

1. Nikdy nezabaliť APQC obsah do frameworku.
2. Adaptované diela vždy s atribúciou podľa ich licencie, kým sú odvodené časti vo frameworku.
3. Žiadne klientske dáta, mená osôb, firiem ani produktov z delivery praxe vo framework dokumentoch.
4. Worked examples výhradne s fiktívnymi organizáciami.
5. Štruktúrna inšpirácia inými frameworkami (napr. hodnotový systém / reťazec / dimenzie) nikdy nepreberá ich text, terminológiu ani brand — ITIL je proprietárny (PeopleCert), žiadne „ITIL-based/compatible" claims.

---

## 4. Anatómia frameworku

Kanonická štruktúra: hodnotový systém → principles → value chain → lifecycle → disciplines → roles → artifacts → data standard → measurement → tiers. Štruktúrne inšpirované modernými practice frameworkami (hodnotový systém + reťazec + dimenzie); obsah a formulácie sú vlastné.

### 4.0 AI Value System (AVS) — celkový model

Mytológia frameworku — odpoveď na otázku „ako to celé drží pokope":

```
Signály & Dopyt  →  ┌─────────────── AI VALUE SYSTEM ───────────────┐  →  Realizovaný Return
                    │  Guiding Principles · Governance              │
                    │  AI Value Chain · Disciplíny D1–D5            │
                    │  Recalibration Loop                           │
                    └───────────────────────────────────────────────┘
```

**AI Value Chain — 7 aktivít** (univerzálne slovesá; engagement stages sú ich operatívnou inštanciou):

| Aktivita | Čo sa deje | Inštancia v engagemente |
|---|---|---|
| **Sense** | zber signálov z verejných zdrojov, hypotézy | Stage 0 Groundwork |
| **Align** | kalibrácia ambície s vedením | Stage 1 Alignment Session |
| **Assess** | capability assessment (organizácia + procesy) | Stage 1–2 |
| **Shape** | tvarovanie príležitostí naviazaných na bolesť | Stage 2 + Interim Analysis |
| **Decide** | rozhodnutie s obhájiteľným returnom | Stage 3 Decision Session |
| **Realize** | realizácia — **na strane klienta** | post-engagement (roadmapa) |
| **Recalibrate** | meranie realizovaného returnu, spätná väzba do systému | Retrospective + follow-up |

Kľúčový ťah mytológie: **reťazec nie je uzavretý decision reportom, ale realizovaným returnom.** Realize je aktivita Sponzora; framework ju nedoručuje, ale pripravuje (roadmapa s ownermi, decision tree, quick wins) a meria (Recalibrate). Tým sa AIROI štrukturálne odlišuje od assessmentov, ktoré končia skóre — a tesní value leak #4.

**Return Equation:**

```
Return = Potential × Fit          kde Fit = Ambícia × Kapacita
```

Príležitosť s vysokým potenciálom bez fitu = shelfware (leak #1). Fit bez potenciálu = busywork. Preto D2 (Ambition Calibration) vždy predchádza D4 (Opportunity Discovery) — a preto Realism Rules škrtajú odporúčania, ktoré organizácia neunesie.

**Return ≠ Score.** Maturity skóre je output — medzikrok. Return je outcome. Framework meria skóre výhradne ako vstup do rozhodnutia o returne, nikdy ako deliverable sám o sebe.

**Return co-realization.** Return nie je „dodaný" poradcom — je ko-realizovaný Sponzorom a Lead Advisorom. Engagement bez klientskych rozhodnutí a kapacity produkuje research artifact, nie return.

**Štyri dimenzie.** Každá disciplína sa na organizáciu pozerá cez štyri dimenzie; Red-Flag Catalog stráži konzistenciu naprieč nimi:

| Dimenzia | Čo pokrýva |
|---|---|
| **People & Judgment** | sponsorship, skills, kapacita zmeny, psychologická bezpečnosť |
| **Evidence & Data** | signály, evidence grades, dátová pripravenosť |
| **Processes & Value Streams** | procesné ukotvenie (PCF), bolesti, value streams |
| **Technology & Partners** | tooling, vendori, build/buy/own rozhodnutia |

**Recalibration Loop.** Retrospektíva každého engagementu aktualizuje sektorové baselines, Red-Flag Catalog a opportunity pool. Framework sa učí z vlastného použitia — practitioner s N engagementmi má kalibrovanejší systém než pri prvom.

### 4.1 Guiding principles (7)

1. **Focus on return.** Každá aktivita, otázka a artefakt musia byť vysledovateľné k realizovanému returnu. Ak krok neprispieva k presnosti Potential, Fit alebo k realizácii — škrtni ho. Skóre, dokumenty a stretnutia sú náklady, nie hodnota.
2. **Evidence over opinion.** Dôkazy vážené v 3 úrovniach: *capital allocation* (najťažšia váha — CapEx, M&A, kľúčové hires) > *strategic behavior* (reštrukturalizácie, produktové launche, nové org. jednotky) > *language* (výroky vedenia, PR — najľahšia váha, aspiračná). Presnosť evidencie = presnosť return case.
3. **Hypotheses, not summaries.** Každé tvrdenie nesie evidence grade **A/B/C/X** (A = silný overiteľný dôkaz, B = viaczdrojová plauzibilita, C = slabý/jednozdrojový signál, X = bez evidencie — otázka do session) a musí byť falzifikovateľné. Test každej hypotézy: „čo urobím v session inak, ak platí / neplatí?"
4. **Realism before ambition.** Najprv kalibrovať, koľko zmeny organizácia chce a unesie (Ambition Vector + Realism Rules), až potom navrhovať riešenia. Fit je najdrahšia veličina na omyl — nadhodnotený fit znehodnotí celý return case.
5. **Un-bias by design.** Respondent vidí vždy čistý, nepredvyplnený formulár. Predvyplnenie s evidence grades existuje len na strane poradcu — ako hypotéza na validáciu, nie ako sugescia. Biasovaný vstup = falošný fit = leak #3.
6. **Psychological safety.** Otázky formulované tak, aby respondent mohol povedať pravdu bez straty tváre — pozitívny reframe pri zachovaní analytickej hodnoty interných kódov. Pravda o kapacite je vstupom Return Equation; defenzíva ju skresľuje.
7. **Advisor in the loop.** AI co-analyst draftuje mechanické časti paralelne (skóring, sizing, konzistencia); úsudok, syntéza a return naratív ostávajú u človeka. Co-analyst je formálny aktér procesu, nie sidecar.

### 4.2 Value chain / lifecycle

```
Stage 0 Groundwork → Stage 1 Alignment Session → Interim Analysis
      → Stage 2 Field Sessions → Synthesis (advisor ∥ co-analyst)
      → Stage 3 Decision Session → Retrospective
```

| Stage | Účel | Kľúčový výstup | Príspevok k returnu |
|---|---|---|---|
| **0 — Groundwork** | hypotézy z verejných zdrojov pred prvým kontaktom | Evidence Dossier + Hypothesis Pack | lacné de-riskovanie: evidencia znižuje cenu neskoršieho omylu v P aj F |
| **1 — Alignment Session** | validovať hypotézy s vedením, kalibrovať ambíciu, vybrať procesy a expertov | validovaný Ambition Vector, procesná heat mapa, zoznam Process Experts | fixuje **Fit** — najdrahšiu veličinu na omyl |
| **Interim Analysis** | konsolidácia Stage 1, príprava deep-dive štruktúr | scope Field Sessions (2–4 procesy) | koncentruje kapacitu na procesy s najvyšším P |
| **2 — Field Sessions** | procesná realita s expertmi: bolesti, objemy, dáta, kandidáti príležitostí | process records, opportunity shortlist | kvantifikuje **Potential** v procesnej realite (leak #2 tesnenie) |
| **Synthesis** | paralelné draftovanie: poradca (naratív) ∥ co-analyst (mechanika) | Decision Report draft | zostavuje return case (P × F argument) |
| **3 — Decision Session** | pre-read, diskusia, rozhodnutia, sign-off | schválený report + roadmapa | konvertuje return case na rozhodnutie s vlastníctvom |
| **Retrospective** | extrakcia vzorov do metodiky a opportunity poolu | aktualizované baselines a katalógy | meria realizovaný R; učenie = budúci return |

Po každej session: anonymný feedback formulár (engagement steering + signál pre vývoj metodiky).

### 4.3 Disciplines (5)

| # | Disciplína | Čo robí | Kľúčové mechaniky | Príspevok k Return Equation |
|---|---|---|---|---|
| D1 | **Evidence & Hypotheses** | pre-engagement research z verejných zdrojov | paralelné research streams (finančný / strategický / technologicko-bolestný / stakeholder), evidence grades, time-boxovaná syntéza, falzifikovateľné hypotézy | presnosť vstupov — kvalitná evidencia znižuje neistotu P aj F odhadov |
| D2 | **Ambition Calibration** | Ambition Vector: koľko zmeny organizácia chce a unesie | osi **Sustain / Scale / Shift** (100 bodov), sektorové baselines, evidence tiers, prepojené slidery vo workshop instrumente, defense rules podľa grade, Realism Rules | kalibruje **Fit** (zložku Ambícia) |
| D3 | **Capability Assessment** | zrelosť organizácie (AI praktiky) aj konkrétnych procesov | organizačný AI maturity assessment (8 domén, L0–L3 + N/A) + process deep-dive (maturity dimenzie, technology, pain points, motivations) na PCF-ukotvených procesoch | meria **Fit** (zložku Kapacita) a lokalizuje, kde sa skrýva P |
| D4 | **Opportunity Discovery** | AI príležitosti naviazané na procesnú bolesť | matching proti opportunity poolu; každá príležitosť → konkrétna bolesť → konkrétny krok procesu → konkrétny vlastník | tvaruje **Potential** — hodnotu s vlastníkom a adresou |
| D5 | **Decision Enablement** | konzistencia, syntéza a rozhodnutie | Red-Flag Catalog (cross-checks), advisor ∥ co-analyst paralelné draftovanie, gradient štruktúra reportu (pre-read → findings → support → appendix), implementačný decision tree (provider app / custom SW / own model / no AI) | chráni R pred nekonzistenciou (leak #3) a pripravuje Realize (leak #4) |

### 4.4 Roles (4)

| Rola | Zodpovednosť | Vzťah k returnu |
|---|---|---|
| **Sponsor** | klientská strana: prístup, informácie, účasť, rozhodnutie, sign-off | vlastní **Realize** — return sa realizuje v jeho organizácii |
| **Lead Advisor** | vedie engagement end-to-end, vlastní úsudok a syntézu, facilituje sessions | vlastní return case — jeho presnosť a obhájiteľnosť |
| **AI Co-analyst** | paralelný výskum, prefill, mechanické draftovanie, konzistencia — formálny aktér s vlastnou lane v procese | znižuje náklad na return case (hlbší case bez dlhšieho času) |
| **Process Expert** | expert na konkrétny proces, vstupuje do Field Session vo svojom bloku | ukotvuje P v procesnej realite — bez neho je potenciál fikcia |

### 4.5 Artifacts

| Artifact | Vzniká v | Formát | Hodnotová funkcia |
|---|---|---|---|
| **Evidence Dossier** | Groundwork | MD, sekcie s hypotézami + evidence grades | de-riskuje engagement pred prvým kontaktom |
| **Hypothesis Pack** | Groundwork | MD + JSON pár (lossless zhoda), plní instrumenty na strane poradcu | prenáša evidenciu do sessions bez straty |
| **Session Instruments** | Stage 1/2 | referenčné implementácie: ambition calibration, maturity assessment, process deep-dive (interaktívne formuláre) | štruktúrovaný zber F a P signálov |
| **Assessment Records** | Stage 1/2 | exporty instrumentov (MD/JSON) so skóre, red flags a poznámkami | auditovateľná stopa meraní |
| **Analysis Artifacts** | Interim/Synthesis | číslovaná séria pracovných MD dokumentov | medziprodukty return case |
| **Decision Report** | Synthesis | gradient štruktúra, as-is / to-be / ambícia / príležitosti / roadmapa 0–3–6–12 | **return case** — P × F argument s realizačnou cestou |
| **Executive Pre-Read** | pred Stage 3 | TL;DR | umožňuje Decide bez čítania na mieste |
| **Feedback Records** | po každej session | anonymné formuláre → satisfaction signál | kvalita procesu, steering |
| **Retrospective Notes** | close | vstup do ďalšej iterácie metodiky | kalibrácia systému = budúci return |

### 4.6 Data standard

- **JSON envelope**: `{ "_meta": {...}, "fields": { "<CODE>": {...} } }` — každý instrument číta/zapisuje rovnakú obálku
- **Enum-keyed schéma**: každé pole má definované enum kľúče (nie voľný text), Likert ako integer, multi-select ako pole hodnôt; field kódy definuje data standard (nezávislé od konkrétneho instrumentu)
- **Evidence Grades**: `A` / `B` / `C` / `X` — jednotný slovník naprieč dossier, prefill a facilitáciou
- **Rationale kontrakt**: každá hypotéza v MD nesie zdôvodnenie, ktoré sa 1:1 prenáša do JSON poľa — instrument ho renderuje ako editovateľný callout pre poradcu
- **Margin Notes**: per-obrazovka poznámkové polia pre facilitátora s agregačným pravidlom pre facilitačné hinty (`Pushback:` / `Defend hardest:` / `Hardest question:`); číslovanie definuje schéma, nie spec
- **Ambition Vector**: `{sustain, scale, shift}` — tri inty, súčet 100, žiadna zložka 0

### 4.7 Measurement systems

Merania nie sú deliverables — sú to vstupy Return Equation. Každý systém meria inú zložku:

| Systém | Meria | Škála | Pravidlá |
|---|---|---|---|
| **Ambition Vector** | Fit — zložka Ambícia | 3 zložky, súčet 100 | sektorové baselines ako prior; evidence tiers; Realism Rules (napr. Shift > 30 pri nízkej tolerancii neistoty → presun do Scale); zákaz 0 % a 33/33/33 |
| **Organizačná AI maturity** | Fit — zložka Kapacita (organizácia) | L0–L3 + N/A per sub-praktika | L0 = 0 vstupuje do priemeru (reálna medzera), N/A vyňaté, skip → incomplete signál; per-doména priemer + celkové skóre |
| **Process maturity** | Fit — zložka Kapacita (proces) + lokalizácia P | úrovne per dimenzia + composite tech skóre | maturity dimenzie + technology composite; kritickosť a frekvencia ako kontext |
| **Red flags** | konzistencia meraní (ochrana R) | katalóg pravidiel | deklaratívne cross-check pravidlá; každé pravidlo má trigger, závažnosť a odporúčanú validáciu v session |

### 4.8 Adoption tiers

Tiers odstupňujú **return-confidence**: koľko istoty o P × F si klient kupuje.

| Tier | Return-confidence | Sessions | Stakeholderi |
|---|---|---|---|
| **Pulse** | prvý odhad return potenciálu — smerový signál | Alignment + komprimovaný field blok | do 6 |
| **Case** | plný return case — obhájiteľné P × F s roadmapou | plný lifecycle | do 12 |
| **Launch** | return case + realizačná príprava (business cases, architektúra, backlog, 90-dňový plán) | + extra expert interviews | do 18 |

---

## 5. Zdroje frameworku

Framework je extrahovaný a generalizovaný z **konzultačnej praxe autorov**. Do frameworku vstupuje výhradne *štruktúra a metóda* — nikdy dáta, mená, nástroje ani dokumenty z konkrétnych engagementov. Detailný pracovný inventár zdrojových materiálov je vedený mimo tohto repozitára a nie je súčasťou frameworku.

**Pravidlo migrácie:** každý komponent sa pred vstupom do spec generalizuje (fiktívne príklady, neutrálne názvoslovie, tool-agnostické kroky). Opportunity pool, sektorové baselines a zdrojové playbooky sú vo frameworku definované len ako formáty; ich naplnenie je practitioner-ova konkurenčná výhoda.

---

## 6. Čo framework NIE JE

- **Nie je maturity scorecard.** Skóre je medzikrok merania Fit — nikdy deliverable. Engagement, ktorý skončí skóre, je podľa AIROI nedokončený (leak #4).
- **Nie je certifikačná schéma.** Žiadne "AIROI certified practitioner". Ak by časom vznikol dopyt, rieši sa ako samostatná vrstva mimo core spec.
- **Nie je nástroj.** Formuláre sú *referenčné implementácie* dátového štandardu — practitioner si môže postaviť vlastné, pokiaľ dodrží schému a princípy.
- **Nie je náhrada APQC ani maturity štandardov.** APQC je referencovaná taxonómia; maturity assessment je jedno meranie z viacerých. AIROI je hodnotová vrstva nad nimi: kalibrácia, verifikácia, delivery, realizácia.
- **Nie je AI stratégia in a box.** Framework produkuje return case; rozhodnutia a realizácia ostávajú na klientovi (return co-realization).
- **Nie je viazaný na konkrétny AI tooling stack.** AI Co-analyst je definovaný capability-based (research, prefill, parallel drafting), nie produktovo.

---

## 7. Verzovanie a governance

- **Semver na úrovni frameworku**: v0.x = draft/inkubácia, v1.0 = prvá stabilná špecifikácia (kritérium: všetkých 5 disciplín spísaných + data standard + red-flag katalóg + aspoň 1 kompletný delivery cyklus podľa spec).
- **CHANGELOG.md** — vedený od v0.3.
- **Zmeny cez PR** — maintainer schvaľuje; breaking zmeny data štandardu = major verzia.
- **Verzovanie schémy** nezávisle od frameworku (`schema_version` v `_meta`).
- **Príspevky tretích strán**: CC-BY-SA, DCO-style sign-off (doriešiť pri prvom externom príspevku).

---

## 8. Authoring roadmap

Poradie písania framework dokumentov. Kanonický jazyk: **angličtina** (`spec/`), slovenský derivát v `translations/sk/` po stabilizácii v1.0.

| Poradie | Dokument | Obsah | Závislosti | Náročnosť |
|---|---|---|---|---|
| 1 | `spec/00-ai-value-system.md` | AVS model, AI Value Chain (7 aktivít), Return Equation, value leaks, 4 dimenzie, Recalibration Loop | — | M |
| 2 | `spec/01-principles.md` | 7 guiding principles s rationale a anti-patterns | 00 | S |
| 3 | `spec/02-lifecycle.md` | stages, aktéri, quality gates, feedback slučky, procesný model; mapping stages → value chain | 00, 01 | M |
| 4 | `spec/04-data-standard.md` | JSON envelope, enum schéma, evidence grades, rationale kontrakt, margin notes, verzovanie schémy | 01 | M |
| 5 | `spec/03-disciplines/D1…D5` | 5 disciplín, každá: účel → vstupy → kroky → výstupy → pravidlá → anti-patterns → príspevok k Return Equation | 01, 02, 04 | L (najväčší blok; poradie D2 → D3 → D1 → D4 → D5) |
| 6 | `spec/05-red-flag-catalog.md` | deklaratívny katalóg pravidiel (trigger, severity, session akcia) | 03-disciplines | M |
| 7 | `spec/06-artifacts.md` | artefakty, šablóny, minimálne sety per tier, report gradient | 02, 03 | M |
| 8 | `spec/07-adoption.md` | tiers ako return-confidence, čo klient commituje, quality gates per tier | 02, 06 | S |
| 9 | `spec/08-glossary.md` | slovník pojmov | všetko | S |
| 10 | `reference-implementations/` | instrumenty (3 formuláre) s AIROI vokabulárom a vlastným vizuálom | 04 | M |
| 11 | `translations/sk/` | slovenský derivát | v1.0 spec | M |

Odhad: kroky 1–4 = jeden sústredený blok; krok 5 je gro práce.

---

## 9. Open items

1. ~~**Definitívne meno**~~ — **vyriešené (v0.10)**: AIROI je definitívne meno frameworku.
2. ~~**Pomenovanie tiers**~~ — **vyriešené (v0.11)**: Pulse / Case / Launch — mená hovoria, čo si klient kupuje (pulz → return case → štart realizácie).
3. ~~**Náhrada maturity modelu**~~ — **vyriešené (v0.8)**: AIROI Capacity Model (ACM) — originálny 6-doménový model ukotvený v NIST AI RMF — nahradil adaptovaný assessment. Spec: `spec/03-disciplines/ACM-capacity-model.md`.
4. **Threat/security modul** — či a ako zaradiť AI security assessment vrstvu (kandidáti: OWASP LLM Top 10, MITRE ATLAS ako referencované rámce); rozhodnúť pri písaní D3/D5.
5. **Opportunity pool štruktúra** — formát definovať v D4; seed data ostávajú mimo frameworku.
6. ~~**Return measurement v Recalibrate**~~ — **vyriešené (v0.9, EP-01/E2)**: Acceptance Cards definujú metriku, zmeranú baseline, kill criteria a review interval per opportunity už pri Decide; Recalibrate číta karty a audituje AI Register.
7. **Cost estimation model** — high-level DEV/OPS odhady v D5: definovať štruktúru modelu (ranges, nie point estimates).
8. **AI co-analyst live asistencia** — živý asistent počas Alignment Session (follow-up hinty, live heat mapa): koncept, zatiaľ mimo spec.
9. **Interviewee-mapping** — PCF oblasť × sektor → typické roly na interview; formalizovať v D3.
10. **Mapping na NIST AI RMF / ISO 42001 / EU AI Act** — crosswalk tabuľky ako appendix po v1.0.
11. **Publikačná identita** — pred prepnutím na public zvážiť, pod akou identitou (osobný vs. organizačný účet) framework publikovať.

---

*Tento blueprint je založený dokument AIROI Frameworku. Licencia: CC-BY-SA 4.0 (viď [LICENSE.md](LICENSE.md)). Atribúcie adaptovaných a referencovaných diel: [ATTRIBUTIONS.md](ATTRIBUTIONS.md).*
