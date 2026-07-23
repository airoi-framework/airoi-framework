# EP-01 — Value Engineering Extension Pack (návrh)

> **Status:** ✅ Accepted & implemented (v0.9) · **Jazyk návrhu:** slovenčina (spec zmeny v angličtine)
> Rozšírenia sú formulované ako originálne AIROI komponenty absorbujúce súčasné priemyselné best practices z AI inžinierstva, AI governance a inžinierskeho manažmentu. Žiadny externý obsah sa nepreberá ani nerefereuje; všetky formulácie sú vlastné.

---

## Prečo tento pack

AIROI v0.8 pokrýva **rozhodnutie** (return case) výborne, ale štyri miesta reťazca sú stále tenké — a všetky štyri ležia medzi *Decide* a *Recalibrate*, teda presne tam, kde tečie leak #4:

1. **Stakes sú spomenuté, nie definované.** D5 hovorí „stakes classified", ale framework nemá škálu ani pravidlo proporcionality kontrol.
2. **Return case nemá definované merania vopred.** Recalibrate agreement existuje, ale bez štruktúry: čo presne sa meria, voči akej baseline, kedy sa opportunity zabíja.
3. **Decision tree je štvorpolievkový.** Provider app / custom / own model / no AI nezachytáva realitu, že medzi „použiť" a „vlastniť" je rebrík s rôznou cenou, kompetenčnými predpokladmi a lock-inom.
4. **Absorpčná kapacita je meraná staticky.** ACM meria prax, ale nie *tok* — tím, ktorý horí v operatíve, neabsorbuje nič bez ohľadu na skóre.

Štyri rozšírenia, každé tesní jedno z týchto miest.

---

## E1 — Stakes Ladder & Oversight Modes

**Posilňuje:** leak #3 (nadhodnotený fit voči riziku) · P4 realizmus · D4/D5

### Stakes Ladder

Štvorstupňová klasifikácia dôsledkov zlyhania AI výstupu — povinný atribút každej shortlistovanej opportunity:

| Stupeň | Meno | Dôsledok chybného/škodlivého výstupu |
|---|---|---|
| **S0** | Negligible | interná nepríjemnosť, okamžite opraviteľná |
| **S1** | Recoverable | viditeľný dopad, plne reverzibilný bežným procesom |
| **S2** | Serious | dopad na zákazníka, financie alebo compliance; náprava drahá |
| **S3** | Critical | nezvratný dopad na osoby, existenčný/regulatórny dopad na organizáciu |

### Oversight Modes

Štyri režimy ľudského dohľadu — druhý povinný atribút opportunity:

| Režim | Meno | Človek… |
|---|---|---|
| **O1** | Human decides | rozhoduje; AI len radí |
| **O2** | Human approves | schvaľuje každý výstup pred účinkom |
| **O3** | Human monitors | dohliada agregovane, zasahuje pri odchýlke |
| **O4** | Autonomous with tripwires | nezasahuje; automatické poistky a eskalácia |

### Pravidlo proporcionality

Minimálny oversight podľa stakes — deklaratívne, vynútiteľné v instrumente:

| Stakes | Minimálny režim |
|---|---|
| S0 | O4 povolené |
| S1 | O3+ |
| S2 | O2+ (O3 len s preukázanou monitoring kapacitou — ACM D6 ≥ 2) |
| S3 | O1/O2; O3+ vyžaduje formálnu výnimku Sponzora zapísanú v Decision Reporte |

### Nový artefakt: AI Register

Handover artefakt pri Decide — inventár schválených AI systémov, ktorý si klient ďalej vedie: opportunity → stakes → oversight mode → owner → review dátum → retirement kritérium. Register je nosič *sunset disciplíny*: každý zápis má dátum revízie a podmienku vyradenia. (Realize prestáva byť čierna skrinka — register je to, čo Recalibrate audituje.)

### Spec dopad

- D4: pool entry formát + shortlist atribúty `stakes`, `oversight_mode`
- D5: proporcionalita ako gate pred sign-off; register v handover kroku
- Spec 04: enumy `S0–S3`, `O1–O4`
- Spec 06: AI Register definícia
- **Nové RF:** RF-31 *stakes-oversight mismatch* (S2/S3 s podlimitným režimom) 🚩 · RF-32 *unclassified stakes* na shortliste 🚩 · RF-33 *autonomy without monitoring* (O3/O4 pri ACM D6 < 2) 🚩

---

## E2 — Acceptance Cards („no eval, no approval")

**Posilňuje:** leak #4 (reťazec končí reportom) · P1 focus on return · D5/Recalibrate

### Princíp

Return nie je merateľný bez definície merania **pred** nasadením. Preto: **žiadna opportunity neprejde cez Decide bez Acceptance Card.** Zrkadlí existujúce pravidlo „no owner, no opportunity" — teraz aj „no measurement, no approval".

### Acceptance Card — štruktúra

Per schválená opportunity, jedna karta:

