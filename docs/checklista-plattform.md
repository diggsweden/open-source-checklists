
# Checklista – arbete på kodsamverkansplattform (Git-leverantör)

**Syfte:** Praktiskt stöd för hur organisationen använder Git-plattformar (t.ex. GitHub).

## A. Skapande av repositorier

- [ ] Repositoriet är skapat under rätt organisation/"org".
- [ ] Namnet följer överenskommen namngivningsprincip.
- [ ] Synlighet (public/private) är satt enligt informationsklassning och beslut.
- [ ] Standardfiler (LICENSE, README, .gitignore, ev. CODEOWNERS) är på plats, gärna från mall.
- [ ] CODEOWNERS-fil används för detaljerad beskrivning av underhåll som komplement till README:s Maintainer-sektion (Should use a CODEOWNERS file for granular maintenance descriptions).

## B. Behörigheter och åtkomst

- [ ] Tvåfaktorsautentisering (2FA) eller multifaktorautentisering (MFA) används för att försvåra kontoövertaganden (Must use two-factor authentication (2FA) or multifactor authentication (MFA)).
- [ ] Behörigheter är satta enligt principen om minsta möjliga åtkomst.
- [ ] Merge- och push-rättigheter till specifika brancher är begränsade (Must limit merge and push rights to specific branches).
- [ ] Rollerna (admin, maintainer, write, read) används konsekvent.
- [ ] Externa samarbetspartners har endast nödvändig åtkomst.
- [ ] En regelbunden översyn av behörigheter är planerad/genomförs (Should have a basic knowledge of committers and maintainers, and must do a periodic review of those).

## C. Branch-strategi och ändringsflöde

- [ ] Ändringar i kod görs huvudsakligen via pull/merge requests.
- [ ] Minst en person utöver den som gjort ändringen granskar innan merge.
- [ ] Skyddade brancher (t.ex. main/master) används där det är möjligt.
- [ ] Automatiska tester kopplas till pull requests där det är rimligt.
- [ ] GitHub-workflow eller liknande är diskuterat och dokumenterat där relevant (May discuss your GitHub workflow).

## D. Loggning och spårbarhet

- [ ] Utveckling sker på ett sätt som möjliggör spårbarhet (vem gjorde vad, när).
- [ ] Direkt push till produktionsbranch utan PR undviks.
- [ ] Eventuella undantag från processen dokumenteras och motiveras.

## E. Plattformsbyten

- [ ] Vid byte av Git-leverantör finns plan för migrering av repos.
- [ ] Länkar i andra system (intranät, webb, dataportal) uppdateras.
- [ ] OSPO/it och relevanta funktioner är involverade i planeringen.

## F. Arkivering av projekt

- [ ] Plattformens "Archival"-funktion används vid arkivering (Should use the platform's "Archival" function - becomes read-only).
- [ ] I README anges att projektet inte längre underhålls (Should state in the README that the project is no longer maintained).
- [ ] Projektet arkiveras om det inte finns förvaltare (Should be archived if there are no maintainers).

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md) ← du är här
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)