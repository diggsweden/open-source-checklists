# Översikt – standarder, specifikationer och principer

**Syfte:** Översikt över standarder, specifikationer och ramverk som checklistorna bygger på. För operativa checkpunkter, se respektive checklista.

---

## DIGG:s styrande dokument

Checklistorna konkretiserar och kompletterar:

- **DIGG: Policy för öppen programvara** (Dnr 2026-02796, beslutad 2026-04-07, giltig t.o.m. 2029-03-26)
- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07, giltig t.o.m. 2029-03-06)

Riktlinjen anger explicit att checklistor och mallar ingår som stöddokument: *"Som komplement till riktlinjen finns detaljerade rutiner samt stöddokument – checklistor och mallar som beskriver hur olika moment ska genomföras i praktiken."*

### Sex principer (ur policyn)

1. **Öppenhet** — insyn i tekniska lösningar och processer bygger förtroende. Begränsningar ska bara ske om det krävs av personlig integritet eller säkerhet, och då i nödvändig omfattning.
2. **Återanvändbarhet** — gemensamma investeringar ger effektivitet. Diggs lösningar ska utformas så att de kan återanvändas.
3. **Att bidra** — aktivt deltagande i öppna samarbeten stärker både egen rådighet och offentlig sektor i stort.
4. **Säkerhet** — insyn ökar förmågan att hantera sårbarheter; egen drift minskar sårbarhet i kris; rådighet över koden möjliggör säkerhetsåtgärder över livstiden.
5. **Öppna standarder** — interoperabilitet och minskad inlåsning; frihet att byta leverantörer.
6. **Transformation** — gemensam digital förvaltning kräver öppenhet som grund och ständig förbättring genom delning av kunskap.

### Två huvudflöden + gemensamma ramar (ur riktlinjen)

Riktlinjen beskriver arbetet i två flöden plus gemensamma ramar:

| Flöde | Aktiviteter |
|---|---|
| **Använda och anskaffa** | Livscykelhantera, Anskaffa öppen programvara |
| **Utveckla och publicera** | Livscykelhantera, Utveckla, Publicera, Hantera bidrag |
| **Gemensamma ramar** | Säkerhet genom hela livscykeln, Licenser och kompatibilitet, Dokumentation/rutiner/projekthälsa |

### Ansvarsmodell

- **Avdelnings- och verksamhetsansvarig chef (informationsägare)** — övergripande ansvar för efterlevnad inom den egna verksamheten.
- **Systemägare / verksamhetsansvarig enhetschef** — programvara hanteras enligt riktlinjen; risker, licenser, beroenden, säkerhet följs upp.
- **Operativt team** — dagligt arbete med kod, beroenden, ärenden, externa bidrag, dokumentation.

---

## Licens­specifikationer

