---
title: Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke
description: U ovoj temi nalaze se informacije o načinu rezervacije imenovanih resursa za projektne timove i o njihovoj dodjeli zadacima.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145349"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete dodati imenovani resurs u projektni tim tako da ga izravno rezervirate za tim. Da biste to učinili, izvršite sljedeće korake:

1. U programu Project Service Automation, idite na **Projekti** i odaberite Otvori projekt za koji rezervirate.
2. Na stranici **Projekt** na kartici **Tim** kliknite **Novo**. 

![Dodavanje člana tima s kartice tima](media/RM-how-to-1.png)

3. U dijaloškom okviru **Brza izrada člana projektnog tima** odaberite resurs koji se može rezervirati. Polje **Uloga** popunit će se zadanom ulogom resursa ako mu je dodijeljena jedna. Prema potrebi, ulogu možete promijeniti. 
4. Odaberite od i do datume koji će biti potrebni za resurs i odaberite način dodjele kapaciteta resursa. 
5. Ako želite da član tima bude odobravatelj projekta, odaberite **Da** u polju **Odobravatelj projekta**. To će značiti da član tima može odobriti poslane unose vremena i troška za ovaj projekt. 
6. Kliknite **Spremi**.

![Dodavanje člana tima u obrazac za brzu izradu](media/RM-how-to-2.png)


Sada možete dodijeliti rezervirani resurs zadacima na projektu. Na stranici **Projekt** kliknite karticu **Raspored** da biste dodijelili zadatke novom resursu. Birač resursa koji je pokrenut iz polja **Resursi** u rešetki zadataka pokazat će članove tima koje možete odabrati.

![Dodjela člana tima zadatku na kartici rasporeda](media/RM-how-to-3.png)

U verziji 3 za program Project Service Automation (PSA), rezervacije resursa i dodjele zadataka nisu usko povezane. To znači da kada koristite birač resursa u rasporedu, možete dodijeliti zadatke članovima tima za više sati nego što njihove rezervacije pokrivaju na projektu.
Možete vidjeti razlike između rezervacija članova tima i dodjela na kartici **Tim** ili na kartici **Usklađivanje resursa**. Možete i uskladiti razlike između rezervacija i dodjela za resurse na detaljnijoj razini.

![Kartica Usklađivanje resursa](media/RM-how-to-4.png)

Možete koristiti i birača resursa na kartici **Raspored** da biste potražili i odabrali resurse koji se mogu rezervirati, a koji još nisu dio projektnog tima. Oni se prikazuju u biraču resursa kao **Ostali resursi**.

![Dodjeljivanje resursa člana koji nije dio tima zadatku](media/RM-how-to-5.png)

Kada ovo činite, resurs se dodaje projektnom timu i dodjeljuje zadatku, ali rezervacije se ne generiraju.

![Član tima s dodjelama i bez rezervacija](media/RM-how-to-6.png)

Možete koristiti mogućnost proširenja rezervacije kartice **Usklađivanje** ili **Ploča s rasporedom** da biste rezervirali kapacitet resursa za projekt.

![Proširivanje rezervacija za člana tima na kartici usklađivanja resursa](media/RM-how-to-7.png)

Nakon što je član tima rezerviran za vaš projekt, možete koristiti održavanje rezervacija ili izravno koristiti Ploču s rasporedom za upravljanje rezervacijama.
