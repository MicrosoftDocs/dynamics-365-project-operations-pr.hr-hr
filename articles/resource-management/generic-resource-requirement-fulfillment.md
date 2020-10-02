---
title: Popunjavanje zahtjeva za generičkim resursima
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za generički zahtjev resursa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897577"
---
# <a name="generic-resource-requirement-fulfillment"></a>Popunjavanje zahtjeva za generičkim resursima

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

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


