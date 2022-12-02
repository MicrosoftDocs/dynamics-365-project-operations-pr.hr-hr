---
title: Novosti u lipnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz lipnja 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031322"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u lipnju 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.43.0.77 ili 4.43.0.119
- Upravljanje projektima i računovodstvo u verziji 10.0.27 okruženja aplikacije Dynamics 365 Finance

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za lipanj 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| --- | --- | --- |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarjelo naslijeđeno polje i mapirano u novo polje za praćenje stanja fakture dobavljača. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Podugovaranje | 2708885 | Ispravljena je poruka o pogrešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji se može rezervirati gdje nije popunjen nijedan resurs koji se može rezervirati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika pokretanja tijeka rada kako bi se spriječila beskonačna petlja kada se projektni zadaci ažuriraju. |
| Vrijeme i trošak | 2641209 | Uvozi vremenskih unosa iz dodjela/rezervacija moraju zadržati referencu resursa koji se može rezervirati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti zaštićeno.|
| Planiranje i praćenje projekta | 2653145 | Dodane su provjere valjanosti kako bi se osiguralo da se ne može stvoriti zapis projekta koji u nazivu ima nevažeće znakove. |
| Vrijeme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **Odobrenja**. |
| Naplata i određivanje cijene | 2667805 | Dodane su provjere valjanosti kako bi se spriječilo stvaranje stvarnih vrijednosti naplaćene prodaje ako ne postoje pozadinske stvarne vrijednosti nenaplaćene prodaje. |
| Naplata i određivanje cijene | 2668378 | Dodane su provjere valjanosti kako bi se spriječilo dodavanje prilagođene dimenzije cijena osim ako su popunjeni naziv logike i naziv polja. |
| Podugovaranje | 2677485 | Ažurirana je ciljna verzija mape dvostrukog pisanja redaka fakture dobavljača. |
| Vrijeme i trošak | 2700428 | Poboljšana je logika odobrenja kako bi se osiguralo da se drugi skupovi odobrenja za projekt mogu obraditi čak i ako je jedan od skupova odobrenja zapeo u poslovima sustava. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se na platformu Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
