---
title: Popunjavanje zahtjeva za generičkim resursima
description: U ovoj temi nalaze se informacije o načinu rezerviranja imenovanih resursa za preduvjet generičkog resursa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130298"
---
# <a name="generic-resource-requirement-fulfillment"></a>Popunjavanje zahtjeva za generičkim resursima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Možete rezervirati imenovani resurs da zamjenite generički resurs koji ima zahtjev resursa.

1. Na stranici **Projekti** odaberite karticu **Tim**.
2. S popisa odaberite generički resurs koji ima zahtjev za resursom, a zatim odaberite **Rezerviraj**. Ili otvorite zahtjev za resursom, a zatim odaberite **Rezerviraj**.
3. Na stranici **Pomoćnik za raspored**, odaberite imenovani resurs koji ćete rezervirati u projektni tim, a zatim odaberite **Rezerviraj**.

Kada je rezervacija dovršena i ispunjena od strane imenovanog resursa, generički resurs zamjenjuje se imenovanim resursom.

Zadaci u rasporedu ažuriraju se i s imenovanim resursom.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Ispunite generički resurs s više imenovanih resursa
Ispunjavanje zahtjeva za generički resurs s više imenovanih resursa slično je dodjeljivanju jednog imenovanog resursa. Na primjer, postoji zadatak u trajanju od pet dana i 120 sati napora. Ovaj zadatak ne može dovršiti jedan resurs koji odrađuje uobičajeni osmosatni radni dan tijekom pet dana u tjednu. 

Zahtjev je za 120 sati inženjerske robotike tijekom pet dana, što je 24 sata dnevno.

Ovo je primjer kada je potrebno više imenovanih resursa za ispunjavanje zahtjeva generičkog resursa. Morat ćete rezervirati više resursa za ispunjavanje zahtjeva.

Glavna razlika u ovom scenariju je da generički resurs ostaje u timu koji je dodijeljen zadatku, a članovi tima rezerviranog imenovanog resursa ne dodjeljuju se kao dio položaja. Upravitelj projekta može dodijeliti rad po potrebi imenovanim resursima. Prikaz **Usklađivanje** može pomoći upravitelju projekta kod razvrstavanja rezervacija više resursa u dodjele zadataka. To se ne izvodi automatski jer u bilo kojem scenariju koji je složeniji od jednostavnog primjera gore, kao što je slučaj gdje postoji skupina zadataka koji čine zahtjev ili namjera upravitelja projekta za dodjeljivanjem mora biti prepoznata od strane sustava. Budući da sustav ne može razumjeti namjeru, vjerojatnije je kako će se pretpostavke razlikovati od namjere i pojavit će se netočan ili nepredvidljiv rezultat. Predvidljiv ishod je da generički resurs ostaje dodijeljen dok upravitelj projekta namjerno ne izradi dodjele, uz pomoć prikaza **Usklađivanje**.


