# Checklista – arbete på kodsamverkansplattform

**Syfte:** Praktiskt stöd för hur organisationen använder kodsamverkansplattformar (GitHub, GitLab, Codeberg/Forgejo) — antingen självdriftade eller som SaaS. *Definition från DIGG-riktlinje §Definitioner.*

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

Den här checklistan är **kanonisk hemvist** för branch protection, behörigheter, 2FA, code review och repository-grundkrav. Andra checklistor länkar hit.

## A. Skapande av repositorier

- [ ] **SKA** — Repositoriet är skapat under rätt organisation/"org".
- [ ] **SKA** — Namnet följer överenskommen namngivningsprincip.
- [ ] **SKA** — Synlighet (public/private) är satt enligt informationsklassning och beslut.
- [ ] **SKA** — Standardfiler (LICENSE, README, .gitignore) är på plats, gärna från [open-source-project-template](https://github.com/diggsweden/open-source-project-template). `.gitignore` täcker språkets/byggsystemets default-output så att genererade artefakter inte versionshanteras. *Källa: OSPS-QA-05.01 (L2).*
- [ ] **BÖR** — CODEOWNERS-fil används för granulär maintenance-beskrivning som komplement till README:s Maintainer-sektion (se [forvaltning §A](checklista-publicering-forvaltning.md#a-beslut-ansvar-och-förvaltare)).

## B. Behörigheter och åtkomst

- [ ] **SKA** — Tvåfaktorsautentisering (2FA/MFA) krävs för alla collaborators som kan ändra repository-inställningar.
- [ ] **SKA** — Behörigheter följer principen om minsta möjliga åtkomst (least privilege).
- [ ] **SKA** — Merge- och push-rättigheter till release-brancher är begränsade.
- [ ] **SKA** — Rollerna (admin, maintainer, write, read) används konsekvent.
- [ ] **SKA** — Externa samarbetspartners har endast nödvändig åtkomst, tidsbegränsad där det är tillämpligt.
- [ ] **SKA** — Periodisk översyn av behörigheter genomförs (rekommenderat: minst halvårsvis).

## C. Branch-strategi, code review och ändringsflöde

- [ ] **SKA** — Branch protection är aktiverad på release-branch(er) (`main`/`master`/`release/*`).
- [ ] **SKA** — Direkt push till release-branch är förhindrad; ändringar går via ändringsförfrågningar (PR/MR).
- [ ] **SKA** — Code review krävs: minst en granskare utöver författaren innan merge.
- [ ] **SKA** — Automatiserade statuskontroller (tester, linters, säkerhetsskanning) måste passera innan merge — eller ha dokumenterat manuellt godkännande.
- [ ] **SKA** — CI är kopplad till ändringsförfrågningar.
- [ ] **BÖR** — Trunk-based eller GitHub-flow är valt och dokumenterat i `CONTRIBUTING.md`.
- [ ] **BÖR** — För GitHub: var medveten om risken med `pull_request_target` i workflows och granska Actions-rättigheter (`permissions:`).

## D. Signering och spårbarhet

- [ ] **SKA** — Release-taggar och release-artefakter signeras (Sigstore/cosign rekommenderas; GPG accepteras). *Källa: OSPS-BR-06.01.*
- [ ] **SKA** — Utveckling sker så att spårbarhet bevaras (vem gjorde vad, när).
- [ ] **SKA** — Eventuella undantag från processen dokumenteras och motiveras.
- [ ] **BÖR** — Signerade commits används där risknivån motiverar det.

## E. Plattformsbyten

- [ ] **SKA** — Vid byte av Git-leverantör finns plan för migrering av repos (ärenden, ändringsförfrågningshistorik, taggar).
- [ ] **SKA** — Länkar i andra system (intranät, webb, dataportal) uppdateras.
- [ ] **SKA** — OSPO/IT och relevanta funktioner är involverade i planeringen.

## F. Arkivering av projekt

- [ ] **SKA** — Plattformens arkiveringsfunktion används (read-only).
- [ ] **SKA** — README anger att projektet inte längre underhålls.
- [ ] **SKA** — Projekt utan förvaltare arkiveras.

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Definitioner (kodsamverkansplattformar)*, *Utveckla*, *Livscykelhantera*
- [OpenSSF OSPS Baseline – Access Control](https://baseline.openssf.org/) — AC-01 till AC-05, BR-06.01
- [OpenSSF Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software) — MFA, code review, signering
- [Standard for Public Code](https://standard.publiccode.net/) — *Maintain version control*, *Require review of contributions*
- [GitHub: Securing your repository](https://docs.github.com/en/code-security)

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md) ← du är här
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
