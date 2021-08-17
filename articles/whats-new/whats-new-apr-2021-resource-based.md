---
title: Novosti u travnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju rješenja Project Operations u travnu 2021. godine za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dbce86e88f8315ac4a4957c1128b5619d5328bdbbe27793e161f8f2691899481
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008127"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u travnju 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

- Project Operations u verziji 4.9.0.221 okruženja platforme Dataverse
- Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.17

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Materijali za projekte koji nisu na zalihama. Ključne mogućnosti uključuju:
  - Procjena i određivanje cijene materijala koji nije na zalihama tijekom prodajnog ciklusa za projekt. Dodatne informacije potražite u odjeljku [Postavljanje cijena koštanja i prodaje za kataloške proizvode – osnovno](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Praćenje uporabe materijala koji nisu na zalihama tijekom isporuke projekta. Dodatne informacije potražite u odjeljku [Bilježenje uporabe materijala na projektima i projektnim zadacima](../material/material-usage-log.md).
  - Fakturiranje troškova za upotrijebljen materijal koji nije na zalihama. Dodatne informacije potražite u odjeljku [Upravljanje zaostalim naplatama](../proforma-invoicing/manage-billing-backlog.md).
  - Informacije o načinu konfiguriranja ove značajke potražite u članku [Konfiguriranje materijala koji nije na zalihi i faktura dobavljača na čekanju](../procurement/configure-materials-nonstocked.md)
- Naplata temeljena na zadatku: Dodana je mogućnost povezivanja projektnih zadataka s redcima ugovora o projektu, podvrgavajući ih istom načinu naplate, učestalosti faktura i istim klijentima kao što su oni iz retka ugovora. Ovo pridruživanje osigurava točno fakturiranje, računovodstvo, procjenu prihoda i priznanje za rad u skladu s ovom postavkom na projektnim zadacima.
- Novi API-ji u aplikaciji Dynamics 365 Dataverse omogućuju stvaranje, ažuriranje i brisanje operacija s pomoću značajke **Entiteta za planiranje**. Dodatne informacije potražite u odjeljku [Uporaba API-ja rasporeda za izvođenje operacija s pomoću entiteta planiranja](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za travanj 2021. godine.

| **Karta entiteta** | **Ažurirana verzija** | **Komentari** |
| --- | --- | --- |
| Stvarni podaci o integraciji aplikacije Project Operations (msdyn\_actuals) | 1.0.0.14 | Karta izmijenjena za sinkronizaciju stvarnih podataka o materijalu za projekt. |
| Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn\_estimateslines) | 1.0.0.2 | Dodana je sinkronizacija retka ugovora o projektu s aplikacijama Finance and Operations za podršku naplate koja se temelji na zadacima. |
| Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn\_resourceassignments) | 1.0.0.5 | Dodana je sinkronizacija retka ugovora o projektu s aplikacijama Finance and Operations za podršku naplate koja se temelji na zadacima. |
| Tablica integracije aplikacije Project Operations za procjene materijala (msdyn\_estimatelines) | 1.0.0.0 | Nova karta tablice za sinkronizaciju procjena materijala s platforme Dataverse u aplikacije Finance and Operations. |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nova karta tablice za sinkronizaciju zaglavlja faktura dobavljača iz aplikacija Finance and Operations na platformu Dataverse. |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nova karta tablice za sinkronizaciju redaka fakture dobavljača iz aplikacija Finance and Operations na platformu Dataverse. |

