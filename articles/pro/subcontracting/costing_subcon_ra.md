---
title: Procjena troškova dodjela resursa kooperantima
description: Ovaj tema objašnjava kako Microsoft Dynamics 365 Project Operations izračunava procjenu troškova podugovarateljskih dodjela resursa.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903002"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Procjena troškova dodjela resursa kooperantima

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Dodjele zadataka članova projektnog tima kooperanta koštaju pomoću **cjenika nabave** pridruženog podugovaljku u povezanom zapisu člana tima. To se razlikuje od načina na koji se košta dodjela resursa zaposlenika ako se dodjele zadataka resursa zaposlenika koštaju pomoću **cjenika** troška koji je pridružen ugovornom odjelu projekta. 

Za generičke članove projektnog tima koji su kooperanti, dodjele se koštaju pomoću postavljanja cijene temeljene na ulogama u cjeniku nabave pridruženom kooperantu. Nabavne cijene mogu se postaviti i posebno za svaki resurs. Te cijene specifične za resurse imat će prioritet kada su dodjele zadataka troškova imenovanih članova projektnog tima ugovorni radnici. 

Prioritet korištenja kupovne cijene specifične za ulogu u odnosu na specifičnu za resurs temelji se na postavljanju prioriteta dimenzije određivanja cijena u **parametrima > dimenzijama određivanja cijena na temelju iznosa**.

Ova funkcionalnost dinamičkog izvođenja cijena na temelju postavljanja dimenzija za nabavne cijene kooperanata slična je načinu na koji se cijene troškova i računa izvode za zaposlenike s punim radnim vremenom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Stvaranje dodjela zadataka za dobivanje procjena troškova resursa kooperanta

Dodjele zadataka za kooperante mogu se stvoriti na dva načina: 
- Korištenje **kartice** Zadaci.
- Korištenje **kartice** Tim.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Stvaranje dodjela resursa pomoću kartice Zadaci
Pomoću **popisa Resursi** na **kartici Zadaci** za određeni zadatak možete stvoriti dodjelu zadatka za imenovani resurs ili generički resurs. Ako odaberete imenovani resurs s **padajućeg izbornika Dodijeljeni resursi** na zadatku, a taj resurs je ugovorni radnik, imenovani resurs dodjeljuje se zadatku, a odgovarajući zapis člana projektnog tima stvara se s vrstom radnika postavljenom na **Ugovorni radnik, a valjanost je** **postavljena** na **Nevažeće**. Kao sljedeći korak morat ćete otvoriti zapis člana projektnog tima i odabrati redak kooperanta i kooperanta. Time će se zadatak ažurirati tako da se odnosi na redak kooperanta i kooperanta, a status člana tima ažurirat će i na **Valjano**.

Ako odlučite stvoriti generičkog člana tima s **padajućeg izbornika Dodijeljeni resursi** na zadatku, **dijaloški okvir za stvaranje generičkih članova tima** omogućit će vam odabir retka kooperanta i kooperanta. Kada se generički resurs dodijeli zadatku i stvori odgovarajući zapis člana projektnog tima, primijetit ćete da je zapis člana projektnog tima stvoren s vrstom radnika postavljenom na **Ugovorni radnik** i Valjanost **postavljena** na **Valjano**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Stvaranje članova projektnog tima pomoću kartice Tim
Pomoću kartice Tim na projektu možete stvoriti generičkog ili imenovanog člana tima. Prilikom kreiranja člana tima imate mogućnost da izaberete liniju kooperanta i kooperanta. Nakon stvaranja člana tima morat ćete dodijeliti člana tima zadatku pomoću **padajućeg izbornika Dodijeljeni** resursi na zadatku. 

## <a name="updating-estimates"></a>Ažuriranje procjena
Nakon što dodijelite članove projektnog tima zadacima, morat ćete prijeći **na karticu Procjene** u projektu i **odabrati Ažuriraj cijene da biste** osigurali da se cijene dodjela resursa kooperanta ažuriraju na temelju popisa nabavnih cijena priloženih podugovaranom ugovoru. Imajte na umu da se procjene ne generiraju za nedodijeljene zadatke u Microsoftu Dynamics 365 Project Operations. Kao rezultat toga, morat ćete stvoriti zadatke za cijenu i trošak različitih zadataka na vašem projektu. 

> [NAPOMENA!] Članovi projektnog tima koji imaju **vrstu Radnik** kao **ugovorni radnik,** ali nemaju referencu podugovora, označeni su kao **nevažeći u** **rešetki članova projektnog** tima. Ako postoje članovi projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja retka kooperanta i kooperanta tako da procjena financijskih troškova točno odražava trošak kooperanta na **kartici** Procjene. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