**[REUSE-specifikationen](https://reuse.software/)** — tydlig och standardiserad licensefterlevnad.  
→ *Se:* [checklista-licenser.md](checklista-licenser.md), [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

**[ISO/IEC 5230 (OpenChain)](https://www.openchainproject.org/)** — Open Source License Compliance.  
→ *Se:* [checklista-licenser.md](checklista-licenser.md)

**[SPDX (ISO/IEC 5962)](https://spdx.dev/)** — License- och SBOM-format.  
→ *Se:* [checklista-licenser.md](checklista-licenser.md), [checklista-sakerhet.md](checklista-sakerhet.md)

**[EUPL 1.2](https://joinup.ec.europa.eu/collection/eupl)** — European Union Public Licence; juridiskt bindande på svenska, hanterar SaaS, kompatibel med flera medlemsstaters lagstiftning.  
→ *Se:* [checklista-licenser.md](checklista-licenser.md)

---

## Commit och versionshantering

**[Conventional Commits](https://www.conventionalcommits.org/)** — strukturerad projekthistorik.  
→ *Se:* [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

**[Keep a Changelog](https://keepachangelog.com/)** — användarvänlig releasehistorik.  
→ *Se:* [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

**[Semantic Versioning 2.0.0](https://semver.org/)** — konsekvent versionsnumrering.  
→ *Se:* [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

---

## Community och samarbete

**[Contributor Covenant](https://www.contributor-covenant.org/)** — uppförandekod för respektfullt och inkluderande samarbete.  
→ *Se:* [checklista-arenden-community.md](checklista-arenden-community.md)

**[Developer Certificate of Origin (DCO)](https://developercertificate.org/)** — bidragsgivare intygar rätt att bidra.  
→ *Se:* [checklista-bidrag-uppstrom.md](checklista-bidrag-uppstrom.md)

**[TODO Group](https://todogroup.org/)** — OSPO-praxis och policymallar.  
→ *Se:* [checklista-bidrag-uppstrom.md](checklista-bidrag-uppstrom.md)

---

## Säkerhet och kvalitet

**[OpenSSF OSPS Baseline](https://baseline.openssf.org/)** — minimum av säkerhetskontroller på tre mognadsnivåer. (Riktlinjen anger explicit att rekommendationer från OpenSSF ska användas där det är relevant.)  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md), [checklista-plattform.md](checklista-plattform.md), [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

**[OpenSSF Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)** — 29 praktiker för säker mjukvaruutveckling.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md), [checklista-plattform.md](checklista-plattform.md)

**[OpenSSF Scorecard](https://github.com/ossf/scorecard)** — bedöma och förbättra säkerhetshälsa.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[Sigstore](https://www.sigstore.dev/)** — signering av artefakter (cosign) och provenance.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[SLSA](https://slsa.dev/)** — Supply-chain Levels for Software Artifacts.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[ISO/IEC 18974](https://www.iso.org/standard/86529.html)** — Security Assurance.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[ISO/IEC 27001/2](https://www.iso.org/standard/27001)** — informationsklassning och informationssäkerhet.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)** — Application Security Verification Standard. (Riktlinjen anger explicit OWASP som referensram.)  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[OWASP Cheatsheets](https://cheatsheetseries.owasp.org/)** och [OWASP Software Developer Guide](https://owasp.org/www-project-developer-guide/release/).  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[CycloneDX](https://cyclonedx.org/)** — SBOM-format, alternativ till SPDX.  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[SAFECode Fundamental Practices for Secure Software Development](https://safecode.org/publications/)**  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

**[CNCF Security TAG – Software Supply Chain Best Practices](https://github.com/cncf/tag-security/blob/main/supply-chain-security/supply-chain-security-paper/CNCF_SSCP_v1.pdf)**  
→ *Se:* [checklista-sakerhet.md](checklista-sakerhet.md)

---

## Metadata och upptäckbarhet

**[PublicCode.yml-specifikationen](https://yml.publiccode.tools/)** — metadata-indexering för bättre upptäckbarhet.  
→ *Se:* [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md)

**[Standard for Public Code](https://standard.publiccode.net/)** — 16 kriterier för kvalitet och hållbarhet i offentlig kod.  
→ *Se:* [checklista-publicering-forvaltning.md](checklista-publicering-forvaltning.md), [checklista-sakerhet.md](checklista-sakerhet.md), [checklista-arenden-community.md](checklista-arenden-community.md)

---

## Regelverk och förordningar

**[Interoperabilitetsförordningen (EU) 2024/903](https://eur-lex.europa.eu/eli/reg/2024/903/oj)** — EU-förordning om åtgärder för en hög nivå av interoperabilitet i offentlig sektor. Refereras explicit i DIGG:s policy och riktlinje.  
→ *Se:* [checklista-anskaffning.md](checklista-anskaffning.md)

**[European Interoperability Framework (EIF)](https://ec.europa.eu/isa2/eif_en/)** — rekommendationer för interoperabilitet.  
→ *Se:* [checklista-anskaffning.md](checklista-anskaffning.md)

**[SOU 2009:86](https://www.regeringen.se/rattsliga-dokument/statens-offentliga-utredningar/2009/10/sou-200986/)** — Strategi för myndigheternas arbete med e-förvaltning. Definierar öppna standarder för upphandling.  
→ *Se:* [checklista-anskaffning.md](checklista-anskaffning.md)

**[Tryckfrihetsförordningen (1949:105)](https://www.riksdagen.se/sv/dokument-och-lagar/dokument/svensk-forfattningssamling/tryckfrihetsforordning-1949105_sfs-1949-105/)** — allmänna handlingar.  
→ *Se:* [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md)

**[Offentlighets- och sekretesslagen (2009:400)](https://www.riksdagen.se/sv/dokument-och-lagar/dokument/svensk-forfattningssamling/offentlighets--och-sekretesslag-2009400_sfs-2009-400/)**  
→ *Se:* [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md)

**[GDPR / Dataskyddsförordningen](https://www.imy.se/lagar--regler/dataskyddsforordningen/)** — när personuppgifter förekommer i öppen kod, ärenden eller ändringsförfrågningar.  
→ *Se:* [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md), [checklista-sakerhet.md](checklista-sakerhet.md)

---

## Andra DIGG-styrdokument som riktlinjen hänvisar till

- Arbetsordning för Myndigheten för digital förvaltning
- Riktlinje för säker informationshantering
- Riktlinje för it-säkerhet
- Rutiner för hantering av allmänna handlingar

---

## Externa resurser och community

### Utbildning och kunskap

- [opensource.guide](https://opensource.guide) — utbildning i öppen programvara
- [EU-kommissionens Open Source Strategy](https://commission.europa.eu/about-european-commission/departments-and-executive-agencies/informatics/open-source-software-strategy_en) — refereras i policyn

### Svensk offentlig sektor

- [diggsweden/open-source-project-template](https://github.com/diggsweden/open-source-project-template) — implementeringsmall
- [NOSAD (Nätverk för Open Source And Data)](https://nosad.se) — vägledning, mallar, strategiska dokument
  - [NOSAD:s vägledning om upphandling av öppen programvara](https://nosad.se/upphandling-oss)
- [Kammarkollegiets vägledning](https://www.kammarkollegiet.se) — avrop från ramavtalet *Programvaror och tjänster*
- [Inköpsrådets artikelserie](https://inkopsradet.se/upphandling/dela-kostnader-och-undvik-inlasningar/) — upphandling och öppen programvara
- [offentligkod.se](https://offentligkod.se) — katalog över öppna programvaror
- [Sveriges dataportal](https://www.dataportal.se) — community-forum för offentlig sektor

### Internationella resurser

- [EU Open Source Solutions Catalogue](https://interoperable-europe.ec.europa.eu/eu-oss-catalogue)
- [Joinup](https://joinup.ec.europa.eu/) — EU:s plattform för öppen programvara och interoperabilitet
- [Foundation for Public Code](https://www.publiccode.net/)

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md) ← du är här

---

**Senast uppdaterad:** 2026-04-26
