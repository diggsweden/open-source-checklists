# Checklista – använda öppen programvara (slutanvändarperspektiv)

**Syfte:** Stöd för dig som ska *använda* öppen programvara — i drift, i utveckling, eller som beroende. Den här checklistan är inte primärt för dem som *publicerar*; för det, se [förberedelse inför publicering](checklista-publicering-forvaltning.md).

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

## A. Innan du laddar ner

- [ ] **SKA** — Identifiera vilken release-version och vilket repo som är auktoritativt.
- [ ] **SKA** — Kontrollera projektets licens (OSI-godkänd?) och förenlighet med din användning. Se [checklista-licenser.md](checklista-licenser.md).
- [ ] **SKA** — Läs `README.md`, `SECURITY.md` och `CHANGELOG.md`.
- [ ] **BÖR** — Granska projektets `publiccode.yml` om sådan finns.
- [ ] **BÖR** — Kontrollera projektets maturity-status (alpha/beta/stable/deprecated) och deklarerat stödfönster.

## B. Verifiera artefakten

- [ ] **SKA** — Verifiera releasens **integritet** (kontrollsumma) och **äkthet** (signatur).
  - Sigstore/cosign: `cosign verify-blob …`
  - GPG: `gpg --verify <signature> <artefact>`
  - SHA256: jämför mot publicerad checksumma.
- [ ] **SKA** — Granska medföljande **SBOM** (`*.spdx.json` eller `*.cdx.json`) för att förstå sammansättning och beroenden.
- [ ] **BÖR** — Kontrollera projektets [OpenSSF Scorecard](https://scorecard.dev/) eller motsvarande hälsobedömning.

## C. Säkerhet och beroenden

- [ ] **SKA** — Mappa SBOM mot din egen sårbarhetsdatabas (t.ex. OSV.dev, NVD).
- [ ] **SKA** — Bevaka projektets sårbarhetsadvisories (GitHub Security Advisories, CVE-flöden).
- [ ] **SKA** — Etablera rutin för att uppdatera till nya releaser snabbt vid kritiska sårbarheter.
- [ ] **BÖR** — Använd pakethanterare med pinning (lockfiles) för reproducerbara byggen.

## D. Drift och förvaltning

- [ ] **SKA** — Notera projektets **maintenance-status** ("aktivt förvaltat" / "arkiverat" / "no longer maintained"). Vid arkivering — planera ersättning eller fork.
- [ ] **SKA** — Notera deklarerat **stödfönster** (säkerhetsuppdateringar fram till …) och planera uppgradering före utgång.
- [ ] **SKA** — Konfigurera projektet via dokumenterade konfigurationsmekanismer (undvik forks för enkla anpassningar).
- [ ] **BÖR** — Dokumentera internt vilken version och konfiguration som är i drift.

## E. Bidra tillbaka

- [ ] **BÖR** — Rapportera programfel och förbättringsförslag till projektet via dess ärendehanterare. *Källa: DIGG-policy §Att bidra; DIGG-riktlinje §Hantera bidrag till öppna programvaruprojekt.*
- [ ] **BÖR** — Bidra med programfixar enligt [checklista-bidrag-uppstrom.md](checklista-bidrag-uppstrom.md).
- [ ] **BÖR** — Om du forkar långsiktigt — överväg att registrera projektet på [offentligkod.se](https://offentligkod.se) eller i [Joinup](https://joinup.ec.europa.eu/).

## F. Vid problem

- [ ] **SKA** — Sårbarhet upptäckt: rapportera enligt projektets `SECURITY.md` (privat kanal).
- [ ] **SKA** — Programfel eller fråga: använd projektets ärendehanterare.
- [ ] **BÖR** — Om projektet är arkiverat eller övergivet och innehåller sårbarheter — diskutera fork eller ersättning med OSPO/säkerhetsansvarig.

---

## Källor

- **DIGG: Policy för öppen programvara** (Dnr 2026-02796, beslutad 2026-04-07) — *Återanvändbarhet*, *Att bidra*, *Säkerhet*
- [OpenSSF OSPS Baseline](https://baseline.openssf.org/) — DO-03 (verifiera releaser), QA-02 (SBOM), DO-04/05 (stödfönster)
- [OpenSSF's Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)
- [OpenSSF Scorecard](https://scorecard.dev/) — projekthälsa
- [Sigstore](https://www.sigstore.dev/) — verifiera signaturer
- [OSV.dev](https://osv.dev/) — sårbarhetsdatabas
- [Standard for Public Code](https://standard.publiccode.net/) — *Document maturity*

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md) ← du är här
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
