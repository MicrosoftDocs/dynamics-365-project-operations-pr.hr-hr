---
title: Novosti u listopadu 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/nenaseljenim resursima u listopadu 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806717"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u listopadu 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.57.0.176
- Upravljanje projektima i računovodstvo u verziji 10.0.30 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Planiranje i praćenje projekta | **Vanjsko zakazivanje operacija projekta**<br>Vanjski način zakazivanja omogućuje korisnicima izvorno stvaranje, ažuriranje i brisanje entiteta koji su povezani sa strukturama raščlambe rada (WBS) korištenjem izvornih Dataverse API-ja, bez trenutnih ograničenja koja nameće Project za web. | [Vanjsko zakazivanje](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementacija i konfiguracija | <p>**Dopuštanje korisnicima da odaberu vrstu implementacije**<br>Ažuriranja projektnih operacija na temelju proizvoda (PDF- ovi) koriste se za automatsku instalaciju rješenja za dvostruko pisanje projekata kada se u okruženje instaliraju rješenja za jezgru i orkestraciju s dva pisanja.</p><p>Ova značajka uvodi novi **parametar ponašanja** nadogradnje rješenja u parametrima projekta. Kada je ovaj parametar postavljen samo **na** Lite, PUD-ovi više neće automatski instalirati Project Operations Dual-write rješenje, čak i ako su u okoliš instalirana rješenja s dvostrukom jezgrom i orkestracijom. Takvo će ponašanje koristiti kupcima koji planiraju koristiti rješenja s dvostrukim pisanjem za integraciju naloga za prodaju u financijske i operativne aplikacije, ali žele koristiti Project Operations u Lite načinu rada (to jest, bez integracije u financijske i operativne aplikacije).</p> | |
| Naplata i određivanje cijene | <p>**Konverzija valute za transakciju neplaćene prodaje troškova u integriranim okruženjima**<br>Za korisnike koji koriste projektne operacije integrirane s financijskim i operativnim aplikacijama (to jest, u vrsti implementacije resursa/ne zaliha), tečajevi se obično ovladavaju u aplikacijama za financije i operacije. Međutim, ako bi se kategorija troškova trebala cijeniti pomoću metode izračuna cijene "po trošku" ili "marža iznad troška" kada se kupcu naplati, tečaj koji se koristi za izračunavanje iznosa prodaje koristi tečajeve u Dataverse aplikacijama za financije i operacije, a ne tečajeve iz financijskih i operativnih aplikacija.</p><p>Ova značajka uvodi novi **parametar ponašanja** pretvorbe valuta u parametrima projekta. Kada je ovaj parametar postavljen na **Prošireno s rezervnim povratom**, neplaćeni iznosi prodaje na transakcije troškova izračunavaju se pomoću tečajeva iz financijskih i operativnih aplikacija.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2316317 | Sustav omogućuje kreiranje fakture koja nema transakcija koje se mogu naplatiti. |
| Naplata i određivanje cijene | 2737300 |  **Provjeri raspoloživost polja Kupca** prije nego što se pristupi obrascu. |
| Naplata i određivanje cijene | 2744948 | Dodajte provjeru null za metodu naplate. |
| Naplata i određivanje cijene | 2763515 | Prilikom nedostatka ugovora o prodaji fakture nema null rukovatelja referentnom pogreškom. |
| Naplata i određivanje cijene | 2844301 | Stvaranje skupne fakture ne uspijeva zbog pogreške. |
| Naplata i određivanje cijene | 2845869 | Neispravna pohrana usluge tvrtke ili ustanove. |
| Naplata i određivanje cijene | 2853729 | Pojedinosti o ulozi i cijeni ažuriraju se prilikom izmjene vrste naplate. |
| Naplata i određivanje cijene | 2940350 | Kada su stvarne cijene, potrebno je automatski unijeti samo aktivne cjenike. |
| Implementacija i konfiguracija | 3001206 | Entitet msdyn\_ replaylogheader sprječava nadogradnje korisničkih orgova. |
| Upravljanje prilikama | 2755582 | U pomoći za podijeljeno pravilo naplate rukuje se iznimkama null referenci. |
| Upravljanje prilikama | 2761477 | Kada se koristi podijeljena naplata, brisanje prekretnice (zaglavlja) ostavlja prekretnice za rijetke slučajeve. |
| Upravljanje prilikama | 2767595 | Kada se zapis o korištenju materijala otvori u glavnom obrascu, resurs za koji se može rezervirati za zapis mijenja se u trenutno prijavljenog korisnika. |
| Planiranje i praćenje projekta | 2790384 | Prekoračenje vremena skupa operacija na čekanju je prekratko. |
| Planiranje i praćenje projekta | 2957840 | Zadatke nije moguće spremiti, a stupce nije moguće dodati na **stranicu Zadaci** u integriranim operacijama projekta. |
| Upravljanje resursima | 2751560 | Nedosljedne jedinice preferirane organizacije u zahtjevima resursa. |
| Podugovaranje | 2853245 | Podudaranje za stvarne retke fakture dobavljača ne obnavlja status potvrde ako je redak ugovora već povezan s retkom fakture dobavljača. |
| Podugovaranje | 2907231 | Faza obrade faktura dobavljača ne može se unaprijediti. |
| Vrijeme i trošak | 2867363 | Zapisi ne ispadaju iz prikaza Izostanci/godišnji odmori za odobravanje kada su stavljeni u red čekanja za odobrenje. |
| Vrijeme i trošak | 2894405 | TESA: Neiskorišteni DIREKTORIJ POC-a uzrokuje probleme s usklađenosti. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se u aplikaciju Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
