# Checklista – förberedelse inför publicering av öppen programvara

**Syfte:** Säkerställa att öppna projekt är trygga att publicera, begripliga att använda och tydliga för omvärlden.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

**Nästa steg:** När grundkraven är uppfyllda och projektet närmar sig en stabil release — se [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md).

Den här checklistan är **kanonisk hemvist** för Maintainer-deklaration och versionshantering.

## A. Beslut, ansvar och förvaltare

DIGG-riktlinjens ansvarsmodell:

| Roll | Ansvar |
|---|---|
| Avdelnings-/verksamhetsansvarig chef (informationsägare) | Övergripande efterlevnad inom verksamheten |
| Systemägare / verksamhetsansvarig enhetschef | Programvaran hanteras enligt riktlinjen; risker, licenser, beroenden, säkerhet följs upp |
| Operativt team | Dagligt arbete med kod, beroenden, ärenden, externa bidrag, dokumentation |

- [ ] **SKA** — Beslut om publicering är fattat av behörig chef/systemägare (informationsägare).
- [ ] **SKA** — Operativt team är identifierat och informerat. Om projektet berör flera informationsägare är ansvarsfördelningen tydliggjord.
- [ ] **SKA** — Koppling till diariefört ärende (projektnummer, diarienummer) är dokumenterad — se [checklista-diarie-arkiv.md](checklista-diarie-arkiv.md).
- [ ] **SKA** — README innehåller en `## Maintainers`-sektion som anger team, individ eller roll.
- [ ] **SKA** — Programvaran är publikt tillgänglig på Internet **redan under utveckling** (källkod, dokumentation, byggskript). *Källa: DIGG-riktlinje §Utveckla öppen programvara — "Källkod, dokumentation och annan nödvändig information ska successivt göras tillgänglig på vald kodsamverkansplattform."*
- [ ] **SKA** — Ärendehanteraren är publik och påslagen så länge tjänsten är aktivt utvecklad — se [checklista-arenden-community.md §A](checklista-arenden-community.md#a-bevaka-ärenden).
- [ ] **SKA** — Bidragsgivare intygar rätten att bidra — antingen via DCO (Developer Certificate of Origin, signerade commits med `Signed-off-by:`) eller via CLA. *Källa: OSPS-LE-01.01 (L2).*
- [ ] **BÖR** — `CODEOWNERS`-fil används för granulär maintenance-beskrivning — se [checklista-plattform.md §A](checklista-plattform.md#a-skapande-av-repositorier).
- [ ] **BÖR** — Operativa team har grundläggande kunskap om etablerade arbetssätt, säker utveckling och licenshantering. *Källa: DIGG-riktlinje §Utveckla öppen programvara.*

## B. OSS-specifika säkerhetskontroller inför publicering

Allmänna säkerhetskrav (informationsklassning, riskanalys, säker systemutveckling) följer DIGG:s Riktlinje för it-säkerhet och Riktlinje för säker informationshantering. Punkterna nedan är de OSS-specifika kontroller som krävs *innan* källkoden går publik.

- [ ] **SKA** — Koden är granskad så att inga känsliga uppgifter finns kvar (lösenord, API-nycklar, tokens, interna adresser, dokumentlänkar).
- [ ] **SKA** — Loggar, testdata och konfigurationsfiler med känslig information är borttagna eller maskerade.
- [ ] **SKA** — Det är tydligt vad som ska ligga öppet och vad som ska vara internt; informationsklassningen är klar (utförd enligt Riktlinje för säker informationshantering).
- [ ] **SKA** — Code review är gjord — se [checklista-plattform.md §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde).

För djupare OSS-specifika säkerhetskrav se [checklista-sakerhet.md](checklista-sakerhet.md).

## C. Licens och rättigheter

- [ ] **SKA** — Licens är vald enligt DIGG:s riktlinjer och är OSI-godkänd — se [checklista-licenser.md §B](checklista-licenser.md#b-nytt-projekt--val-av-licensmodell).
- [ ] **SKA** — `LICENSE`-fil finns i projektet.
- [ ] **SKA** — Projektet följer [REUSE-specifikationen](https://reuse.software/) — se [checklista-licenser.md §D](checklista-licenser.md#d-copyright-och-märkning-reusespdx).
- [ ] **SKA** — Licenser för beroenden är kontrollerade och dokumenterade.
- [ ] **SKA** — Avstegsbeslut (om proprietär lösning väljs) är godkända av IT-chef och dokumenterade.

## D. Dokumentation och projekthälsa

Enligt DIGG-riktlinjens §*Dokumentation, rutiner och projekthälsa* ska projekten ge en överskådlig bild av vad lösningen gör, hur den används, vilka förutsättningar som gäller och under vilka licensvillkor den tillhandahålls.

- [ ] **SKA** — Titel och beskrivning (vad, för vem, i vilken miljö).
- [ ] **SKA** — `LICENSE` — val av licens som omfattar källkod, dokumentation och övriga delar.
- [ ] **SKA** — Instruktioner för att installera och köra programvaran.
- [ ] **SKA** — Instruktioner för att sätta upp en utvecklingsmiljö och kompilera.
- [ ] **SKA** — Instruktioner för hur externa kan bidra (`CONTRIBUTING.md`).
- [ ] **SKA** — Tillkännagivande av aktörer som bidragit.
- [ ] **SKA** — Uppförandekod (`CODE_OF_CONDUCT.md`) — t.ex. Contributor Covenant.
- [ ] **SKA** — Kontaktväg för frågor och felrapporter (ärenden, mejl, community).
- [ ] **SKA** — Användningsdokumentation och arkitekturbeskrivning relevant för projektet.
- [ ] **SKA** — Designdokumentation som visar systemets aktörer, aktioner och **externa gränssnitt** (så att andra myndigheter kan bedöma återanvändbarhet). *Källa: OSPS-SA-01.01 (L2), OSPS-SA-02.01 (L2); DIGG-policy §Återanvändbarhet.*
- [ ] **BÖR** — Dokumentation skriven i klarspråk och anpassad till bredare målgrupp. *Källa: Standard for Public Code – Use plain language.*

## E. Status, förvaltning och stödfönster

- [ ] **SKA** — Det är tydligt om projektet är aktivt förvaltat eller arkiverat/avslutat.
- [ ] **SKA** — Maturity-status är deklarerad (alpha/beta/stable/deprecated). *Källa: Standard for Public Code – Document maturity.*
- [ ] **SKA** — Det finns en plan för hur inkommande ärenden och ändringsförfrågningar ska hanteras — se [checklista-arenden-community.md](checklista-arenden-community.md).
- [ ] **SKA** — En övergripande strategi för beroendeuppdateringar är beskriven.
- [ ] **SKA** — Det finns en releaseplan med strategier för kommunikation och spridning.
- [ ] **SKA** — Någon är utsedd som ansvarig för säkerhetsärenden — se [checklista-sakerhet.md §D](checklista-sakerhet.md#d-sårbarhetshantering).
- [ ] **BÖR** — Stödfönster ("säkerhetsuppdateringar fram till YYYY-MM-DD") är publicerat. *Källa: OSPS-DO-04.01, OSPS-DO-05.01.*

## F. Publicering

- [ ] **SKA** — Projektnamnet har kontrollerats mot befintliga projekt och varumärken.
- [ ] **SKA** — En sökmotorkontroll har gjorts för att säkerställa att namnet inte krockar.
- [ ] **SKA** — Projektet ligger i rätt organisation/yta hos Git-leverantör.
- [ ] **SKA** — Synlighet (public) är korrekt satt enligt informationsklassning.
- [ ] **SKA** — Eventuell extern kommunikation (webb, dataportal, community) är planerad.

## G. Versionshantering och releaser

- [ ] **SKA** — Projektet använder Semantic Versioning 2.0.0; stabila API:er stöds och deprecation flaggas tidigt.
- [ ] **SKA** — Release-taggar används.
- [ ] **SKA** — Conventional Commits-format används för strukturerad projekthistorik.
- [ ] **SKA** — Keep-A-Changelog-format används för tydlig releasehistorik.
- [ ] **SKA** — Det är lätt för slutanvändare att uppgradera till nya releaser.
- [ ] **SKA** — Releaser signeras och har verifieringsinstruktioner — se [checklista-sakerhet.md §F](checklista-sakerhet.md#f-releaser-och-leveranskedja).

## H. Kvalitet, upptäckbarhet och offentlig kod

- [ ] **SKA** — `publiccode.yml` finns i rotmappen för metadata-indexering och upptäckbarhet (i [Joinup EU-katalogen](https://interoperable-europe.ec.europa.eu/eu-oss-catalogue), [offentligkod.se](https://offentligkod.se), nationella kataloger). *Källa: Standard for Public Code – Make findable.*
- [ ] **BÖR** — Standard for Public Code används som benchmark för kvalitet och hållbarhet.
- [ ] **BÖR** — Projektet är konfigurerbart för olika sammanhang (ingen hårdkodad miljö-/organisationsspecifik information). *Källa: Standard for Public Code – Make codebase reusable and portable.*
- [ ] **BÖR** — Projektets objectives/roadmap är dokumenterade. *Källa: Standard for Public Code – Document codebase objectives.*
- [ ] **BÖR** — Om projektet implementerar regelverk eller policy som kod, är källan till regeln/policyn buntad i repot. *Källa: Standard for Public Code – Bundle policy and source code.*

---

## Källor

- **DIGG: Policy för öppen programvara** (Dnr 2026-02796, beslutad 2026-04-07) — Principer
- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Livscykelhantera*, *Utveckla*, *Publicera*, *Dokumentation, rutiner och projekthälsa*
- [diggsweden/open-source-project-template](https://github.com/diggsweden/open-source-project-template) — implementeringsmall för krav i denna checklista
- [Standard for Public Code](https://standard.publiccode.net/) — *Document maturity*, *Make findable*, *Document codebase objectives*, *Use plain language*, *Make codebase reusable*
- [OpenSSF OSPS Baseline](https://baseline.openssf.org/) — DO-01 till DO-06, GV-01 till GV-04, SA-01, SA-02
- [PublicCode.yml-specifikationen](https://yml.publiccode.tools/)
- [Semantic Versioning 2.0.0](https://semver.org/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Keep a Changelog](https://keepachangelog.com/)
- [Contributor Covenant](https://www.contributor-covenant.org/) — Code of Conduct
- [REUSE Software](https://reuse.software/)

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md) ← du är här
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
