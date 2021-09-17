---
title: Novosti u kolovozu 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za kolovoz 2021. godine.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cd5a7e74fc90c6138cd672ff6109b59a8d2ae916
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323452"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u kolovozu 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

   - Project Operations u okruženju platforme Microsoft Dataverse verzije 4.13.0.152.
   - Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.20.

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- **Skupovi odobrenja**: Skupovi odobrenja grupiraju zahtjeve za vrijeme, trošak ili uporabu materijala u manje podskupove operacija. Ovo grupiranje omogućuje da se odobrenja obrađuju određenim redoslijedom po projektu i omogućuje ponovni pokušaj i sekvencioniranje. Grupiranje zahtjeva poboljšava pouzdanost i sljedivost obrade odobrenja za velike količine odobrenja. Dodatne informacije potražite u članku [Skupovi odobrenja](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. 

Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane tablične karte dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti na stranici **Dvostruko pisanje** u stupcu **Verzija**. Aktivirajte novu verziju karte odabirom mogućnosti **Verzije tabličnih karata**, odabirom najnovije verzije, a zatim spremanjem odabrane verzije. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem s nedostatkom stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2295625 | Naziv kontrolne točke mora se kopirati iz rasporeda računa u pojedinost retka fakture. |
| Naplata i određivanje cijene | 2316323 | Popust se ne smije uređivati na predračunu u aplikaciji Project Operations za scenarije koji se temelje na resursima. |
|   Upravljanje prilikama | 2338619 | Poslovna pravila **Prilika** i **Ponuda** moraju se pozivati samo na stranicama. |
| Upravljanje resursima | 2316523 | Uporaba mogućnosti **Pošalji zahtjev** iz zahtjeva za resurs koji ima pridruženu ulogu ne bi trebao prikazati pogrešku. |
| Upravljanje resursima | 2326885 | Stvaranje zahtjeva za resurs kroz projekt ne bi trebalo prikazivati pogrešku. |
| Vrijeme i trošak | 2335584 | Zastarjeli zadatak teče u vremenskom unosu. |
| Vrijeme i trošak | 2336884 | Gumb za vremenski unos **Kopiraj tjedan** mora raditi ne samo za trenutačnog korisnika. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi netočnih transakcija dobavljača i poreza na promet knjiže se kada se trošak stvori u transakciji kreditnom karticom. |
| Putovanje i trošak | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Pogrešno namirenje su redci nastali tijekom generiranja dnevnika plaćanja. |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi netočnih transakcija poreza na promet knjiže se kada se trošak stvori u transakciji kreditnom karticom. |
| Putovanje i trošak | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje retka troška može potrajati. |
| Projektno računovodstvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sustav ne podržava postavljanje kontinuiranog sekvencioniranja brojeva kada objavite procjenu nakon primjene KB 4619395. |
| Projektno računovodstvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Knjiženje fakture dobavljača možda neće uspjeti s porukom o pogrešci: „Transakcije na vaučeru nisu uravnotežene prema 17.5.2021. (računovodstvena valuta: 0,00 – izvještajna valuta: 0,01)” |