---
title: Procjena troškova dodjela podugovornih resursa
description: U ovom se članku objašnjavaju neki način na koji Microsoft Dynamics 365 Project Operations izračunava procjenu troškova dodjela kooperantskih resursa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262050"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Procjena troškova dodjela podugovornih resursa

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Dodjele zadataka članova projektnog tima kooperanta koštaju se pomoću **cjenika nabave** priloženog podugovaranju na zapisu povezanog člana tima. To se razlikuje od načina na koji se koštaju dodjele resursa zaposlenika ako se dodjele zadataka resursa zaposlenika koštaju pomoću **cjenika Troškova** koji je povezan s ugovornom jedinicom projekta. 

Za generičke članove projektnog tima koji su podugovarani, dodjele se koštaju pomoću postavke cijena na temelju uloga u cjeniku nabave priloženom kooperantu. Nabavne cijene mogu se postaviti i posebno za svaki resurs. Ove cijene specifične za resurse imat će prioritet kada su dodjele zadataka imenovanih članova projektnog tima ugovorni radnici. 

Prioritet korištenja nabavne cijene specifične za ulogu u odnosu na specifičnu za resurs temelji se na postavljanju prioriteta dimenzije određivanja cijena u **parametrima > dimenzijama cijena na temelju iznosa**.

Ova funkcionalnost dinamičkog izvlačenja cijena na temelju postave dimenzije za nabavne cijene kooperanata slična je načinu na koji se izvode cijene troškova i računa za zaposlenike s punim radnim vremenom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Kreiranje dodjela zadataka za dobivanje procjena troškova resursa kooperanata

Dodjele zadataka za podizvođače mogu se stvoriti na dva načina: 
- Pomoću kartice **Zadaci koristite karticu Zadaci**.
- Pomoću kartice **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Stvaranje dodjela resursa pomoću kartice Zadaci
Pomoću popisa Resursi **na** **kartici Zadaci** za određeni zadatak možete stvoriti dodjelu zadatka za imenovani resurs ili generički resurs. Ako odaberete imenovani resurs s padajućeg izbornika **Dodijeljeni resursi** na zadatku, a taj je resurs ugovorni radnik, imenovani resurs dodjeljuje se zadatku i stvara se odgovarajući zapis člana projektnog tima s vrstom radnika postavljenom na **Ugovorni radnik** i **Valjanost postavljenom** na **Nevaljano**. Kao sljedeći korak morat ćete otvoriti zapis člana projektnog tima i odabrati liniju kooperanta i kooperacije. Time će se dodjela zadatka ažurirati tako da ima referencu na liniju podugovaratelja i podugovaranja, a status člana tima ažurirat će i na **Valjano**.

Ako odlučite stvoriti generičkog člana tima s padajućeg izbornika **Dodijeljeni resursi** na zadatku, **dijaloški okvir stvaranje** članova generičkog tima omogućit će vam odabir retka kooperanta i kooperacije. Kada se zadatku dodijeli generički resurs i stvori se odgovarajući zapis člana projektnog tima, primijetit ćete da se zapis člana projektnog tima stvara s vrstom radnika postavljenom na **Ugovorni radnik** i **Valjanost** postavljenom na **Valjano**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Stvaranje članova projektnog tima pomoću kartice Tim
Pomoću kartice Tim na projektu možete stvoriti generičkog ili imenovanog člana tima. Prilikom stvaranja člana tima možete odabrati redak podugovaranja i podugovaranja. Nakon stvaranja člana tima morat ćete dodijeliti člana tima zadatku pomoću **padajućeg izbornika Dodijeljeni resursi** na zadatku. 

## <a name="updating-estimates"></a>Ažuriranje procjena
Nakon što dodijelite članove projektnog tima zadacima, morat ćete prijeći **na karticu Procjene** u projektu i odabrati **Ažuriraj cijene** da biste osigurali da se stope troškova dodjele resursa kooperanta ažuriraju na temelju popisa nabavnih cijena priloženog kooperantu. Procjene se ne generiraju za nedodijeljene zadatke u Microsoftu Dynamics 365 Project Operations. Kao rezultat toga, morat ćete stvoriti zadatke za cijenu i troškove različitih zadataka na vašem projektu. 

> [NAPOMENA!] Članovi projektnog tima koji imaju vrstu Radnika kao **ugovorni radnik**, ali nemaju referencu kooperanta, označeni su kao **Nevažeći** u rešetki članova **projektnog** **tima.** Ako postoje članovi projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja retka podugovaratelja i podugovaranja tako da procjena financijskog troška točno odražava trošak kooperanta na **kartici Procjene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
