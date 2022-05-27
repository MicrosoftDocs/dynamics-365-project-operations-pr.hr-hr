---
title: Izrada rezervacije projekta s ploče rasporeda
description: Ova tema pruža informacije o izradi rezervacije projekta s ploče rasporeda.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 693f4c4be1371bae232f636a5e168e889e81b09c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578009"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Izrada rezervacije projekta s ploče rasporeda

[!include [banner](../includes/psa-now-project-operations.md)]

Možete rezervirati resurs za projekt izravno s kartice projekta **Tim** ili generiranjem zahtjeva resursa iz zadatka generičkog člana tima, a zatim ispunjavanjem generiranog zahtjeva s članom projektnog tima.

Resurs možete rezervirati za projekt i izravno s ploče rasporeda. To možete učiniti na tri načina:

- **Rezerviraj iz generiranog preduvjeta resursa:** Možete generirati preduvjet resursa nakon što izradite generički resurs i dodijelite zadatke unutar projekta.

- **Rezerviraj iz primarnog preduvjeta:** Primarni preduvjeti prikazuju se na ploči rasporeda na kartici **Projekt**. 

- **Rezerviraj iz novog preduvjeta resursa:** Možete izraditi preduvjet resursa od nule i povezati ga s projektom. Na ploči s rasporedom, preduvjet resursa prikazuje se na kartici **Otvoreni preduvjeti**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervirajte iz generiranog preduvjeta resursa

Možete izraditi generički resurs i dodijeliti ga jednom ili više zadataka unutar projekta. Zatim možete generirati preduvjet resursa od generičkog člana tima. 

1.  Na ploči s rasporedom, taj resurs prikazat će se na kartici **Otvoreni zahtjevi**. Možda ćete morati koristiti filtre stupaca na rešetki ako imate mnogo otvorenih zahtjeva. 

    ![Dodavanje kartice preduvjeta ploči s rasporedom.](media/FAQ-Project-Booking-Schedule-Board-1.png "Snimka zaslona tablice rezervacija i dodjela")

2. Odaberite preduvjet. Kartica **Pronađi dostupnost** pojavit će se pri vrhu odabranog retka.
 
3. Odabirom kartice otvara se se Pomoćnik rasporeda ploče s rasporedom i filtriraju se dostupni resursi koji ispunjavaju zahtjev resursa. Zatim možete rezervirati resurs.

4. Možete i povući i ispustiti odabrani redak s dna ploče s rasporedom do ćelije resursa na rešetki iznad. Kada ga ispustite, na desnoj strani će se otvoriti panel **Stvori rezervaciju za resurs**.

    Odabirom **Rezerviraj** resurs se rezervira za projektni tim.

![Izrada panela Rezervacije resursa.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervacija od primarnog preduvjeta

Stvaranjem projekta u aplikaciji Project Service automatski se stvara preduvjet resursa nazvan primarnim preduvjetom. To je prazni zahtjev koji se koristi za brzo rezerviranje resursa s pomoću ploče s rasporedom bez generiranja zahtjeva ili njegove izrade od nule. Budući da je taj zahtjev prazan, morat ćete navesti datume, kao i način dodjele i sate, ako je primjenjivo. 

1. Za rezervaciju resursa s primarnim preduvjetom, na ploči s rasporedom odaberite karticu **Projekt**. Ako imate mnogo projekata, možda ćete morati koristiti filtar stupaca u stupcu **Projekt** .

   ![Filtri kolona na ploči s rasporedom.](media/FAQ-Project-Booking-Schedule-Board-2.png "Snimka zaslona tablice rezervacija i dodjela")

2. Odaberite zahtjev koji ima samo naziv projekta u svom nazivu i koji ima trajanje vrijednosti nula (0).

3. Odaberite karticu **Pronađi dostupnost** koja se pojavi u tom retku. To će ploču s rasporedom prebaciti u način rada s pomoćnikom rasporeda i prikazat će dostupne resurse koji se mogu rezervirati za projekt.

4. Budući da je **Primarrni zahtjev** prazni zahtjev s trajanjem vrijednosti nula (0), kada birate i rezervirate resurs, trebate postaviti trajanje na panelu **Izradi rezervaciju resursa**.

5. Također možete odabrati **Primarni zahtjev projekta** pri dnu ploče s rasporedom i povući ga i ispustiti na resurs da biste ga rezervirali.
 
    Budući da je **Primarrni zahtjev** prazni zahtjev s trajanjem vrijednosti nula (0), kada birate i rezervirate resurs, trebate postaviti trajanje na panelu **Izradi rezervaciju resursa**.
 
    Kada rezervirate resurs putem **Primarrnog preduvjeta** na ploči s rasporedom, dodat ćete ga projektnom timu bez ikakvih zadataka.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervirajte iz novog preduvjeta resursa
Dovršite sljedeće korake za rezervaciju iz novog zahtjeva resursa. 

1. Idite na **Zahtjevi resursa** i odaberite **Novo** kako biste izradili novi zahtjev resursa.

2. Na kartici **Projekt** odaberite projekt za pridruživanje zahtjeva projektu.
 
    Taj novi zahtjev prikazuje se kao **Otvoreni zahtjev** na ploči s rasporedom i možete ga ispuniti.

3. Rezervirajte resurs da biste ga dodali projektnom timu.

4. Sada kad je resurs rezerviran, morate ručno dodijeliti zadatke.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
