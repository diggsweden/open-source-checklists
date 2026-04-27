# Checklista – licensval och licenskompatibilitet

**Syfte:** Stöd vid val av licens och hantering av licenser i projekt.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

Den här checklistan är **kanonisk hemvist** för licensval, REUSE/SPDX och kompatibilitetsbedömning.

## A. Bidrag till ett befintligt projekt?

- [ ] **SKA** — Det är identifierat om detta är ett bidrag till ett existerande open source-projekt.
- [ ] **SKA** — Om ja: projektets befintliga licens är känd och bedömd som acceptabel för organisationen. *Källa: DIGG-riktlinje §Licenser och kompatibilitet — "Digg ska i normalfallet följa projektets etablerade licens, så länge den är kompatibel med myndighetens användning och krav."*
- [ ] **SKA** — Eventuella copyleft-effekter är genomtänkta (påverkan på organisationens användning).

## B. Nytt projekt – val av licensmodell

DIGG-riktlinjen säger att licensvalet ska göras utifrån projektets syfte — *"ibland är det viktigast att säkerställa att vidareutveckling förblir öppen, ibland att möjliggöra både öppen och sluten vidareutveckling"*. Den här checklistans rekommendationer:

1. **När vidareutveckling ska förbli öppen** (typiskt plattform/infrastruktur): copyleft-licens — i prioriteringsordning **EUPL 1.2**, GPL-3.0, AGPL-3.0.
2. **När både öppen och sluten vidareutveckling ska tillåtas**: tillåtande licens — MIT eller Apache License 2.0.

- [ ] **SKA** — Ställning har tagits till om vidareutveckling ska "tvingas" vara öppen (copyleft) eller få vara både öppen och sluten.
- [ ] **SKA** — Vald licens är OSI-godkänd (se [opensource.org/licenses](https://opensource.org/licenses)).
- [ ] **BÖR** — För plattform/infrastruktur har EUPL 1.2 övervägts (juridiskt bindande på svenska, kompatibel med flera medlemsstaters lagstiftning, hanterar SaaS-distribution).
- [ ] **SKA** — Licensvalet är dokumenterat **innan** utvecklingsarbetet påbörjas.
- [ ] **BÖR** — Juridik/OSPO är konsulterad vid behov.

## C. Beroenden och kompatibilitet

- [ ] **SKA** — Alla tredjepartsbibliotek och beroenden är inventerade med sina licenser.
- [ ] **SKA** — En kompatibilitetsbedömning är gjord (t.ex. copyleft-beroenden vs vald huvudlicens). Verktyg: [Joinup Licence Compatibility Checker](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant).
- [ ] **SKA** — Det är dokumenterat hur tredjeparts licensinformation ska ges (t.ex. NOTICE-fil).
- [ ] **BÖR** — För GPL: version (v2/v3) är aktivt vald och konsekvent.
- [ ] **BÖR** — För AGPL: nätverksklausulens konsekvenser för SaaS-användning är förstådda.

## D. Copyright och märkning (REUSE/SPDX)

- [ ] **SKA** — Projektet följer [REUSE-specifikationen](https://reuse.software/) — varje fil har `SPDX-License-Identifier` och `SPDX-FileCopyrightText`.
- [ ] **SKA** — Projektet har tydliga copyright-angivelser (årtal, organisation, ev. medförfattare).
- [ ] **SKA** — Licensfil (`LICENSE`) finns på rotnivå.
- [ ] **SKA** — `NOTICE`-fil finns där det krävs (t.ex. för Apache 2.0 med tredjepartsattribution).
- [ ] **BÖR** — Projektet strävar efter att uppfylla [ISO/IEC 5230 (OpenChain)](https://www.iso.org/standard/81039.html) för licenshantering där det är rimligt.

## E. Dokumentation och övrigt material

- [ ] **SKA** — Licens för dokumentation, exempel, konfiguration är vald och tydlig.
- [ ] **SKA** — Dokumentation ges ut under en tillåtande licens (t.ex. CC0, CC BY 4.0, CC BY-SA 4.0).

## F. Stöd och eskalering

- [ ] **SKA** — Kontaktväg för licensfrågor (juridik, OSPO) är känd.
- [ ] **SKA** — Beslut om licens är dokumenterat (t.ex. i projektbeskrivning kopplad till diarienummer; se [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md)).

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Licenser och kompatibilitet*
- [Open Source Initiative – Licenser](https://opensource.org/licenses)
- [REUSE Software](https://reuse.software/) — copyright och licensmärkning
- [SPDX License List](https://spdx.org/licenses/)
- [EUPL 1.2 – European Union Public Licence](https://joinup.ec.europa.eu/collection/eupl)
- [Joinup Licence Compatibility Checker](https://joinup.ec.europa.eu/collection/eupl/solution/joinup-licensing-assistant)
- [ISO/IEC 5230 (OpenChain)](https://www.openchainproject.org/) — licensefterlevnadsstandard
- [Creative Commons](https://creativecommons.org/licenses/) — för dokumentation och annat icke-kod-material
- [OpenSSF OSPS Baseline – Legal](https://baseline.openssf.org/) — LE-01.01, LE-02.01, LE-03.01

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md) ← du är här
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
