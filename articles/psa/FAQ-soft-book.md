---
title: Promjenjivo rezerviranje resursa
description: Ova tema pruža informacije o tome kako uvjetno planirati ili promjenjivo rezervirati članove projektnog tima.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146429"
---
# <a name="soft-book-a-resource"></a>Promjenjivo rezerviranje resursa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete uvjetno zakazati ili „promjenjivo rezervirati” resurs za projektni tim da biste pokazali da planirate dodijeliti resurs projektu. Promjenjive rezervacije ne troše dostupni kapacitet resursa, te projektnim zadacima možete dodijeliti promjenjivo rezervirane članove tima. Međutim, budući da promjenjiva rezervacija ne troši kapacitet resursa, i dalje možete „fiksno rezervirati” resurs za druge zadatke za isto razdoblje. Generički resursi ne mogu se promjenjivo rezervirati i promjenjiva rezervacija ne može ispuniti zahtjev za generički resurs.

Promjenjivo rezervirani članovi projektnog tima popisani su na kartici **Tim** stranice **Projekt** s njihovim promjenjivo rezerviranim satima prikazanim u stupcu **Promjenjivo rezervirani sati** u prikazu **Imenovani članovi tima**. Promjenjivo rezervirani članovi tima također su popisani na ploči s rasporedom. Budući da su promjenjivo rezervirani, ploča s rasporedom ne prikazuje nikakvo trošenje kapaciteta tih resursa. Promjenjivo rezervirano vrijeme ne prikazuje se na kartici **Usklađivanje** niti u polju **Produži rezervacije** na kartici **Usklađivanje** ploče s rasporedom. 

Postoje dva načina promjenjive rezervacije člana tima za projekt: izravno s ploče s rasporedom ili dodavanjem člana tima na kartici **Tim**. 

## <a name="soft-book-from-the-schedule-board"></a>Promjenjiva rezervacija s ploče s rasporedom
Dovršite sljedeće korake za promjenjivu rezervaciju resursa s ploče s rasporedom. 

1. Otvorite ploču s rasporedom, a zatim na panelu **Preduvjeti rezervacije** odaberite karticu **Projekt**.
2. Pronađite projekt za koji želite promjenjivo rezervirati resurs. Ako na popisu postoji veliki broj projekata, odaberite zaglavlje stupca **Projekt**, a zatim koristite filtar da biste pretražili jedan ili više projekata.
3. Odaberite projekt, a zatim ga povucite i ispustite na vremenskoj rešetki resursa.
5. Na panelu **Izradi rezervaciju resursa** prilagodite datum početka i završetka, postavite **Status rezervacije** na **Promjenjiva**, a zatim postavite sate. 
6. Kliknite **Rezerviraj**. Kod projekta će se resurs sada prikazati na kartici **Tim** kao resurs. U prikazu **Imenovani član tima** vidjet ćete promjenjivo rezervirane sate u stupcu s **Promjenjivo rezervirani sati**.

> [!NOTE]
> Sada možete dodijeliti promjenjive rezervacije zadacima na kartici **Raspored**. Na kartici **Usklađivanje**, resurs prikazuje manjak rezervacija u odnosu na njegove dodjele zadataka budući da kartica **Usklađivanje** uzima u obzir samo fiksne rezervacije. Možete koristiti značajku **Produži rezervacije** kako biste fiksno rezervirali resurs i riješili manjak fiksnih rezervacija u odnosu na dodjele resursa. Morat ćete ručno otkazati promjenjive rezervacije resursa koristeći značajku **Zadrži rezervacije**.

## <a name="soft-book-on-the-team-tab"></a>Promjenjiva rezervacija na kartici Tim

Možete dodati članove tima izravno na kartici **Tim** , a zatim promjeniti status njihove rezervacije s **Fiksna** na **Promjenjiva** s pomoću značajke **Zadrži rezervacije**. Kada člana tima dodate na ovaj način, to će uvijek rezultirati fiksnom rezervacijom, osim ako ne odaberete način dodjele **Nijedan**.

Za korištenje ovog načina, poduzmite sljedeće korake.

1. Na stranici **Projekt** na kartici **Tim** kliknite **Novo**.
2. Odaberite resurs koji se može rezervirati, ulogu i datume od i do.
3. Odaberite bilo koji način dodjele osim **Nijedan**.
4. Odaberite **Spremi**. Resurs ćete vidjeti na rešetki, a njegove sate u stupcu **Fiksno rezervirani sati**.
5. Zadržite rezervacije resursa odabirom **Zadrži rezervacije**.
6. Kada se ploča s rasporedom otvori, proširite resurs za prikaz njegovih rezervacija. Rezervacija će biti prikazana kao **Fiksna**.
7. Desnim klikom kliknite na rezervaciju i pod stavkom **Promijeni status** odaberite **Promjenjiva rezervacija** \> **Promjenjiva**. Status rezervacije sada je **Promjenjiva**.
8. Nakon zatvaranja ploče s rasporedom, kada gledate u prikazu **Imenovani članovi tima**, vidjet ćete da su sati resursa premješteni iz stupca s **Fiksno rezervirani sati** u **Promjenjivo rezervirani sati** na rešetki kartice **Tim**.

> [!NOTE]
> Ako fiksno rezervirate resurs za tim, a zatim mu dodijelite zadatke u rasporedu, kada koristite značajku **Zadrži rezervacije** za promjenu statusa s **Fiksna** na **Promjenjiva**, dodjele zadataka za taj resurs će ostati. Međutim, taj resurs će na kartici **Usklađivanje** imati manjak rezervacija budući da se samo fiksne rezervacije uzimaju u obzir pri usklađivanju rezervacija i dodjela. Možete koristiti značajku **Produži rezervacije** na kartici **Usklađivanje** kako biste fiksno rezervirali resurs i riješili manjak fiksnih rezervacija u odnosu na dodjele resursa. Morat ćete otkazati promjenjive rezervacije resursa koristeći značajku **Zadrži rezervacije**.

Kada budete spremni za promjenu promjenjivo rezerviranog resursa člana tima u fiksno rezerviranog člana tima, uradite sljedeće:

1. Na ploči s rasporedom proširite resurs za prikaz njegovih rezervacija. Rezervacija će biti prikazana kao **Promjenjiva**.
2. Desnim klikom kliknite na rezervaciju i pod stavkom **Promijeni status** odaberite **Fiksna rezervacija** \> **Fiksna**. Status rezervacije je sada **Fiksna**.
3. Nakon zatvaranja ploče s rasporedom, vratite se na projekt i otvorite karticu **Tim**, kada ste u prikazu **Imenovani članovi tima**, vidjet ćete da su sati resursa premješteni iz stupca **Promjenjivo rezervirani sati** u stupac **Fiksno rezervirani sati** na kartici **Tim**. Ako je resurs dodijeljen zadacima, više neće prikazivati manjak rezervacija na kartici **Usklađivanje** budući da su njegove rezervacije postale fiksne.



[!INCLUDE[footer-include](../includes/footer-banner.md)]