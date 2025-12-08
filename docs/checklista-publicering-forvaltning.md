
# Checklista – förberedelse inför publicering av öppen programvara

**Syfte:** Säkerställa att öppna projekt är trygga att publicera, begripliga att använda och tydliga för omvärlden.

## A. Beslut och ansvar

- [ ] Beslut om publicering är fattat av behörig chef/systemägare.
- [ ] Förvaltande team är identifierat och informerat.
- [ ] Koppling till diariefört ärende (t.ex. projektnummer, diarienummer) är dokumenterad.
- [ ] Förvaltare/maintainers har utbildning eller erfarenhet av öppen programvara (Must ensure maintainers have education or experience with open source).
- [ ] En Maintainer-sektion finns i README som anger team, individ eller roll (Must include a Maintainer section in every project README).

## B. Informations- och it-säkerhet

- [ ] Koden är granskad så att inga känsliga uppgifter finns kvar (lösenord, API-nycklar, tokens, interna adresser, interna dokumentlänkar m.m.) (Must use secret scanning tools to detect secrets).
- [ ] Loggar, testdata och konfigurationsfiler med känslig information är borttagna eller maskerade.
- [ ] Programvaran är informationsklassad och bedömningen är dokumenterad.
- [ ] Det är tydligt vad som ska ligga öppet och vad som ska vara internt.
- [ ] Projektet har genomgått kodgranskning (Must verify that the project has undergone a code review).

## C. Licens och rättigheter

- [ ] Licens är vald enligt myndighetens policy/riktlinjer (t.ex. EUPL/GPL/AGPL eller MIT/Apache).
- [ ] Licensfil (LICENSE) finns i projektet.
- [ ] Copyright- och licensangivelser är konsekventa (t.ex. enligt REUSE-principer) (License declarations must follow the REUSE licensing specification).
- [ ] Licenser för beroenden/tredjepart är kontrollerade och dokumenterade (Must ensure the project's license doesn't conflict with third-party licenses).

## D. Dokumentation

### Miniminivå

- [ ] README som beskriver syfte, funktion, målgrupp och förutsättningar.
- [ ] Kort beskrivning av hur man installerar, bygger, testar och driftsätter (Should make it easy to use the project - documentation, examples, pre-built releases).
- [ ] Kontaktväg för frågor och felrapporter (issues, mejl, community).
- [ ] Tydlig licensinformation (i README och/eller separat licensfil).
- [ ] Användningsdokumentation och arkitekturbeskrivningar relevanta för projektet (Should include usage documentation and architecture descriptions relevant to the project).

### Vid behov

- [ ] Uppförandekod (Code of Conduct) (Must ensure the project includes standard Community Health Files).
- [ ] CHANGELOG-fil som följer Keep-A-Changelog format (Must ensure the project includes standard Community Health Files - CHANGELOG).
- [ ] Säkerhetspolicy/SECURITY-fil med instruktion för rapportering av sårbarheter (Must have a security policy in place).
- [ ] CONTRIBUTING-fil med riktlinjer för externa bidrag (Must ensure the project includes standard Community Health Files - CONTRIBUTING).

## E. Status och förvaltning

- [ ] Det är tydligt om projektet är aktivt förvaltat eller arkiverat/avslutat (Should state in the README that the project is no longer maintained - vid arkivering).
- [ ] Det finns en plan för hur inkommande issues och pull requests ska hanteras (Must ensure maintainers have a plan for handling merge/pull requests).
- [ ] Det finns en plan för community engagement och hantering av issues (Must ensure maintainers have a plan for community engagement).
- [ ] En övergripande strategi för beroendeuppdateringar är beskriven.
- [ ] Det finns en releaseplan med tydliga strategier för kommunikation och spridning (Should establish a release plan with clear announcement and promotion strategies).
- [ ] Någon är utsedd som ansvarig för säkerhetsärenden (Must ensure someone is responsible for security issues).

## F. Publicering

- [ ] Projektnamnet har kontrollerats mot befintliga projekt och varumärken (Should ensure that the project name does not conflict with an existing project or infringe on trademarks).
- [ ] En sökning har gjorts för att säkerställa att projektnamnet inte krockar (Conduct a general search engine check for the proposed project name).
- [ ] Projektet ligger i rätt organisation/ytor hos Git-leverantör.
- [ ] Synlighet (public/private) är korrekt satt.
- [ ] Eventuell extern kommunikation (webb, dataportal, community) är planerad om relevant.

## G. Versionshantering och releaser

- [ ] Projektet använder Semantic Versioning 2.0.0 för konsekvent versionsnumrering (Should use Semantic Versioning 2.0.0).
- [ ] Release tags används (Should use release tags).
- [ ] Conventional Commits-format används för strukturerad projekthistorik där relevant (Conventional Commits - Provides clear and structured project history).
- [ ] Keep-A-Changelog-format används för att upprätthålla tydlig releasehistorik där relevant (Keep-A-Changelog - Maintains clear and user-friendly release history).
- [ ] Det är lätt för slutanvändare att uppgradera till nya releaser (Should make it easy for end-users to upgrade to new releases).
- [ ] Semantisk versionshantering används, stabila API:er stöds och deprecation flaggas tidigt (Use semantic versioning, support stable APIs, and flag deprecation early).

## H. Kvalitet och standarder för offentlig kod

- [ ] PublicCode.yml har övervägts för metadata-indexering och upptäckbarhet (PublicCode.yml - Facilitates easy metadata indexing for better discoverability).
- [ ] Standard for Public Code har övervägts för att säkerställa kvalitet och hållbarhet (Standard for Public Code - Ensures the project meets criteria for public code quality and sustainability).

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md) ← du är här
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