Uvijek trebate pokrenuti najnoviju verziju karte u svom okruženju i omogućiti sve povezane karte tablice dok ažurirate svoje verzije rješenja aplikacije Project Operations platforme Dataverse i aplikacija Finance and Operations. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Novu verziju karte možete aktivirati odabirom **Verzije karte tablice**, odabirom najnovije verzije, a zatim spremanjem odabrane verzije. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations u aplikaciji Dynamics 365 Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2124532 | Gumb **Ispravi fakturu** prikazuje se na predračunu kada iznos zadržanja ili primijenjeni iznos zadržanja postoji na izvornoj fakturi. Gumb se prikazuje samo u okruženjima s verzijom 10.0.19 aplikacije Financije ili novijom. |
| Naplata i određivanje cijene | 2224568 | Dodana je logika za omogućivanje prilagodbi koje uključuju pozivanje dodatka za potvrdu računa. |
| Naplata i određivanje cijene | 2101098 | Poboljšana je logika zadanih polja predračuna: **Adresa naplate**, **Naziv naplate** i **Uvjeti plaćanja** sada se zadaju iz odgovarajućeg zapisa o klijentu u ugovoru o projektu. |
| Naplata i određivanje cijene | 2021413 | Ažurirana su polja **Stvarni trošak** i **Prodaja** na entitetu **Zadatak** kako bi uključivala prodajne vrijednosti iz nenaplaćene i naplaćene troškove za zadatke. |
| Naplata i određivanje cijene | 2182110 | Pri kopiranju ugovora o projektu, ID retka ugovora generira se u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje prilikama | 2186741 | Dodane su provjere valjanosti kako bi se osiguralo da se polja **Podrijetlo** i **Vrsta transakcije** ne može ažurirati s postojećim pojedinostima retka ponude. |
| Upravljanje prilikama | 2191353 | Kontrole točke ne smiju se stvarati na retku ugovora za vrijeme i materijal. |
| Upravljanje prilikama | 2216956 | Ispravljeni su problemi sa značajkom **Ažuriraj cijene**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje redaka procjene troškova s izvornog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje naziva položaja resursa s izvornog projekta. |
| Planiranje i praćenje | 2184799 | Kopija projekta: Pooštrena je kontrola kako bi se osiguralo da se procijenjeni datum početka ne može promijeniti tijekom kopiranja. |
| Planiranje i praćenje | 2185134 | Kopija projekta: Predviđeni datum početka odredišnog projekta postavljen je na današnji datum. |
| Planiranje i praćenje | 2196373 | Kopija projekta: Osigurano je da se zapisi voditelja projekta i članova tima ne dupliciraju u projektnom timu. |
| Planiranje i praćenje | 2211833 | Kopija projekta: Zadaci resursa kopiraju se iz izvornog projektnog zadatka u odredišni projekt. |
| Planiranje i praćenje | 2186541 | Popravljeni su problemi u rešetki **Procjene** do kojih je dolazilo pri grupiranju po resursu. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodjela resursa**. |
| Upravljanje resursima | 2125362 | Ispravljeni su problemi do kojih je dolazilo tijekom stvaranja generičkog člana tima s pomoću načina raspodjele zasnovane na satima. |
| Vrijeme i trošak | 2113603 | Ispravljen je problem povezan s prilagodbom koji je uzrokovao uklanjanje atributa sa stranice **Vremenski unos**. Sustav sada provjerava postoji li atribut na stranici prije nego što im pristupi s pomoću skripte. |
| Vrijeme i trošak | 2204377 | Kopirane vremenske tablice moraju se automatski prikazati kada odaberete **Kopiraj tjedan** tijekom vremenskog unosa. |
| Vrijeme i trošak | 2209059 | Polje **Stanje** može se uređivati za vremenske unose u aplikaciji Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacija stornirane procjene ne radi u odjeljku **Povremeno**.  |
| Upravljanje projektom i računovodstvo | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Značajke **Računovodstvena prilagodba** stvara problem s računima glavne knjige za koje je odabrana značajka **Nemoj dozvoliti ručni unos**. |
| Upravljanje projektom i računovodstvo | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Dodana je poslovna logika za obradu korektivnih faktura, uključujući iznos zadržanja ili primijenjeni iznos zadržanja. |
| Upravljanje projektom i računovodstvo | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Knjiženje vrijednosti WIP-prodaje u fakturiranju projekata unutar tvrtke odabire neočekivani račun. |
| Upravljanje projektom i računovodstvo | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Kada u aplikaciji Project Operations radite s akontacijama, promjena zadanog projekta na ugovoru nakon fakturiranja pretplate uzrokuje probleme s dolaznim odbitcima. |
| Upravljanje projektom i računovodstvo | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Uklanjanjem projekta iz ugovora u aplikaciji Project Operations, trebao bi se vratiti zadani projekt iz ugovora, ako je potrebno. |
| Upravljanje projektom i računovodstvo | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Pogrešni redci troškova u aplikaciji Project Operations prikazuju se na popisu **Dodaj redak** na fakturi među poduzećima unutar tvrtke. |
| Upravljanje projektom i računovodstvo | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Stranica **Kupoprodajni ugovor** u aplikaciji Project Operations nije vidljiva u financijskim pravnim osobama koje su integrirane s aplikacijom Project Operations. |
| Upravljanje projektom i računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Zbog pogreške pri integraciji platforme Dataverse ponudu ne možete pretvoriti u dobivenu u aplikaciji Project Operations. |
| Upravljanje projektom i računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** može postaviti adresu fakture izvora financiranja od drugog klijenta.  |
| Upravljanje projektom i računovodstvo | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | U aplikaciji Project Operations ne odabiru se veličine kada stvarate fakturu za knjiženje za transakciju. |
| Putovanje i trošak | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo gotovinskog predujma ne ažurira se za izvješće o troškovima ako je odobreno i proknjiženo redak po redak. |
| Putovanje i trošak | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Porezi za podrobna izvješća o troškovima među poduzećima unutar tvrtke nisu se pravilno izračunavali. |
| Putovanje i trošak | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Dodatna polja koja se odnose na projekte prikazuju se na ponovno osmišljenoj stranici **Izvješća o troškovima među poduzećima unutar tvrtke**. |
| Putovanje i trošak | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Na zaglavljima izvješća s potvrdama o troškovima prikazuje se netočna poruka o pogrešci. |
| Putovanje i trošak | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Izvješće o troškovima pogrešno se knjižilo u scenariju među poduzećima iste tvrtke ako je porez na promet knjižen u odredišnu pravnu osobu. |
| Putovanje i trošak | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Datumi slanja izvješća ne ispisuju se na odobrenim izvješćima o troškovima. |
| Putovanje i trošak | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Polja **Datum odobren** i **Datum odbijen** ne popunjavaju se nakon odobrenja troškova. |
| Putovanje i trošak | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Putni nalog stvoren za jednog radnika može se upotrijebiti za izvješće o troškovima drugog radnika. |
| Putovanje i trošak | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorije troškova zaključavaju se tijekom dodavanja novog retka troška. |
| Putovanje i trošak | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Preciziranje već podijeljenih redaka izvješća o troškovima dovodi do nepotpunog knjiženja dugovanja \ vaučera Glavne knjige i prekida značajku Istraživanje računovodstvenih izvora jer je duplicirana značajka **TRVEXPTRANS.SOURCEDOCUMENTLINE**. |
| Putovanje i trošak | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Pravila za putne naloge ne funkcioniraju prema očekivanjima. |
| Putovanje i trošak | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Naziv računa dobavljača ne prikazuje se u proknjiženim projektnim transakcijama za izvješća o troškovima. |
| Putovanje i trošak | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | U aplikaciji Project Operations ne možete odobriti vrijeme sa zadatkom za projekt između poduzeća unutar tvrtke. |
| Putovanje i trošak | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategorija povrata gotovinskog predujma ne ažurira salda gotovinskih predujmova kada se knjiže. |
| Putovanje i trošak | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Prodajna cijena netočno se izračunava u izvješćima o troškovima koji su stvoreni u stranoj valuti s pomoću uvezenih transakcija kreditnom karticom i povezani su s projektom. |
| Putovanje i trošak | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Poništavaju se podatkovni entitet **TrvRequisitionLine** i pridruženi jedinstveni indeks. |
| Putovanje i trošak | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Dodan je instrumentarij generiranju **SOURCEDOCUMENTLINE**. |
| Putovanje i trošak | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Prikazivao se pogrešan dnevnik sporedne knjige u scenariju među poduzećima iste tvrtke ako je porez na promet knjižen u odredišnu pravnu osobu. |
| Putovanje i trošak | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Procjene troškova u aplikaciji Project Operations ne brišu se iz financija kad se brišu s platforme Dataverse. |
| Putovanje i trošak | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kada je kategorija troškova kategorija koja nije projekt, financijske veličine odabrane na stranici **Trošak** ne kopiraju se u izvješće o troškovima. |
