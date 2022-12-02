---
title: Novosti u veljači 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za veljaču 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932977"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u veljači 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.28.0.120
- Upravljanje projektima i računovodstvo u verziji 10.0.24 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

- Od ovog izdanja možete dodati do 300 članova tima u jedan projekt. Ranije je ograničenje broja članova tima bilo 150. Dodatne informacije potražite u članku [Ograničenja projekta](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeći popis prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za veljaču 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn\_expenses) | 1.0.0.3 | Prošireno za sinkronizaciju projektnih aktivnosti s platformom Dataverse. |

Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2415109 | Zadana vrijednost u polju **Uvjeti plaćanja operacija** mora biti zapis klijenta ugovora o projektu i zapis predračuna. |
| Naplata i određivanje cijene | 2497369 | Ispravak materijala mora slijediti vrijednost datuma u parametrima **Ispravak**. |
| Naplata i određivanje cijene | 2498697 | Poboljšana sigurnosna konfiguracija za **Podsjećanje na unos vremena**. |
| Naplata i određivanje cijene | 2513824 | Za scenarije temeljene na resursima ID kategorije transakcije ne smije premašiti 28 znakova u aplikaciji Project Operations. |
| Naplata i određivanje cijene | 2517455 | Radnja **Osvježi transakcije retka fakture** ne smije se pokretati više puta istovremeno za istu fakturu. |
| Naplata i određivanje cijene | 2517465 | Radnja **Deaktiviraj pojedinosti retka fakture** bokirana je jer nije podržana. |
| Naplata i određivanje cijene | 2556660 | Ispravljene su provjere datuma stupanja na snagu koje se provode na cjeniku koji je priložen uz zapis parametara projekta. |
|   Upravljanje prilikama | 2369202 | Ispravljena je poslovna logika koja potvrđuje da se cjenici koji imaju preklapajuće datume stupanja na snagu mogu priložiti istom projektnom ugovoru. |
|   Upravljanje prilikama | 2385965 | Ispravljeno ponašanje u kartici **Kupci** na stranici **Ugovor o projektu** kada odaberete **Spremi i zatvori**. |
| Vrijeme i trošak | 2538503 | Projektni zadatak mora biti dostupan u entitetu **Stvarne vrijednosti projekta** nakon knjiženja izvješća o troškovima. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Tijekom uvoza odobrenja dobavljača dolazi do pogreške. Poruka o pogrešci glasi: "Iznos zadržavanja ne može biti veći od preostalog neto iznosa." |
| Upravljanje projektom i računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ako prijedlog fakture uključuje transakcije s nultim iznosom naknade koje su nenaplaćene stvarne prodaje, fakturiranje se ne može dogoditi. |
| Upravljanje projektom i računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Knjiženi trošak nije točan nakon ažuriranja nabavne cijene i opcija **Aktiviraj upravljanje promjenama** je omogućena.|
| Upravljanje projektom i računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Procjena knjiženja za projekt s fiksnom cijenom koristi netočnu valutu i iznos u vaučeru procjene, čak i kada je omogućena značajka **Omogući valutu ugovora o projektu za izračun procjene**. |
| Upravljanje projektom i računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_proširenje** ne bi trebalo uputiti poziv za omogućavanje praćenja promjena bez hvatanja iznimaka za entitete koji imaju konfiguracijske ključeve koji nisu omogućeni. |
| Upravljanje projektom i računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Skupni posao je fiksiran kada se objavi više naprednih dnevnika i dođe do pogreške. |
| Putovanje i trošak | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zbog problema s podmirenjem koji se odnosi na predujmove u gotovini u izvješćima o troškovima, iznos poreza nije pokriven kao dio predujma u gotovini. |
| Putovanje i trošak | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Podaci o porezu na promet nisu uključeni u izvješće **Trošak – knjižene transakcije**. |
| Putovanje i trošak | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kršenje pravila o troškovima **Potrebni su računi** netočno prikazuje upozorenje u izvješćima o troškovima. |
| Putovanje i trošak | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Projektna transakcija ne uključuje porez na promet koji se ne može povratiti u ukupni iznos prodaje kada je transakcija rezultat troška kilometraže. |
| Putovanje i trošak | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kada redak stavke ima porez, ne možete promijeniti datum retka stavke i javlja se pogreška stanja izvornog dokumenta. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i zastarjele značajke

Članak [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](removed-depreciated-features-project.md) opisuje značajke koje su uklonjene ili zastarjele za aplikaciju Dynamics 365 Project Operations.

- Značajka uklonjeno više nije dostupna u proizvodu.
- Značajka zastarjelo ne nalazi se u aktivnom razvoju i u nekom budućem ažuriranju može biti uklonjena.

Obavijest o zastarjelosti pojavit će se u članku [Uklonjene ili zastarjele značajke u aplikaciji Project Operations](removed-depreciated-features-project.md) 12 mjeseci prije uklanjanja bilo koje značajke iz proizvoda.

Za prijelomne promjene koje utječu samo na vrijeme kompilacije, ali su binarno kompatibilne sa sigurnim testnim okruženjem i radnim okruženjima, vrijeme zastarjelosti bit će manje od 12 mjeseci. Obično su te promjene funkcionalna ažuriranja koja se moraju izvršiti na kompilatoru.
