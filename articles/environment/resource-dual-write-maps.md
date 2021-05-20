---
title: Verzije karte s dvostrukim pisanjem u aplikaciji Project Operations
description: U ovoj temi nalazi se popis karata s dvostrukim pisanjem koje su potrebne za aplikaciju Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938959"
---
# <a name="project-operations-dual-write-map-versions"></a>Verzije karte s dvostrukim pisanjem u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Uporaba aplikacije Dynamics 365 Project Operations za scenarije resursa / bez zalihe zahtijeva skup karata s dvostrukim upisivanjem koji će se izvršavati u okruženju. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Karte preduvjeta: Rješenje za organizaciju dvostrukog pisanja

Sljedeće su karte preduvjeti rješenje aplikacije Project Operations. Obavezno pokrenite karte navedene u sljedećoj tablici i sve povezane karte tablice u svojem okruženju.

| Karta tablice | Početna sinkronizacija |
| --- | --- |
| Glavna knjiga (msdyn_ledgers) | Zahtijeva početnu sinkronizaciju za kartu tablice i sve preduvjete. Aplikacije Finance and Operations glavne su za početnu sinkronizaciju. |
| Pravne osobe (cdm_companies) | Nije obvezno. Sustav automatski popunjava ovaj entitet kada su okruženja povezana s pomoću dvostrukog pisanja. |
| Klijenti V3 (računi) | Nije potrebno za dodjelu resursa. |
| Dobavljači V2 (msdyn_vendors) | Nije potrebno za dodjelu resursa. |

1. S popisa karata odaberite kartu Glavna knjiga **(msdyn\_ledgers)** sa svim preduvjetima i odaberite potvrdni okvir **Početna sinkronizacija**. U polju **Glavni za početnu sinkronizaciju** odaberite **Aplikacije Finance and Operations** i za kartu glavne knjige i za sve karte preduvjeta. Odaberite **Pokretanje**.

![Sinkronizacija karte knjige](media/DW6.png)

1. Slijedite iste korake za sve preostale karte tablice navedene u gornjoj tablici. Pri pokretanju tih karata nemojte odabrati potvrdni okvir **Početna sinkronizacija**.

## <a name="project-operations-dual-write-maps"></a>Karte s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeće su karte potrebne za rješenje aplikacije Project Operations.

| **Karta entiteta** | **Najnovija verzija** | **Početna sinkronizacija** |
| --- | --- | --- |
| Entitet integracije za odnose projektne transakcije (msdyn\_transactionconnections) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Zaglavlja projektnih ugovora (prodajni nalozi) | 1.0.0.1 | Nije potrebno za dodjelu resursa. |
| Redci ugovora o projektu (pojedinosti prodajnog naloga) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Izvor financiranja projekta (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Nije potrebno za dodjelu resursa. |
| Tablica integracije aplikacije Project Operations za procjene materijala (msdyn\_estimatelines) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Prijedlozi faktura za projekt V2 (fakture) | 1.0.0.2 | Nije potrebno za dodjelu resursa. |
| Stvarni podaci aplikacije Project Operations (msdyn_actuals) | 1.0.0.14 | Nije potrebno za dodjelu resursa. |
| Kontrolne točke retka ugovora za integraciju aplikacije Project Operations (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Nije potrebno za dodjelu resursa. |
| Entitet za integraciju aplikacije Project Operations za procjene troškova (msdyn_estimateslines) | 1.0.0.2 | Nije potrebno za dodjelu resursa. |
| Entitet za integraciju aplikacije Project Operations za procjene sati (msdyn_resourceassignments) | 1.0.0.5 | Nije potrebno za dodjelu resursa. |
| Entitet izvoza kategorija troškova projekta za integraciju aplikacije Project Operations (msdyn_expensecategories) | 1.0.0.2 | Nije potrebno za dodjelu resursa. |
| Entitet izvoza troškova projekta za integraciju aplikacije Project Operations (msdyn_expenses) | 1.0.0.2 | Nije potrebno za dodjelu resursa. |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Uloge resursa za projekt za sve tvrtke (kategorije resursa koji se mogu rezervirati) | 1.0.0.1 | Zahtijeva početnu sinkronizaciju za mapu tablice za sinkronizaciju uloga resursa voditelja projekta i člana tima koji su tijekom dodjele resursa popunjeni u okruženju sustavu Dynamics 365 Dataverse. Dataverse je glavni izvor za početnu sinkronizaciju. |
| Projektni zadaci (msdyn_projecttasks) | 1.0.0.4 | Nije potrebno za dodjelu resursa. |
| Kategorije projektnih transakcija (msdyn_transactioncategories) | 1.0.0.0 | Nije potrebno za dodjelu resursa. |
| Projekti V2 (msdyn_projects) | 1.0.0.1 | Nije potrebno za dodjelu resursa. |

Poduzmite sljedeće korake za pokretanje navedenih karata.

1. Omogućite uloge resursa projekta za kartu tablice **sve tvrtke (kategorije resursa koji se mogu rezervirati)** jer ova karta zahtijeva početnu sinkronizaciju. U polju **Glavni za početnu sinkronizaciju** odaberite **Common data service**. 

 ![Sinkronizacija karte tablice uloge resursa](media/6ResourceInitialSync.jpg)

 Pričekajte dok stanje karte ne postane **Izvršava se** prije nego što prijeđete na sljedeći korak.

2. Odaberite sve preostale potrebne karte. Možete ih filtrirati na popisu karata s dvostrukim pisanjem s pomoću ključne riječi **Projekt** u pretraživanju u gornjem desnom kutu. Možete višestruko odabrati sve karte, a zatim ih pokrenuti. Dodatne informacije potražite u članku [Upravljanje s više karata tablice](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Obvezno omogućite i pokrenite povezane karte entiteta.

### <a name="project-operations-dual-write-map-versions"></a>Verzije karte s dvostrukim pisanjem u aplikaciji Project Operations

Uvijek pokrenite najnoviju verziju karte u okruženju. Određene značajke i mogućnosti možda neće raditi ispravno ako postoji neki od sljedećih uvjeta:

- Nije aktivirana karta.
- Nije aktivirana najnovija verzija karte. 
- Nisu aktivirane povezane karte tablice.

Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Novu verziju karte možete aktivirati odabirom **Verzije karte tablice**, odabirom najnovije verzije, a zatim spremanjem odabrane verzije. Ako ste prilagodili gotovu kartu tablice, morat ćete ponovno primijeniti promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
