---
title: Prikaz pomoćnika za raspored
description: U ovoj temi nalaze se informacije o radu s pomoćnikom za raspored za rezerviranje resursa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 309cb94ea30c525daccf032c625004c42fb408dada4b337b65d8f36d76219669
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990217"
---
# <a name="schedule-assistant-overview"></a>Prikaz pomoćnika za raspored

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Pomoćnik za raspored upotrebljava se za rezerviranje resursa na temelju zahtjeva definiranih od strane voditelja projekta. Pomoćnik za raspored oslanja se na parametre dane u preduvjetu resursa kako bi pronašao resurs. Pomoćnik za raspored preporučuje resurse koji se podudaraju s relevantnim preduvjetima, poput vremenskih okvira ili potrebnih vještina.

Nakon što se utvrde prikladni resursi, voditelj resursa ili projekta može rezervirati resurs za rad.

## <a name="prerequisites"></a>Preduvjeti

Pomoćnik za raspored dio je rješenja Universal Resource Scheduling. Ovo je rješenje uključeno i instalirano uz aplikacije Dynamics 365 Project Operations, Dynamics 365 Field Service i Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Odgovarajući zahtjevi i resursi

Preduvjet generiranog resursa temelji se na pojedinostima kao što su:

-   Značajke
-   Uloge
-   Poslovne jedinice
-   Preference resursa
-   Konture rada
-   Vremenska zona

Pomoćnik za raspored ove pojedinosti upotrebljava za filtriranje resursa.

## <a name="launch-the-schedule-assistant"></a>Pokretanje pomoćnika za raspored

Postoje dva načina na koja se pokreće pomoćnik za raspored. Ako upotrebljavate hibridni način, u rešetki članova tima možete odabrati bilo kojeg člana tima s neispunjenim preduvjetima resursa, a zatim odabrati mogućnost **Rezerviraj**. Ako koristite središnji način, resurs pronalazi i odabire upravitelj resursa.

## <a name="schedule-assistant-filters"></a>Filtri pomoćnika za raspored

Nakon pokretanja pomoćnika za raspored, pojedinosti iz preduvjeta resursa prikazuju se kao filtrirane vrijednosti u lijevom oknu. Upravitelj resursa ili projekta može precizno prilagoditi rezultate prilagodbom filtara kako bi udovoljili potrebama planiranja.

Okno filtra prikazuje mogućnosti povezane s radom, uključujući:

-   Početak i završetak rada
-   Značajke
-   Uloge
-   Organizacijske jedinice
-   Tvrtka resursa
-   Vrste resursa
-   Željeni resursi


[!INCLUDE[footer-include](../includes/footer-banner.md)]