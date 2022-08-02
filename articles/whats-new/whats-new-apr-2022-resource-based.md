---
title: Novosti u travnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/neutemeljenim resursima u travnju 2022.
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

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.41.0.45
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.26

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

Kategorije nabave mogu se koristiti u narudžbenicama za projekt i fakturama dobavljača na čekanju. Dodatne informacije potražite u članku [Korištenje kategorija nabave s narudžbenicama za projekt i fakturama dobavljača na čekanju](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanju projektnih operacija u ožujku 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| -------------- | ------------------- | ------------|
| Projekt Operations integracija projekt dobavljač faktura redak izvozni entitet msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Ova karta podržava korištenje kategorija nabave s narudžbenicama i fakturama dobavljača na čekanju. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| ------------ | ---------------- | -------------- |
| Vrijeme i trošak | 2573900 | Značajka **modernog odobrenja** mora biti omogućena prema zadanim postavkama. |
| Naplata i određivanje cijene | 2603313 | Ispravljena je dvostruka pogreška zapisa koja je spriječila dodavanje redaka ponude i ugovora s proizvodom. |
| Implementacija i konfiguracija | 2611368 | Korisnici moraju moći dodati do pet prilagođenih entiteta u rješenje pomoću modernog dizajnera aplikacija. |
| Vrijeme i trošak | 2628285 | Riješen je problem koji je utjecao na mogućnost postavljanja ispravne kategorije resursa tijekom uvoza stavke vremena. |
|   Upravljanje prilikama| 2628815 | Ažurirajte ograničenje znakova opisa detalja retka ponude tako da odgovara ograničenju znakova predmeta zadatka tako da uvoz uspije za zadatke u kojima je predmet dulji od 100 znakova. |
| Vrijeme i trošak| 2629547 | Polje **Poslano po** odobrenjima projekta mora upućivati na korisnika koji je poslao zapis. |
| Vrijeme i trošak| 2629865 | Polje **Kopiraj kategoriju** za zadatke prilikom kopiranja projekata. |
| Vrijeme i trošak| 2636463 | Fiksirali su filtre na odobrenja u modernim obrascima za odobrenja. |
| Planiranje i praćenje projekta | 2648300 | Riješen je problem koji sprječava promjenu vlasnika projekta. |
| Naplata i određivanje cijene | 2563000 | Reci temeljnice za neplaćenu prodaju u kojima se valuta razlikuje od ugovorne valute ne smiju biti dopušteni. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu (LCS) i pogledajte članak [iz](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) baze znanja.
