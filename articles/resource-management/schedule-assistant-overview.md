---
title: Pregled pomoćnika za raspored
description: U ovom se članku nalaze informacije o radu s pomoćnikom za raspored za rezerviranje resursa.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 884684aa572cd8444c11211a35894073d0f128b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918441"
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