# Checklista – hantering av ärenden, frågor och externa bidrag

**Syfte:** Stöd för hur team hanterar ärenden (issues), frågor och ändringsförfrågningar (PR/MR) i öppna projekt.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

## A. Bevaka ärenden

- [ ] **SKA** — Ärendehanteraren är publik och påslagen så länge tjänsten är aktivt utvecklad. *Källa: DIGG-riktlinje §Utveckla öppen programvara — "felanmälningar, förbättringsförslag och andra ärenden hanteras strukturerat och synligt så länge projektet är aktivt".*
- [ ] **SKA** — Det finns en överenskommen frekvens för genomgång av ärenden och ändringsförfrågningar (t.ex. veckovis).
- [ ] **SKA** — Nya ärenden kategoriseras (programfel, förbättring, fråga, annat).
- [ ] **SKA** — Nya ärenden får en första återkoppling inom rimlig tid (rekommenderat: ≤ 5 arbetsdagar).
- [ ] **SKA** — Ärenden med potentiella säkerhetsimplikationer hanteras enligt sårbarhetsrutiner (se [checklista-sakerhet.md §D](checklista-sakerhet.md#d-sårbarhetshantering)).

## B. Frågor och kontaktvägar

- [ ] **SKA** — Produkt- och projektrelaterade frågor besvaras av ansvarigt team via ärendehanteraren eller motsvarande.
- [ ] **SKA** — Generella frågor om öppen programvara hänvisas till överenskommen funktion (t.ex. OSPO eller community).
- [ ] **SKA** — Allmänna frågor om organisationens verksamhet hänvisas till ordinarie kontaktvägar (t.ex. info/registrator).
- [ ] **SKA** — Dessa kontaktvägar framgår i README eller dokumentationen.

## C. Externa bidrag (ändringsförfrågningar)

- [ ] **SKA** — Externa ändringsförfrågningar (PR/MR) välkomnas och granskas systematiskt enligt [checklista-plattform.md §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde).
- [ ] **SKA** — Bidrag granskas genom samma flöden som övrig utveckling: granskning, tester, kontroll av beroenden — manuella och automatiserade kvalitetskontroller. *Källa: DIGG-riktlinje §Hantera bidrag till öppna programvaruprojekt.*
- [ ] **SKA** — Tydliga riktlinjer i `CONTRIBUTING.md` avgränsar omfattning och kvalitetskrav. AI-genererade bidrag bedöms på samma grunder som övriga — automatiska kontroller och tydliga ramar är särskilt viktiga. *Källa: DIGG-riktlinje §Hantera bidrag till öppna programvaruprojekt.*
- [ ] **SKA** — Kodkvalitet, stil och testbarhet kontrolleras.
- [ ] **SKA** — Säkerhetspåverkan bedöms (särskilt vid ändringar nära gränssnitt eller behörighetshantering).
- [ ] **SKA** — Licens- och copyrightfrågor för bidraget är godtagbara; bidragsgivare har intygat rätten att bidra (DCO eller CLA).
- [ ] **SKA** — Påverkan på projektets inriktning är bedömd i förhållande till dokumenterade objectives/roadmap.
- [ ] **SKA** — Bidrag kan nekas om de inte följer rutiner, mallar, krav eller bedöms passa projektets riktning. Avslag kommuniceras respektfullt och begripligt.
- [ ] **BÖR** — Contributor Covenant eller motsvarande uppförandekod används.

## D. Avslutade/arkiverade projekt

- [ ] **SKA** — Om projektet inte längre förvaltas aktivt är detta tydligt i README.
- [ ] **SKA** — Projektet är markerat som arkiverat eller liknande i plattformen.
- [ ] **SKA** — Öppna ärenden och ändringsförfrågningar hanteras (stängs eller kommenteras) med motivering.

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Utveckla öppen programvara*, *Hantera bidrag till öppna programvaruprojekt*
- [Contributor Covenant](https://www.contributor-covenant.org/) — uppförandekod
- [OpenSSF OSPS Baseline](https://baseline.openssf.org/) — VM-04.01, GV-03.01
- [Standard for Public Code](https://standard.publiccode.net/) — *Welcome contributors*, *Make contributing easy*

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md) ← du är här
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
