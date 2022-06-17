---
title: Rezerviraj imenovane resurse iz zahtjeva resursa
description: U ovom se članku nalaze informacije o rezervaciji imenovanih resursa za općeniti zahtjev za resursima.
author: JohnPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916233"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezerviraj imenovane resurse iz zahtjeva resursa

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete rezervirati imenovani resurs da zamjenite generički resurs koji ima zahtjev resursa.

1. U sustavu Project Service Automation (PSA) na stranici **Projekti**, kliknite karticu **Tim**.
2. S popisa odaberite generički resurs koji ima zahtjev resursa, a zatim kliknite **Rezerviraj**. Ili otvorite zahtjev resursa, a zatim kliknite **Rezerviraj**.


![Rezervacija generičkog člana tima.](media/RM-how-to-14.png)


3. Na stranici **Pomoćnik za raspored**, odaberite imenovani resurs koji ćete rezervirati u projektni tim, a zatim kliknite **Rezerviraj**.

![Rezervacija generičkog člana tima s pomoću pomoćnika za raspored.](media/RM-how-to-15.png)

Kada je rezervacija dovršena i ispunjena od strane imenovanog resursa, generički resurs zamjenjuje se imenovanim resursom.

![Imenovani član tima zamjenjuje generičkog člana tima.](media/RM-how-to-16.png)

Zadaci u rasporedu ažuriraju se i s imenovanim resursom.

![Imenovani član tima dodijeljen projektnim zadacima.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Ispunite generički resurs s više imenovanih resursa
Ispunjavanje zahtjeva za generički resurs s više imenovanih resursa slično je dodjeljivanju jednog imenovanog resursa. Na primjer, postoji zadatak u trajanju od pet dana i 120 sati napora. Ovaj zadatak ne može dovršiti jedan resurs koji odrađuje tipičan dan od osam sati u pet dana u tjednu. 

![Zadatak koji treba 120 sati rada tijekom pet dana.](media/RM-how-to-21.png)

Zahtjev je za 120 sati inženjerske robotike tijekom pet dana, što je 24 sata dnevno.

![Zahtjev po danu.](media/RM-how-to-22.png)

Ovo je primjer kada je potrebno više imenovanih resursa za ispunjavanje zahtjeva generičkog resursa. Morat ćete rezervirati više resursa za ispunjavanje zahtjeva.

![Rezervacija više resursa za ispunjavanje zahtjeva.](media/RM-how-to-23.png)

Glavna razlika u ovom scenariju je da generički resurs ostaje u timu koji je dodijeljen zadatku, a članovi tima rezerviranog imenovanog resursa ne dodjeljuju se kao dio položaja. Upravitelj projekta može dodijeliti rad po potrebi imenovanim resursima. Prikaz **Usklađivanje** može pomoći upravitelju projekta kod razvrstavanja rezervacija više resursa u dodjele zadataka. To se ne izvodi automatski jer u bilo kojem scenariju koji je složeniji od jednostavnog primjera gore, kao što je slučaj gdje postoji skupina zadataka koji čine zahtjev, namjera upravitelja projekta za dodjeljivanjem mora biti prepoznata od strane sustava. Budući da sustav ne može razumjeti namjeru, šanse su da će pretpostavke biti različite od predviđenog i da će doći do netočnog ili nepredvidljivog rezultata. Predvidljiv ishod je da generički resurs ostaje dodijeljen dok upravitelj projekta namjerno ne izradi dodjele, uz pomoć prikaza **Usklađivanje**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
