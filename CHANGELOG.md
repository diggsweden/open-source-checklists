# Changelog

Alla noterbara ändringar dokumenteras i den här filen.

Formatet följer [Keep a Changelog 1.1.0](https://keepachangelog.com/en/1.1.0/) och projektet följer [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- README med rolltabell, statusbadge och referenser till nya DIGG-styrdokumenten.
- `checklista-anvandning.md` — slutanvändarperspektiv.
- Stilkonvention (SKA/BÖR) i alla checklistor.
- "Källor"-sektion i alla checklistor.
- DIGG:s sex principer, två huvudflöden och ansvarsmodell i `checklista-standarder.md`.
- Krav: "öppet redan under utveckling", "ärendehanteraren påslagen under aktiv utveckling", `publiccode.yml` som SKA, document maturity, stödfönster/EOL.
- Säkerhetskrav (OSS-specifika): CVD-tidsfönster, privat rapporteringskanal, release-verifieringsinstruktioner, SBOM levereras med varje release, krypterade kanaler för CI (BR-07.02), genererade artefakter ej i VCS (QA-05.01), designdokumentation av externa gränssnitt som SKA (SA-01.01/SA-02.01).
- Avgränsning mot allmänna säkerhetsdokument: `sakerhet.md` och `forvaltning.md §B` hänvisar nu till Riktlinje för it-säkerhet och Riktlinje för säker informationshantering för generella säkerhetskrav (informationsklassning, riskanalys, hotmodellering). OSS-specifika krav stannar i checklistorna.
- Bidragskrav: DCO eller CLA för inkommande bidrag (LE-01.01), AI-bidragshantering enligt DIGG-riktlinje §Hantera bidrag.
- SfPC: bundle policy and source code som BÖR.
- Community health files för repot självt: `LICENSE` (CC0), `SECURITY.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md`, `CODEOWNERS`, `REUSE.toml`.

### Changed
- Alla DIGG-referenser uppdaterade från 2022-versionen till 2026-04-07-versionen (Policy Dnr 2026-02796, Riktlinje Dnr 2026-02797).
- Inline §-referenser uppdaterade till nya rubriker: *Utveckla öppen programvara*, *Säkerhet genom hela livscykeln*, *Anskaffa öppen programvara*, *Hantera bidrag till öppna programvaruprojekt*, *Dokumentation, rutiner och projekthälsa*, *Licenser och kompatibilitet*, *Livscykelhantera öppen programvara*.
- Interoperabilitetsförordningen uppdaterad från SFS 2018:1486 till EU 2024/903 (refereras explicit i nya DIGG-policyn).
- Kodsamverkansplattformar — `plattform.md` är nu plattformsneutral (GitHub, GitLab, Codeberg/Forgejo) enligt DIGG-riktlinjens definition.
- Avstegsbeslut — formuleringen mjukad från "godkänt av IT-chef" (2022) till "dokumenterad motivering" enligt 2026-riktlinjen.
- Avduplicering: SECURITY-policy kanonisk i `sakerhet.md`, branch protection + 2FA + signering i `plattform.md`, REUSE i `licenser.md`, Maintainer i `forvaltning.md`, code review i `plattform.md`. Övriga checklistor länkar.
- `licenser.md §B` — EUPL 1.2 är nu den här checklistans rekommendation, inte direkt citerad ur riktlinjen (eftersom 2026-riktlinjen lämnar detaljerna till stöddokumenten).
- `forvaltning.md §A` — utökad ansvarsmodell (informationsägare → systemägare → operativt team) enligt 2026-riktlinjen.
- `forvaltning.md §D` — heter nu "Dokumentation och projekthälsa" (tidigare "Dokumentation enligt Bilaga B").
- `arenden-community.md §C` — utökat med AI-bidragshantering enligt 2026-riktlinjen.
- `bidrag-uppstrom.md` — omstrukturerad från `---`-separatorer till `## A. / ## B.` med SKA/BÖR-markörer.
- `diarie-arkiv.md` — stilkonvention applicerad; whitespace städad.
- `publicering-1.0.md` — stack-specifika krav (Java/JS) avgränsade i egen sektion. Conventional Commits flyttad från BÖR till SKA. Stilkonvention dokumenterad.

### Terminology
- Svenska termer enligt DIGG-riktlinje 2026: *ärende* (issue), *ändringsförfrågan* (PR/MR), *programfel* (bug), *programfix* (patch), *ärendehanterare* (issue-tracker). Konsekvent applicerat i alla checklistor, README, CONTRIBUTING, SECURITY.

### Removed
- Engelska "(Must …/Should …)"-citat ur sex filer.
- Döda referenser till `policy2026.md` och `riktlinje2026.md` i `standarder.md`.
- Dubbletter i `forvaltning.md §G` (SemVer två gånger, Keep-A-Changelog två gånger).
- Referenser till "Bilaga A", "Bilaga B" och "Bilaga C" som inte finns i 2026-versionen av riktlinjen.

### Fixed
- Stavfel i `README.md` ("som som").
- Felöversättning i `sakerhet.md §C` ("linter ... upptäcka sårbarheter" — linters upptäcker programfel/stil; SAST/SCA upptäcker sårbarheter).
- Saknade länkar i `anskaffning.md §G` (Inköpsrådet del 2/3/4 — endast del 1 hade URL).
