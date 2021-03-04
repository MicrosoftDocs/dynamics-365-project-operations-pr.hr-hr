---
title: Održavanje članova tima
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za projektne timove i o dodjeli istih zadacima.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131514"
---
# <a name="maintain-team-members"></a>Održavanje članova tima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete dodati imenovani resurs projektnom timu tako da ga izravno rezervirate za tim.

1. U aplikaciji Dynamics 365 Project Operations, idite na **Projekti** i odaberite otvori projekt za koji rezerviraš.
2. Na stranici **Projekt**, na kartici **Tim**, odaberite **Novo**. 
3. U dijaloškom okviru **Brza izrada člana projektnog tima** odaberite resurs koji se može rezervirati. Polje **Uloga** popunit će se zadanom ulogom resursa ako mu je dodijeljena jedna. Ulogu možete promijeniti. 
4. Odaberite početni i završni datum koji će biti potrebni za resurs i odaberite način dodjele kapaciteta resursa. 
5. Ako želite da član tima bude odobravatelj projekta, u polju **Odobravatelj projekta** odaberite **Da**. Član tima može odobriti poslane unose vremena i troška za ovaj projekt. 
6. Odaberite **Spremi**.

Sada možete dodijeliti rezervirani resurs zadacima na projektu. Na stranici **Projekt**, na kartici **Raspored**, dodijelite zadatke novom resursu. Birač resursa koji je pokrenut iz polja **Resursi** u rešetki zadataka pokazat će članove tima koje možete odabrati.


U aplikaciji Project Operations, rezerviranja resursa i dodjele zadataka nisu usko povezani. Kada upotrebljavate birač resursa u rasporedu, možete dodijeliti zadatke članovima tima za više sati nego što njihove rezervacije pokrivaju na projektu.

Razlike između rezervacija i zadataka članova tima prikazane su na karticama **Tim** i **Usklađivanje resursa**. Također možete uskladiti razlike između rezervacija i zadataka za resurse na podrobnijoj razini.

Upotrijebite birač resursa na kartici **Raspored** kako biste potražili i odabrali resurse koji se mogu rezervirati, a koji još nisu dio projektnog tima. Ti se resursi prikazuju u biraču resursa kao **Ostali resursi**.

Kada izvršite odabir, resurs se dodaje projektnom timu i dodjeljuje zadatku, ali rezervacije se ne generiraju.

Možete koristiti mogućnost proširenja rezervacije kartice **Usklađivanje** ili **Ploča s rasporedom** da biste rezervirali kapacitet resursa za projekt.

Nakon što je član tima rezerviran za vaš projekt, za upravljanje rezervacijama možete upotrijebiti mogućnost **Održavanje rezervacija** ili izravno **Ploču s rasporedom**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]