| Pole | Obsah |
|---|---|
| `success_metric` | čo sa meria (outcome metrika, nie aktivita) |
| `baseline` | hodnota **pred** nasadením — zmeraná, nie odhadnutá |
| `target` | očakávaná hodnota v ranges (žiadna falošná presnosť) |
| `eval_method` | ako sa meria: referenčná sada prípadov / A-B porovnanie / prevádzková metrika |
| `quality_bar` | minimálna kvalita výstupu pre daný stakes stupeň |
| `kill_criteria` | podmienka, pri ktorej sa opportunity zastavuje alebo vracia |
| `review_interval` | kedy Recalibrate meria (nadväzuje na measurement agreement) |

### Kľúčové pravidlá

1. **Baseline pred nasadením.** Bez zmeranej baseline sa return nedá preukázať — nasadenie bez baseline je RF.
2. **Kill criteria sú súčasť schválenia.** Rozhodnutie „kedy to vypneme" sa robí pri Decide, keď je hlava chladná — nie po roku prevádzky, keď je sunk cost горúci.
3. **Referenčná sada prípadov** (zlaté príklady s očakávanými výstupmi) je preferovaný eval_method pre S1+ — buduje sa z reálnych prípadov Process Expertov už počas Field Sessions (lacné, a experti ju aj tak poznajú naspamäť).

### Spec dopad

- D5: Acceptance Card ako gate; Decision Report roadmap items nesú karty
- Spec 06: artefakt definícia + karta v gradient štruktúre (appendix)
- Spec 02: Recalibrate číta karty, nie ad-hoc dohody → open item „return measurement" z blueprintu sa týmto rieši
- **Nové RF:** RF-34 *approval without acceptance card* 🚩 · RF-35 *deployment without baseline* 🚩 · RF-36 *activity metric as success metric* (meria sa použitie, nie outcome) ⚠

---

## E3 — Adaptation Ladder & Unit Economics

**Posilňuje:** D5 decision tree · D4 sizing · Return Equation (P zložka)

### Adaptation Ladder

Existujúci štvorpolievkový decision tree sa nahrádza rebríkom s piatimi priečkami — každá má cenový profil, kompetenčný a dátový predpoklad (previazané na ACM):

| Priečka | Meno | Čo to znamená | Predpoklady (ACM) | Lock-in |
|---|---|---|---|---|
| **A1** | Use | hotová AI schopnosť tak, ako je | D2 ≥ 1 | nízky |
| **A2** | Instruct | prispôsobenie inštrukciami a konfiguráciou | D2 ≥ 1, D4 ≥ 1 | nízky |
| **A3** | Ground | napojenie na vlastné dáta a znalosti | D3 ≥ 2, D4 ≥ 2 | stredný |
| **A4** | Specialize | úprava správania modelu na vlastných dátach | D3 ≥ 2, D4 ≥ 3, D5 ≥ 2 | vysoký |
| **A5** | Own | vlastná AI schopnosť end-to-end | D3 ≥ 3, D4 ≥ 3, D6 ≥ 2 | najvyšší |
| **A0** | No AI | proces redesign alebo štandardný softvér | — | — |

