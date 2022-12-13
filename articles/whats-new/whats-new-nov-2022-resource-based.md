---
title: Novosti u studenom 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/neutemeljenim resursima u studenome 2022.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831124"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.58.0.119
- Upravljanje projektima i računovodstvo u verziji 10.0.30 okruženja aplikacije Dynamics 365 Finance

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane tablične karte dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2781818 | Pogreška prilikom zadane cijene za zapisnik korištenja materijala nije pronađena ključem. |
| Naplata i određivanje cijene | 2922373 | Nije moguće povezati redak ponude s projektom koji je zatvoren kao izgubljena ponuda. |
| Naplata i određivanje cijene | 2943206 | **Polje Redak** ugovora u entitetu projekta mora biti neobavezno. |
| Naplata i određivanje cijene | 2953182 | Poboljšajte poruku o pogrešci za korektivne fakture.|
| Naplata i određivanje cijene | 2959500 | Nije moguće povezati redak ponude s projektnim zadatkom koji je već povezan s izgubljenom ponudom.|
| Naplata i određivanje cijene | 2959560 | Poruka "Ovaj kupac je već na ugovoru o projektu" primljena je tijekom zatvaranja ponude kao osvojene u određenim regionalnim shemama. |
| Naplata i određivanje cijene | 3031727 | Dodjele resursa ne uspijevaju s pogreškom Obavezno polje 'msdyn_Company'. |
| Naplata i određivanje cijene | 3036905 | Posjedovanje tvrtke nikada nije inicijalizirano na ProjectTeamMember. |
| Upravljanje prilikama | 2763519 | Pogreška Null Reference u odjeljku EnsureProjectContractAllowsUpdates. |
| Upravljanje prilikama | 2783798 | Prilikom uvoza procjena projekta u redak ponude nedostaju opisi zadataka za procjene troškova i materijala.|
| Upravljanje prilikama | 2988635 | Poboljšajte msg opis pogreške prilikom brisanja kupca na ponudi. |
| Upravljanje prilikama | 3001191 | Nije moguće stvoriti ponudu iz prilike u kojoj je način naplate naveden kao null. |
| Nadogradnja | 3012324 | Pretvorba projekta nije uspjela na projektu s kontrolnim znakovima kao što je Tab u nazivu. || Planiranje i praćenje projekta | 2790384 | Prekoračenje vremena skupa operacija na čekanju je prekratko. |
| Planiranje i praćenje projekta | 3044275 | Nedostaje lokalizacija za: nedostajeProjectSchedulerErrorMessage. |
| Planiranje i praćenje projekta | 3044277 | Rešetka izviđača projekta ne učitava se kada je planer neiskorišten.|
| Upravljanje resursima | 2943153 | Ažuriraj karticu Praćenje da bi se prikazala dva decimalna mjesta za Trajanje.|
| Podugovaranje | 2932774 | Pogreška u neispravnom odbacivanju retka fakture Za čitanje samo bacanje. |
| Podugovaranje | 2939556 | Status zaglavlja fakture dobavljača ne bi trebao biti postavljen na Skica internetskog brisanja ako nije aktivna. |
| Vrijeme i trošak | 2939998 | Iskoristite novu TESA verziju u ProjOpsu. |


### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se u aplikaciju Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
