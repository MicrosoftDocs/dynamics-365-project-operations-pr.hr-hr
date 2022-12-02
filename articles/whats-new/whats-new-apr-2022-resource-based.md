---
title: Novosti u travnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz travnja 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110875"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u travnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.41.0.45
- Upravljanje projektima i računovodstvo u verziji 10.0.26 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Kategorije nabave mogu se koristiti u projektnim narudžbenicama i fakturama dobavljača na čekanju. Za više informacije vidjeti [Korištenje kategorija nabave s projektnim narudžbenicama i fakturama dobavljača na čekanju](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za ožujak 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| -------------- | ------------------- | ------------|
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Ova karta podržava korištenje kategorija nabave s narudžbenicama i fakturama dobavljača na čekanju. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| ------------ | ---------------- | -------------- |
| Vrijeme i trošak | 2573900 | Značajka **Moderno odobrenje** mora biti omogućena prema zadanim postavkama. |
| Naplata i određivanje cijene | 2603313 | Ispravljena je pogreška dupliciranog zapisa koja je sprječavala dodavanje ponuda i redaka ugovora koji sadrže proizvod. |
| Implementacija i konfiguracija | 2611368 | Klijenti moraju moći dodati do pet prilagođenih entiteta u rješenje s pomoću modernog dizajnera aplikacija. |
| Vrijeme i trošak | 2628285 | Riješen je problem koji je utjecao na mogućnost postavljanja ispravne kategorije resursa tijekom uvoza unosa vremena. |
|   Upravljanje prilikama| 2628815 | Ažurirajte ograničenje broja znakova u opisu pojedinosti retka ponude kako bi odgovaralo ograničenju broja znakova predmeta zadatka, tako da uvoz bude uspješan za zadatke u kojima je predmet duži od 100 znakova. |
| Vrijeme i trošak| 2629547 | Polje **Predao** odobrenja projekta mora upućivati na korisnika koji je predao zapisnik. |
| Vrijeme i trošak| 2629865 | Polje **Kopiraj kategoriju** u zadacima kada se projekti kopiraju. |
| Vrijeme i trošak| 2636463 | Ispravljeni filtri u odobrenjima u modernim obrascima odobrenja. |
| Planiranje i praćenje projekta | 2648300 | Riješen je problem koji sprječava promjenu vlasnika projekta. |
| Naplata i određivanje cijene | 2563000 | Reci u dnevniku za nenaplaćenu prodaju u kojima se valuta razlikuje od valute ugovora ne smiju biti dopušteni. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se na platformu Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