*(A0 ostáva first-class odporúčaním — dôveryhodnosť frameworku stojí na schopnosti povedať „tu AI netreba".)*

### Pravidlo výstupu po rebríku

**Climb on evidence:** začína sa na najnižšej priečke, ktorá podľa Acceptance Card evalu spĺňa quality bar. Vyššia priečka sa odporúča **len** ak nižšia preukázateľne bar nespĺňa — nikdy pre technologickú atraktivitu. (Prepája E2 a E3: eval evidencia je palivo výstupu.)

### Unit economics disciplína

Sizing v D4 sa dopĺňa o jednotkovú ekonomiku:

- **Cost per outcome** — náklad na jednotku výsledku (vybavený prípad, vygenerovaný dokument), nie technický náklad na volanie. Ranges.
- **Trojuholník kvalita × náklad × latencia** — každá opportunity deklaruje, ktorý vrchol je pevný a ktoré dva sa obchodujú.
- **Kaskádový vzor** — kde objem × cena hryzie: lacná cesta rieši bežné prípady, eskalácia drahšej ceste len pre zvyšok; navrhovať pri sizingu, nie po nasadení.
- **Value class** — každá opportunity nesie `value_class`: *efficiency* (šetrí) / *revenue* (zarába) / *risk* (chráni) — portfólio v Decision Reporte ukazuje mix; jednostranné portfólio je signál pre Sponzora.

### Spec dopad

- D5: decision tree sekcia nahradená Adaptation Ladder + climb-on-evidence pravidlo
- D4: sizing rozšírený o unit economics + `value_class`
- Spec 04: enumy `A0–A5`, `value_class`
- **Nové RF:** RF-37 *rung above capacity* (priečka nad ACM predpokladmi) 🚩 · RF-38 *rung above evidence* (vyššia priečka bez eval dôkazu, že nižšia nestačí) ⚠ · RF-39 *single-class portfolio* (všetky opportunities v jednej value class) ℹ

---

## E4 — Flow States & Absorption Rules

**Posilňuje:** Fit (Capacity zložka) · P4 realizmus · leak #1 · D1/D3/roadmapa

### Delivery Flow States

Kapacita nie je len prax (ACM) — je aj **tok**. Tímy, ktoré ponesú realizáciu, sa klasifikujú do štyroch stavov:

| Stav | Meno | Charakteristika | Absorpčná kapacita |
|---|---|---|---|
| **F1** | Underwater | hasenie, práca prichádza rýchlejšie než odchádza | ~nulová |
| **F2** | Steady | drží krok, žiadna rezerva | quick-wins only |
| **F3** | Investing | spláca dlh, buduje si kapacitu | selektívna |
| **F4** | Compounding | zlepšuje sa zrýchľujúco | plná |

### Flow evidence

Stav tímu sa neurčuje pýtaním „ako sa máte", ale **pozorovateľnými tokovými signálmi** — behaviorálna evidencia (tier 2), odolná voči self-scoring flattery:

- ako často tím reálne doručuje zmenu (kadencia),
- ako dlho trvá zmena od rozhodnutia po účinok,
- čo sa deje pri zlyhaní (ako rýchlo sa obnovuje, či sa z neho učí),
- pomer plánovanej vs. vynútenej práce.

Zbiera sa v D1 (verejné signály: releasy, inzeráty na hasičov) a D3 (Field Sessions: priamo od Process Expertov).

### Absorption Rules pre roadmapu

1. **WIP pravidlo:** počet súbežných opportunities v horizonte ≤ počet vlastníkov v stave F3/F4. Ostatné sa **sekvencujú**, nie zoškrtajú.
2. **F1 pravidlo:** tímu v Underwater stave sa nepriraďuje žiadna nová opportunity — prvý roadmap item pre taký tím je *obnova toku* (odstránenie požiarov), ktorá je sama osebe efficiency-class opportunity.
3. **Stakes × flow:** S2/S3 opportunity nesmie niesť tím pod F3.

### Culture texture (mini-sonda)

Doplnok k P6: tri otázky v Field Sessions o toku informácií — *čo sa stane, keď niekto prinesie zlú správu; ako sa dozvedáte, čo robia ostatné tímy; kto je „vinný" pri incidente.* Odpovede sa neškálujú — sú kvalitatívny signál realizačného rizika do Decision Reportu (kultúra, ktorá trestá zlé správy, zabije aj Acceptance Card meranie).

### Spec dopad

- D3: flow states + flow evidence ako tretia sekcia (popri dvoch lens)
- D1: flow signály do research streams (tech-pain stream)
- D5/Spec 06: roadmapa validovaná absorption rules; flow stav owner tímu pri každom roadmap iteme
- Spec 04: enum `F1–F4` per team/owner
- **Nové RF:** RF-40 *roadmap overcommitment* (viac súbežných items než absorbujúcich vlastníkov) 🚩 · RF-41 *underwater assignment* (opportunity na F1 tíme) 🚩 · RF-42 *stakes-flow mismatch* (S2+ na tíme < F3) 🚩

---

## Súhrn dopadov

| Rozšírenie | Nové enumy (Spec 04) | Nové RF | Nový artefakt | Menené specs |
|---|---|---|---|---|
| E1 Stakes & Oversight | S0–S3, O1–O4 | RF-31…33 | AI Register | D4, D5, 04, 05, 06 |
| E2 Acceptance Cards | — (karta = štruktúra) | RF-34…36 | Acceptance Card | D5, 02, 04, 05, 06 |
| E3 Adaptation Ladder | A0–A5, value_class | RF-37…39 | — | D4, D5, 04, 05 |
| E4 Flow & Absorption | F1–F4 | RF-40…42 | — | D1, D3, D5, 04, 05, 06 |

Katalóg RF narastie z 30 na 42 pravidiel. Glossary (Spec 08) sa dopĺňa o ~15 pojmov.

## Poradie implementácie

1. **E1 + E2 spolu** — obe sú gate pri Decide a zdieľajú miesto v D5/Spec 06; E2 zároveň rieši blueprint open item „return measurement v Recalibrate".
2. **E3** — mení D5 decision tree (nahradenie, nie prílepok).
3. **E4** — dotýka sa najviac dokumentov, ale je nezávislé; môže ísť aj paralelne s E3.
4. Instrumenty: Acceptance Card builder ako súčasť budúceho process deep-dive instrumentu alebo samostatný mini-instrument; stakes/oversight/ladder polia do D4-D5 fázy (žiadny existujúci instrument sa nemení).

## Čo zámerne NEpreberáme

- **Žiadne cudzie metriky ani škály menami** — všetko má AIROI mená a definície.
- **Žiadne technologické recepty** (konkrétne architektúry, vendori, modely) — framework ostáva tool-agnostický; Adaptation Ladder popisuje *vzťah k schopnosti*, nie technológiu.
- **Žiadna certifikačná/compliance vrstva** — Stakes Ladder je interná disciplína frameworku; mapping na externé regulatórne kategórie je budúci crosswalk appendix (blueprint open item), nie súčasť core.

---

*AIROI Framework proposal · CC-BY-SA 4.0*
