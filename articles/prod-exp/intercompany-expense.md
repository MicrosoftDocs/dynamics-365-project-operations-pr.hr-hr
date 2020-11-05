---
title: Međukompanijski troškovi
description: Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi. U ovoj situaciji možete koristiti značajku troškova unutar tvrtke kako biste troškove radnika dodijelili pravnoj osobi za koju je posao obavljen.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073539"
---
# <a name="intercompany-expenses"></a>Međukompanijski troškovi

[!include [banner](../includes/banner.md)]

Radnik koji je zaposlen u jednoj pravnoj osobi u tvrtki ili ustanovi može obavljati posao za drugu pravnu osobu u istoj tvrtki ili ustanovi. U ovoj situaciji možete koristiti značajku troškova unutar tvrtke kako biste troškove radnika dodijelili pravnoj osobi za koju je posao obavljen. Pravna osoba koja zapošljava radnika naziva se pravnom osobom koja posuđuje. Pravna osoba kojoj radnik stvara troškove naziva se pravnom osobom koja se zadužuje. 

Prije nego što radnik može stvoriti i poslati troškove za rad koji se obavlja za drugu pravnu osobu, u pravnoj osobi koja posuđuje, na stranici **Parametri upravljanja troškovima** odaberite mogućnost **Omogući retke troška unutar tvrtke**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Knjiženje poreza za troškove unutar kompanije

[!include [banner](../includes/banner.md)]

Ako želite upotrebljavati porezne grupe koje su povezane s pravnom osobom koja posuđuje (izvor) umjesto pravne osobe koja se zadužuje (odredište), u svom izvješću o troškovima morat ćete to konfigurirati u postavkama PDV-a u glavnoj knjizi. Kada parametar **Pravna osoba za knjiženje poreza unutar kompanije** glavne knjige postavljen na **Izvor** , a **Primijeni pravila oporezivanja PDV-om** postavljen na **Ne** , upotrijebit će se porezna kombinacija za pravnu osobu koja posuđuje. Kada je isti parametar postavljen na **Odredište** , koristit će se porezna kombinacija za zaduženu pravnu osobu. Za pravne osobe u SAD-u, kada je parametar postavljen na **Izvor** , polje **Potraživanje od poreza na promet** također mora biti konfigurirano na novoj stranici **Grupe za knjiženje u glavnu knjigu**. Računovodstveni mehanizam upotrijebit će podatke iz ovog polja za računovodstveno knjiženje u vezi s porezom.   
Ponašanje je u skladu s redcima troškova knjiženim s projektom ili bez njega.  
