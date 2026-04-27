# Checklista – anskaffning och val av öppen programvara

**Syfte:** Stöd för beställare, kravställare och systemägare när öppen programvara övervägs eller väljs.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

## A. Förberedelse – behov och krav

- [ ] **SKA** — Verksamhetsbehovet är beskrivet (vad, för vem, i vilken miljö).
- [ ] **SKA** — Det är tydligt att vid anskaffning av öppen programvara upphandlas tjänster (implementation, support, underhåll, utbildning) — inte själva programvaran som är fritt tillgänglig.
- [ ] **SKA** — Kravställare/beställare föreslår specifik öppen programvara i upphandlingsunderlaget för att underlätta upphandling och undvika inlåsning.
- [ ] **SKA** — Det är känt att organisationen får ställa obligatoriskt krav på specifik namngiven öppen programvara med OSI-godkänd licens vid upphandling (enligt Kammarkollegiets vägledning).
- [ ] **SKA** — Krav på informationssäkerhet är identifierade (informationsklassning).
- [ ] **SKA** — Krav på it-säkerhet är identifierade (loggning, programfixar/patchning, driftmiljö).
- [ ] **SKA** — Krav på interoperabilitet och öppna standarder är formulerade enligt [Interoperabilitetsförordningen (EU) 2024/903](https://eur-lex.europa.eu/eli/reg/2024/903/oj) och European Interoperability Framework (EIF). DIGG:s policy och riktlinje refererar förordningen explicit.
- [ ] **SKA** — Ställning har tagits till om öppen programvara ska vara förstahandsval enligt DIGG:s policy.

## B. Val av projekt/lösning

### Funktionalitet och passform

- [ ] **SKA** — Den öppna lösningen uppfyller centrala funktionella krav.
- [ ] **SKA** — Lösningen kan fungera i organisationens tekniska miljö (plattformar, integrationer).

### Projektets hälsa

- [ ] **SKA** — Projektet uppdateras regelbundet (commits, releaser, ärenden).
- [ ] **SKA** — Det finns en tydlig huvudaktör/organisation bakom projektet.
- [ ] **SKA** — Felrapporter och förbättringsförslag hanteras inom rimlig tid.
- [ ] **SKA** — Projektet har dokumenterad säkerhetshantering (`SECURITY.md`, sårbarhetspolicy).
- [ ] **BÖR** — Projektet redovisar SBOM, releasesignaturer och stödfönster.
- [ ] **BÖR** — OpenSSF Scorecard-poäng eller motsvarande hälsobedömning är granskad.

### Community och governance

- [ ] **SKA** — Det finns en aktiv community/gemenskap kring projektet.
- [ ] **SKA** — Det framgår hur man bidrar (`CONTRIBUTING.md`, governance, code review).

## C. Licens, villkor och ansvar

- [ ] **SKA** — Licensen är identifierad och OSI-godkänd — se [checklista-licenser.md](checklista-licenser.md).
- [ ] **SKA** — Licensen är förenlig med hur organisationen avser att använda programvaran (drift, förändring, ev. egen publicering).
- [ ] **SKA** — Tredjepartslicenser är identifierade och bedömda för kompatibilitet.
- [ ] **SKA** — Det är tydligt att programvaran tillhandahålls "as is" och att kvalitets- och riskansvar ligger hos organisationen.

## D. Säkerhet och drift

- [ ] **SKA** — Det är klarlagt hur sårbarheter och säkerhetsuppdateringar bevakas och hanteras.
- [ ] **SKA** — Det finns stöd för loggning, övervakning och drift i organisationens IT-miljö.
- [ ] **SKA** — Lösningen passar in i organisationens arkitektur (integrationer, beroenden, nätverk).
- [ ] **BÖR** — Total Cost of Ownership (TCO) över livscykeln är skattad.
- [ ] **BÖR** — Exit-/migrationsplan finns även om alternativet är öppen källkod.

## E. Dokumentation av beslut

- [ ] **SKA** — Bedömning och val/avstående är dokumenterat.
- [ ] **SKA** — Om proprietär programvara väljs istället för öppen: beslutet är motiverat och dokumenterat (funktionella, tekniska, säkerhetsmässiga eller ekonomiska skäl).
- [ ] **SKA** — När öppen programvara inte är lämplig eller möjlig finns en dokumenterad motivering (avstegsbeslut). *Källa: DIGG-riktlinje §Anskaffa öppen programvara.*
- [ ] **SKA** — Systemägare/produktägare är utsedd och informerad.
- [ ] **SKA** — Beslutet är diariefört — se [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md).

## F. Upphandlingsregler för öppen programvara

- [ ] **SKA** — Det är känt att Kammarkollegiets ramavtal *Programvaror och tjänster* tillåter obligatoriska krav på specifik namngiven programvara med OSI-godkänd licens som är gratis och fri för alla leverantörer att nyttja.
- [ ] **SKA** — Det är känt att obligatoriska krav på öppna standarder får ställas om standarden uppfyller kraven på en öppen standard enligt SOU 2009:86.

## G. Stöd och vägledning

- [ ] **SKA** — Kammarkollegiets vägledning för avrop från *Programvaror och tjänster* är konsulterad (innehåller fullständigt citat i bilaga "Kravkatalog").
- [ ] **SKA** — [NOSAD:s vägledning om upphandling och öppen källkod](https://nosad.se/upphandling-oss) är konsulterad.
- [ ] **BÖR** — Inköpsrådets artikelserie om upphandling och öppen programvara är konsulterad: [Dela kostnader och undvik inlåsningar](https://inkopsradet.se/upphandling/dela-kostnader-och-undvik-inlasningar/) (del 1).

---

> **Bilaga ur Kammarkollegiets vägledning:**
> Kund får ställa ett obligatoriskt krav på specifik namngiven Programvara som i sin helhet
> - är licensierad med en eller flera licenser godkända av Open Source Initiative (OSI),
> - är gratis och fri för alla leverantörer att nyttja (det krävs ex. ingen återförsäljarstatus).
>
> Kund får ställa obligatoriska krav på standarder om standarden uppfyller kraven på en öppen standard enligt SOU 2009:86.

---

## Källor

- **DIGG: Policy för öppen programvara** (Dnr 2026-02796, beslutad 2026-04-07) — Mål, Principer
- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Anskaffa öppen programvara*, *Livscykelhantera*
- [Kammarkollegiets ramavtal *Programvaror och tjänster*](https://www.kammarkollegiet.se/)
- [NOSAD – Vägledning om upphandling av öppen källkod](https://nosad.se/upphandling-oss)
- [Inköpsrådet – Upphandling och öppen programvara](https://inkopsradet.se/upphandling/dela-kostnader-och-undvik-inlasningar/)
- [Open Source Initiative](https://opensource.org/) — OSI-licenser
- [Interoperabilitetsförordningen (EU) 2024/903](https://eur-lex.europa.eu/eli/reg/2024/903/oj)
- [European Interoperability Framework (EIF)](https://ec.europa.eu/isa2/eif_en/)
- [SOU 2009:86 – Strategi för myndigheternas arbete med e-förvaltning](https://www.regeringen.se/rattsliga-dokument/statens-offentliga-utredningar/2009/10/sou-200986/)
- [OpenSSF's Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)
- [offentligkod.se](https://offentligkod.se) — katalog över öppna programvaror i offentlig sektor

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md) ← du är här
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
