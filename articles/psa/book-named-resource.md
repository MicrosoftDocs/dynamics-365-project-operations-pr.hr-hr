---
title: Rezerviraj imenovane resurse iz zahtjeva resursa
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za generički zahtjev resursa.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145080"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezerviraj imenovane resurse iz zahtjeva resursa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete rezervirati imenovani resurs da zamjenite generički resurs koji ima zahtjev resursa.

1. U sustavu Project Service Automation (PSA) na stranici **Projekti**, kliknite karticu **Tim**.
2. S popisa odaberite generički resurs koji ima zahtjev resursa, a zatim kliknite **Rezerviraj**. Ili otvorite zahtjev resursa, a zatim kliknite **Rezerviraj**.


![Rezervacija člana generičkog tima](media/RM-how-to-14.png)


3. Na stranici **Pomoćnik za raspored**, odaberite imenovani resurs koji ćete rezervirati u projektni tim, a zatim kliknite **Rezerviraj**.

![Rezervacija člana generičkog tima s pomoću pomoćnika za raspored](media/RM-how-to-15.png)

Kada je rezervacija dovršena i ispunjena od strane imenovanog resursa, generički resurs zamjenjuje se imenovanim resursom.

![Imenovani član tima zamjenjuje člana generičkog tima](media/RM-how-to-16.png)

Zadaci u rasporedu ažuriraju se i s imenovanim resursom.

![Imenovani član tima dodijeljen projektnim zadacima](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Ispunite generički resurs s više imenovanih resursa
Ispunjavanje zahtjeva za generički resurs s više imenovanih resursa slično je dodjeljivanju jednog imenovanog resursa. Na primjer, postoji zadatak u trajanju od pet dana i 120 sati napora. Ovaj zadatak ne može dovršiti jedan resurs koji odrađuje tipičan dan od osam sati u pet dana u tjednu. 

![Zadatak koji treba 120 sati truda tijekom pet dana](media/RM-how-to-21.png)

Zahtjev je za 120 sati inženjerske robotike tijekom pet dana, što je 24 sata dnevno.

![Zahtjev po danu](media/RM-how-to-22.png)

Ovo je primjer kada je potrebno više imenovanih resursa za ispunjavanje zahtjeva generičkog resursa. Morat ćete rezervirati više resursa za ispunjavanje zahtjeva.

![Rezervacija više resursa za ispunjavanje zahtjeva](media/RM-how-to-23.png)

Glavna razlika u ovom scenariju je da generički resurs ostaje u timu koji je dodijeljen zadatku, a članovi tima rezerviranog imenovanog resursa ne dodjeljuju se kao dio položaja. Upravitelj projekta može dodijeliti rad po potrebi imenovanim resursima. Prikaz **Usklađivanje** može pomoći upravitelju projekta kod razvrstavanja rezervacija više resursa u dodjele zadataka. To se ne izvodi automatski jer u bilo kojem scenariju koji je složeniji od jednostavnog primjera gore, kao što je slučaj gdje postoji skupina zadataka koji čine zahtjev, namjera upravitelja projekta za dodjeljivanjem mora biti prepoznata od strane sustava. Budući da sustav ne može razumjeti namjeru, šanse su da će pretpostavke biti različite od predviđenog i da će doći do netočnog ili nepredvidljivog rezultata. Predvidljiv ishod je da generički resurs ostaje dodijeljen dok upravitelj projekta namjerno ne izradi dodjele, uz pomoć prikaza **Usklađivanje**.


