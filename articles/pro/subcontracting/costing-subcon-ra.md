---
title: Procjena troškova dodjela podugovornih resursa
description: U ovom se članku objašnjava kako sustav Microsoft Dynamics 365 Project Operations izračunava procjenu troškova dodjela podugovorenih resursa.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522645"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Procjena troškova dodjela podugovornih resursa

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dodjela zadataka podugovorenih članova projektnog tima obračunava se korištenjem cjenika **Kupnja** priloženog podugovoru na povezanom zapisu člana tima. To se razlikuje od načina na koji se obračunavaju troškovi dodjele resursa zaposlenika gdje se dodjela zadataka resursa zaposlenika obračunava korištenjem cjenika **Trošak** priloženog ugovornoj jedinici projekta. 

Dodjele se za generičke podugovorene članove projektnog tima obračunavaju korištenjem postavljanja cijene temeljenog na ulozi u nabavnom cjeniku priloženom podugovoru. Nabavne cijene također se mogu postaviti posebno za svaki resurs. Ovim cijenama specifičnim za resurse dat će se prioritet kada su dodjele zadataka za obračun troškova imenovanih članova projektnog tima radnici zaposleni po ugovoru. 

Prioritet korištenja nabavne cijene specifične za ulogu u odnosu na onu specifičnu za resurs određuje se postavljanjem prioriteta dimenzije cijena u **Parametri > Dimenzije cijena temeljene na iznosu**.

Ova funkcija dinamičkog izvođenja cijena na temelju postavljanja dimenzija za nabavne cijene podizvođača slična je načinu na koji se izvode stope troškova i naplate za zaposlene s punim radnim vremenom. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Izrada dodjela zadataka za dobivanje procjene troškova resursa podizvođača

Dodjele zadataka za podizvođače mogu se izraditi na dva načina: 
- Putem kartice **Zadaci**.
- Putem kartice **Tim**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Izrada dodjela resursa putem kartice Zadaci
Putem popisa **Resursi** na kartici **Zadaci** za određeni zadatak, možete izraditi dodjelu zadatka za imenovani resurs ili generički resurs. Ako odaberete imenovani resurs iz padajućeg izbornika **Dodijeljeni resursi** na zadatku te je taj resurs ugovorni radnik, imenovani resurs dodjeljuje se zadatku te se izrađuje odgovarajući zapis člana projektnog tima s vrstom radnika postavljenom na **Ugovorni radnik** i stavkom **Valjanost** postavljenom na **Nevažeće**. Kao sljedeći korak, morat ćete otvoriti zapis člana projektnog tima i odabrati podugovor i redak podugovora. Time će se ažurirati dodjelu zadatka kako bi imao referencu na podugovor i redak podugovora, a ažurirat će i status člana tima na **Važeće**.

Ako odlučite izraditi generičkog člana tima iz padajućeg izbornika **Dodijeljeni resursi** na zadatku, putem dijaloškog okvira **Izrada generičkog člana tima** moći ćete odabrati podugovor i redak podugovora. Kada je generički resurs dodijeljen zadatku te je izrađen odgovarajući zapis člana projektnog tima, primijetit ćete da je zapis člana projektnog tima izrađen tako da je vrsta radnika postavljena na **Ugovorni radnik**, a **Valjanost** na **Važeće**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Izrada članova projektnog tima putem kartice Tim
Putem kartice Tim na projektu možete izraditi generičkog ili imenovanog člana tima. Prilikom izrade člana tima možete odabrati podugovor i redak podugovora. Nakon što se član tima izradi, morat ćete ga dodijeliti zadatku putem padajućeg izbornika **Dodijeljeni resursi** na zadatku. 

## <a name="updating-estimates"></a>Ažuriranje procjena
Nakon što ste članovima projektnog tima dodijelili zadatke, morat ćete otići na karticu **Procjene** na projektu i odabrati **Ažuriraj cijene** kako bi se stope troškova dodjele resursa podizvođača ažurirale na temelju nabavnog cjenika priloženog podugovoru. Procjene se ne izrađuju za nedodijeljene zadatke u sustavu Microsoft Dynamics 365 Project Operations. Kao rezultat toga, morat ćete izraditi dodjele zadataka kako biste odredili cijene i troškove različitih zadataka svog projekta. 

> [NAPOMENA!] Članovi projektnog tima za koje je stavka **Vrsta radnika** postavljena na **Ugovorni radnik**, no koji nemaju referencu podugovora, nose oznaku **Nevažeće** na rešetki **Članovi projektnog tima**. Ako ima članova projektnog tima s tim statusom, otvorite zapis člana projektnog tima i ručno ažurirajte polja podugovor i redak podugovora tako da procjena financijskog troška točno odražava trošak podizvođača na kartici **Procjene**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
