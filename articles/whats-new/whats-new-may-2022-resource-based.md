---
title: Novosti u svibnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju microsofta Dynamics 365 Project Operations u svibnju 2022. za scenarije koji se temelje na resursima/nenaseljenim resursima.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921385"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u svibnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.42.0.70
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete
### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje resursima | 2634019 | Poboljšane poruke o pogreškama za poslovne provjere valjanosti prilikom dodavanja generičkih članova tima kao resursa. |
| Planiranje i praćenje projekta | 2648515 | Ograničena ažuriranja vlasnika, stanja i statusa **u** entitetima zakazivanja.**·** **·** |
| Naplata i određivanje cijene | 2653167 | **Decimalni razdjelnik rešetke** Procjene mora slijediti postavke oblikovanja u **osobnim mogućnostima**. |
| Naplata i određivanje cijene| 2662251 | Vrijednosti u poljima **Ispravljena jedinica** i **Grupa** jedinica zadane su prilikom stvaranja zapisa u procjenama materijala. |
| Naplata i određivanje cijene| 2571408 | Nenaplaćeni podaci o prodaji ovjereni su ID-om predračunske fakture prilikom kreiranja skice fakture. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu (LCS) i pogledajte članak [iz](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) baze znanja.
