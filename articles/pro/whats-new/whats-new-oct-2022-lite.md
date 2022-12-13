---
title: Što je novo u listopadu 2022. – Osnovna implementacija aplikacije Project Operations
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju implementacije sustava Microsoft Dynamics 365 Project Operations lite u listopadu 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806737"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Što je novo u listopadu 2022. – Osnovna implementacija aplikacije Project Operations

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.57.0.176

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Planiranje i praćenje projekta | **Vanjsko zakazivanje operacija projekta**<br>Vanjski način zakazivanja omogućuje korisnicima izvorno stvaranje, ažuriranje i brisanje entiteta koji su povezani sa strukturama raščlambe rada (WBS) korištenjem izvornih Dataverse API-ja, bez trenutnih ograničenja koja nameće Project za web. | [Vanjsko zakazivanje](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementacija i konfiguracija | <p>**Dopuštanje korisnicima da odaberu vrstu implementacije**<br>Ažuriranja projektnih operacija na temelju proizvoda (PDF- ovi) koriste se za automatsku instalaciju rješenja za dvostruko pisanje projekata kada se u okruženje instaliraju rješenja za jezgru i orkestraciju s dva pisanja.</p><p>Ova značajka uvodi novi **parametar ponašanja** nadogradnje rješenja u parametrima projekta. Kada je ovaj parametar postavljen samo **na** Lite, PUD-ovi više neće automatski instalirati Project Operations Dual-write rješenje, čak i ako su u okoliš instalirana rješenja s dvostrukom jezgrom i orkestracijom. Takvo će ponašanje koristiti kupcima koji planiraju koristiti rješenja s dvostrukim pisanjem za integraciju naloga za prodaju u financijske i operativne aplikacije, ali žele koristiti Project Operations u Lite načinu rada (to jest, bez integracije u financijske i operativne aplikacije).</p> | |

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2316317 | Sustav omogućuje kreiranje fakture koja nema transakcija koje se mogu naplatiti. |
| Naplata i određivanje cijene | 2737300 | Provjeri raspoloživost polja Kupca prije nego što se pristupi obrascu. |
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
| Upravljanje resursima | 2751560 | Nedosljedne jedinice preferirane organizacije u zahtjevima resursa. |
| Podugovaranje | 2907231 | Faza obrade faktura dobavljača ne može se unaprijediti. |
| Vrijeme i trošak | 2867363 | Zapisi ne ispadaju iz prikaza Izostanci/godišnji odmori za odobravanje kada su stavljeni u red čekanja za odobrenje. |
| Vrijeme i trošak | 2894405 | TESA: Neiskorišteni DIREKTORIJ POC-a uzrokuje probleme s usklađenosti. |
